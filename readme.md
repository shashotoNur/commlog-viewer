# Calls & SMS Viewer

A lightweight, local-first web tool for viewing and managing your combined call logs and SMS backups. This single HTML file runs entirely in your browser, ensuring your data remains private and secure on your device.

-----

## Features

  * **Secure & Private:** No data is ever uploaded or sent to a server. The entire application runs directly in your web browser.
  * **Unified View:** Seamlessly merges call logs and SMS messages into a single, chronological conversation thread per contact.
  * **Intuitive Navigation:** Contacts are sorted by the most recent communication, making it easy to find active conversations.
  * **Dual Search Functionality:** Search for contacts by name or number, and search for specific keywords within messages and call logs.
  * **Clear Labeling:** Messages and calls are clearly differentiated with distinct styles and labels.
  * **Date Highlighting:** Date dividers separate messages and calls by day, helping you visualize the timeline of your conversations.

-----

## Usage

Using the Calls & SMS Viewer is incredibly simple. You don't need any special software—just a modern web browser.

### Step 1: Get the Viewer

Since this app is a single HTML file, you can get it in two ways:

1.  **Directly from GitHub Pages:** Access the live version of the app hosted on [GitHub Pages](https://shashotonur.github.io/calls-sms-viewer/).
2.  **Download the Code:** Clone the repository or download the `index.html` file to your computer.

### Step 2: Open the Viewer

If you downloaded the file, open it by double-clicking it or by dragging it into your web browser window.

### Step 3: Load Your Data

In the top-left corner, you'll see two buttons represented by an SVG icon for messages  and another for a phone .

  * Click the **message icon** to select your SMS backup file.
  * Click the **phone icon** to select your call log backup file.

The viewer will automatically parse the data, merge it, and display your conversations. You can load files in any order; the application will handle the merging in the background.

-----

## Required XML File Structures

This application is designed to work with XML backup files created by popular Android apps. Your files must adhere to one of the following structures:

### SMS File Structure (`<sms>` tags)

Each message should be represented by an `<sms>` tag with the following attributes:

  * `address`: The phone number of the contact.
  * `date`: The Unix timestamp of the message.
  * `type`: The type of message (e.g., `1` for received, `2` for sent).
  * `body`: The content of the message.
  * `readable_date`: The human-readable date and time.
  * `contact_name`: The name of the contact, if available.

### Call Log File Structure (`<call>` tags)

Each call should be represented by a `<call>` tag with these attributes:

  * `number`: The phone number of the contact.
  * `duration`: The duration of the call in seconds.
  * `date`: The Unix timestamp of the call.
  * `type`: The type of call (e.g., `1` for incoming, `2` for outgoing, `3` for missed, `5` for rejected).
  * `readable_date`: The human-readable date and time.
  * `contact_name`: The name of the contact, if available.

-----

## License

This project is open-source and available under the **MIT License**.
