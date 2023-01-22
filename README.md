# Home selfhosting using Ansible
This is the setup I use for selfhosting my favourite services on my home server.

![Homer homepage](.github/homer.png)

### Getting Started
To get started with this project, clone the repository.
Then you'll need a Debian 11 system with SSH access configured.

### Prerequisites

- Debian 11 (for the server)
- Ansible >2.14 (on your machine)

### Deployment
To run the Ansible Playbook on your server run the following commmand:
```
ansible-playbook run.yml -i myinventory
```
Where `myinventory` contains your host configuration.

### Available roles
- Frontends
    - Libreddit
    - Nitter
    - Invidious
- Services
    - Linkding
    - Wireguard UI
    - Syncthing

### Security
This configuration is intended to be used within your local network or via a Wireguard VPN connection.
The secure HTTPS protocol is not currently used, so it is strongly discouraged to expose the ports of services on the Internet, because all traffic will be sent unencrypted.

### Hardware
The hardware I use is a Fujitsu Futro S920, with the following configuration:
- CPU: AMD GX-415GA SOC (4 core) @ 1.5GHz
- RAM: 4GB DDR3
- SSD: 120GB Crucial mSata 

### Acknowledgments
Thanks to [@notthebee](https://github.com/notthebee) for inspiring me with his [video](https://www.youtube.com/watch?v=f5jNJDaztqk).