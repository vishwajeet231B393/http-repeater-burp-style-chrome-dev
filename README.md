# HTTP Repeater for Chrome DevTools

A lightweight Chrome DevTools extension that functions similarly to Burp Suite's Repeater tool. This extension allows developers and security researchers to intercept, modify, and replay HTTP requests directly within the browser, eliminating the need for external proxies or certificate configurations.

## Features

* **Direct Integration:** Runs entirely within Chrome DevTools as a dedicated panel.
* **Request Manipulation:** Capture HTTP requests and modify the method, URL, headers, and body before resending.
* **No Proxy Required:** Works directly with the browser's network stack, requiring no external proxy setup or CA certificate installation.
* **Response Analysis:** View raw response headers and body content immediately after replaying a request.
* **History Tracking:** Maintains a session-based history of sent requests for quick comparison.
* **Syntax Highlighting:** Basic formatting for JSON, XML, and HTML response bodies.

## Prerequisites

* Google Chrome, Brave, or any Chromium-based browser.
* Developer Mode enabled in the browser's extension settings.

## Installation

This extension is installed as an unpacked extension in Developer Mode.

1. Download or clone this repository to your local machine.
2. Open your browser and navigate to the Extensions management page (usually found at chrome://extensions).
3. Enable **Developer mode** using the toggle switch in the top right corner.
4. Click the **Load unpacked** button.
5. Select the directory where you downloaded/cloned this repository.
6. The extension should now appear in your list of installed extensions.

## Usage

1. **Open DevTools:** Navigate to any webpage, right-click anywhere on the page, and select **Inspect**, or press F12.
2. **Locate the Panel:** Look for the new tab labeled **HTTP Repeater** (or similar) in the top DevTools navigation bar. If it is not visible, click the double arrows (>>) to reveal hidden tabs.
3. **Capture a Request:** Browse the website as normal. Requests will populate in the extension's sidebar.
4. **Edit and Send:** Click on a captured request to load it into the editor. Modify the parameters as needed and click **Send** to replay the request.
5. **View Response:** The server response will appear in the adjacent panel for analysis.

## Limitations

* **Browser Restrictions:** Certain headers (e.g., Content-Length, Host) are managed by the browser and may not be fully overrideable due to security policies.
* **CORS:** Cross-Origin Resource Sharing (CORS) restrictions may apply depending on the target server's configuration, though the extension attempts to bypass standard checks where possible.

## License

Distributed under the MIT License. See LICENSE for more information.
