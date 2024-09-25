**Advanced Firewall Application Documentation**

### Overview
The Advanced Firewall Application is developed to filter network traffic by evaluating packets based on IP addresses, ports, and protocols. It leverages the Singleton, Strategy, and Factory design patterns to promote flexibility and maintainable architecture.

### Components

#### 1.1 Singleton Pattern: Settings Class
The `Settings` class implements the Singleton pattern to ensure only one instance exists. This instance holds the firewall's default policy.

#### 1.2 Strategy Pattern: FirewallStrategy Abstract Base Class
The `FirewallStrategy` abstract class defines a common interface for different packet filtering strategies, allowing for flexibility in implementation.

#### 1.3 Concrete Strategies

- **IPFilter Class**: Manages packet filtering based on whitelists and blacklists of IP addresses.
- **PortFilter Class**: Filters packets by allowed ports.
- **ProtocolFilter Class**: Filters packets by approved protocols.

#### 1.4 Factory Pattern: StrategyFactory Class
The `StrategyFactory` class provides a centralized method for creating different filtering strategies, such as IP, port, or protocol filters.

### Main Script
The main script initializes the firewall's filters and processes incoming packets. It allows users to input packet details, checks them against the filters, and determines whether to allow or block the packet based on IP, port, and protocol.

### Web Interface
The web interface enables users to enter packet information via a form. The interface validates and submits packet details to the server, where the firewall application checks if the packet is allowed or denied. This interface uses HTML and CSS for styling and includes a simple JavaScript function for handling form submissions.

### Usage

1. **Run the Python Script**: Launch the script to start the firewall.
2. **Web Interface**: After starting the script, open the HTML link in a browser. Enter the packet details (IP address, port, protocol) to check if the packet is permitted or denied.

### Conclusion
The Advanced Firewall Application provides a highly adaptable system for filtering network packets. Through the use of design patterns, the application maintains a balance of flexibility, maintainability, and ease of future enhancements.
