# Bind9 Service Repository

<div class="center-image">
   <img src="https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExMmN6c2QzeXR2NWhtMjhtZGphNWRkNDAwaTN3MnpuaHIza3R4anBoMyZlcD12MV9pbnRlcm5faWZfYnlfaWQmY3Q9Zw/xTiTnxpQ3ghPiB2Hp6/giphy.gif" alt="Bind9 Setup">
</div>

<!-- ![Bind9 Setup](https://i.giphy.com/media/v1.Y2lkPTc5MGI3NjExMmN6c2QzeXR2NWhtMjhtZGphNWRkNDAwaTN3MnpuaHIza3R4anBoMyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/xTiTnxpQ3ghPiB2Hp6/giphy.gif) -->

## Overview

This repository contains the configuration and setup scripts for a Bind9 DNS server. Bind9 is a widely used open-source DNS server that provides domain name resolution services. This repository aims to simplify the deployment and management of Bind9 in various environments.

## Features

- **Easy Setup**: Scripts to install and configure Bind9.
- **Custom Configuration**: Templates for custom DNS zone files.
- **Security**: Guidelines and configurations for securing the Bind9 service.
- **Scalability**: Instructions for setting up Bind9 in a scalable architecture.
- **Monitoring**: Integration with monitoring tools for tracking performance and health.

## Getting Started

### Prerequisites

- A Linux-based operating system (Ubuntu/Debian/CentOS).
- Root or sudo access to the server.
- Basic understanding of DNS concepts.

### Installation

1. **Clone the repository**:
   ```sh
   git clone https://github.com/PedreirosDeBurnout/bind9.git
   cd bind9-service
   ```

2. **Run the setup script**:
   ```sh
   sudo ./setup.sh
   ```

   The script will install Bind9 and apply the default configuration.

### Configuration

1. **Edit the main configuration file**:
   ```sh
   sudo nano /etc/bind/named.conf.options
   ```

2. **Add or modify DNS zones**:
   - Zone files are located in `/etc/bind/zones/`.
   - Use the provided templates to create new zone files.
   - Update the main configuration to include your new zones.

3. **Restart Bind9 to apply changes**:
   ```sh
   sudo systemctl restart bind9
   ```

### Customization

- **Zone File Templates**: Modify the templates in the `zones-templates/` directory to fit your requirements.
- **Security Enhancements**: Follow the guidelines in the `security/` directory to enhance the security of your Bind9 service.

### Monitoring

- Integrate with monitoring tools like Nagios, Zabbix, or Prometheus using the provided configurations in the `monitoring/` directory.

## Contributing

We welcome contributions to improve this repository. Please fork the repository, create a new branch, and submit a pull request with your changes.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Bind9 Documentation](https://bind9.readthedocs.io/en/latest/)
- Community contributors

---

By following this README, you should be able to set up and manage a Bind9 DNS server efficiently. If you encounter any issues, please refer to the troubleshooting section or open an issue in the repository.

## Troubleshooting

- **Common Issues**: Refer to the `troubleshooting.md` file for common issues and solutions.
- **Logs**: Check the Bind9 logs located in `/var/log/named/` for detailed error messages.
- **Support**: Open an issue in the GitHub repository for further assistance.

---

Happy DNS serving!