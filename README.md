# Monkey in the Middle
I built this lab as part of CodePath’s CYB102 cybersecurity course to gain hands-on experience analyzing encrypted and unencrypted network traffic. The goal was to understand how HTTPS encryption protects data in transit, and how a proxy server like mitmproxy can **intercept and decrypt** that traffic when configured correctly. After completing this lab, I learned how to analyze traffic with Wireshark, set up and configure mitmproxy, and intercept and modify HTTP requests in real-time.

## Tools & Technologies Used
- Ubuntu 22.04 LTS VM (Azure Lab or local VirtualBox)
- Wireshark
- mitmproxy (Docker container)
- Firefox (proxy configuration and testing)
- curl (for HTTP request testing)

## What This Lab Does
- Captures encrypted HTTPS traffic using Wireshark and analyzes packet data.
- Installs mitmproxy in a Docker container to intercept HTTPS traffic.
- Configures Firefox to route traffic through mitmproxy and trusts the proxy’s certificate.
- Compares the visibility of encrypted traffic in Wireshark versus decrypted traffic in mitmproxy.
- Intercepts and modifies HTTP requests in transit (example: changing a weather API query).

## Screenshots
### Configuring Firefox to allow a proxy:
<img src="https://github.com/user-attachments/assets/ce85232e-b59a-464e-a495-d0ecfd40a9d7" width="600"/>

### Viewing intercepted traffic in mitmproxy:
<img src="https://github.com/user-attachments/assets/4a612282-123b-40ab-9bb5-ab90f1e04a25" width="600"/>

### Before mitmproxy modification (weather for Dunedin)
<img src="https://github.com/user-attachments/assets/1b92fc8d-b08f-4260-830b-c375bb993b56" width="600"/>

### After mitmproxy modification (weather for Innsbruck)
<img src="https://github.com/user-attachments/assets/76bbc38f-747b-4410-8894-ad1c1335988b" width="600"/>

### How mitmproxy works as a man-in-the-middle proxy
<img src="https://github.com/user-attachments/assets/9610a01c-3484-4952-9a22-577a8332a6f2" width="600"/>
