**Home Networking Troubleshooting Guide**

Structured Debian home-network troubleshooting using routing, DNS, ping, and HTTP validation.

**Network Troubleshooting Decision Tree**

- Provides a systematic process for troubleshooting a network connectivity issue instead of making random changes.
- Starts with the local Debian workstation and moves outward through Wi-Fi, IP addressing, the default gateway, Internet connectivity, DNS, and application access.
- Uses each successful test to narrow the possible failure point before moving to the next layer.
- Separates a single-device problem from a broader router, modem, or ISP issue.
- Defines the point where local troubleshooting ends and escalation to the ISP becomes appropriate.

![Network Troubleshooting Decision Tree](images/01-decision-tree.png)


**Network Troubleshooting Layers**

- Organizes network troubleshooting as a series of layers moving outward from the local interface.
- Shows the relationship between IP configuration, the default gateway, router connectivity, external connectivity, DNS, and the application layer.
- Reinforces the principle of validating one layer before moving outward to the next.
- Provides a simple mental model that can be applied to larger business and enterprise network environments.

![Network Troubleshooting Layers](images/02-network-layers.png)


**Network Connectivity Validation**

- Verified external IP connectivity by successfully reaching 8.8.8.8 with no packet loss.
- Used DNS lookup to confirm that the hostname github.com successfully resolved to an IP address.
- Reviewed the default route to identify the local gateway used by the Debian workstation to reach networks outside the local subnet.
- These checks validate routing, external connectivity, and DNS resolution before moving to application-level troubleshooting.

![Network Connectivity Validation](images/03-network-validation.png)


**HTTP Application Validation**

- Used curl to test HTTPS connectivity to github.com from the Debian workstation.
- Received an HTTP/2 200 response, confirming that the remote web service successfully responded.
- Demonstrates the final application-level validation after routing, external connectivity, and DNS have already been confirmed.

![HTTP Application Validation](images/04-http-validation.png)

