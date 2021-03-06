# OpenVPN

Create OpenVPN server on AWS EC2.

## Requirement

- terraform

## Usage

### Setup VPN server

Configure security group and allow UDP 1194 port inbound traffic.

Launch EC2 instance and download client key.

```
terraform apply
```

### Connect to VPN Server

Install some packages.

```
sudo apt-get install network-manager-openvpn network-manager-openvpn-gnome
```

Select `VPN connection -> VPN setting -> Add -> Import VPN configuration` from network icon and select `client/client.conf`.

Modify `Gateway` IP Address.

After all, connect to VPN server and enjoy internet!

### Destroy VPN server

After disconnect to VPN server, you can terminate VPN server.

```
terraform destroy
```

## Author

[shibataka000](https://github.com/shibataka000)
