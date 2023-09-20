import requests
import json
import tkinter as tk
from tkinter import messagebox

# Function to retrieve the abuse report
def get_abuse_report():
    # Get the IP address from the entry field
    ip_address = ip_entry.get()

    # Check if the IP address is empty
    if not ip_address:
        messagebox.showerror("Error", "Please enter an IP address")
        return

    # Define the API endpoint and parameters
    url = 'https://api.abuseipdb.com/api/v2/check'
    querystring = {
        'ipAddress': ip_address,
        'maxAgeInDays': '90'
    }
    headers = {
        'Accept': 'application/json',
        'Key': 'enter your key'
    }

    # Send the API request
    response = requests.get(url=url, headers=headers, params=querystring)

    # Formatted output
    decoded_response = json.loads(response.text)
    result_text.config(state=tk.NORMAL)  # Enable text widget for editing
    result_text.delete('1.0', tk.END)    # Clear previous results
    result_text.insert(tk.END, json.dumps(decoded_response, sort_keys=True, indent=4))
    result_text.config(state=tk.DISABLED)  # Disable text widget for editing

# Create the main tkinter window
window = tk.Tk()
window.title("AbuseIPDB Checker")

# Create and configure the IP address input field
ip_label = tk.Label(window, text="Enter IP Address:")
ip_label.pack()
ip_entry = tk.Entry(window)
ip_entry.pack()

# Create a button to trigger the API request
check_button = tk.Button(window, text="Check AbuseIPDB", command=get_abuse_report)
check_button.pack()

# Create a text widget to display the results
result_text = tk.Text(window, wrap=tk.WORD, width=40, height=10)
result_text.pack()
result_text.config(state=tk.DISABLED)  # Disable text widget for editing

# Start the tkinter main loop
window.mainloop()
