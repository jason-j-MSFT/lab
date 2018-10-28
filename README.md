Launch a VM in Azure.  This will create a:
1. Resource Group
1. VNET
1. Subnet
1. Linux VM
    1. port 22 open and listening for SSH

<a href="https://azuredeploy.net/" target="_blank">
    <img src="http://azuredeploy.net/deploybutton.png"/>
</a>
<a href="http://armviz.io/#/?load=https://raw.githubusercontent.com/DarylsCorner/ARM-Templates/master/vm-from-user-image/azuredeploy.json" target="_blank">
  <img src="http://armviz.io/visualizebutton.png"/>
</a>

# System Security

## Secure shell (SSH)
### Configure and secure an SSH daemon.  Managing keys and configuring SSH for users. Forward an application protocol over SSH and manage the SSH login.

**Key Knowledge Areas:**

1. OpenSSH configuration files, tools and utilities  
1. Login restrictions for the superuser and the normal users  
1. Managing and using server and client keys to login with and without password  
1. Usage of multiple connections from multiple hosts to guard against loss of connection to remote host following configuration changes

**Terms and Utilities:**

* ssh
* sshd
* /etc/ssh/sshd_config
* /etc/ssh/
* Private and public key files
* PermitRootLogin, PubKeyAuthentication, AllowUsers, PasswordAuthentication, Protocol

## Configuring a router
### Configure a system to forward IP packet and perform network address translation (NAT, IP masquerading) and state its significance in protecting a network. Configuring port redirection, managing filter rules and averting attacks.

**Key Knowledge Areas:**

1. iptables and ip6tables configuration files, tools and utilities  
1. Tools, commands and utilities to manage routing table  
1. Private address ranges (IPv4) and Unique Local Addresses as well as Link Local Addresses (IPv6)  
1. Port redirection and IP forwarding  
1. List and write filtering and rules that accept or block IP packets based on source or destination protocol, port and address  
1. Save and reload filtering configurations

**Terms and Utilities:**

* /proc/sys/net/ipv4/
* /proc/sys/net/ipv6/
* /etc/services
* iptables
* ip6tables
 

## Securing FTP servers
### Configure an FTP server for anonymous downloads and uploads. Precautions to be taken if anonymous uploads are permitted and configuring user access.

**Key Knowledge Areas:**

1. Configuration files, tools and utilities for Pure-FTPd and vsftpd
1. Awareness of ProFTPd
1. Understanding of passive vs. active FTP connections

**Terms and Utilities:**

* vsftpd.conf
* important Pure-FTPd command line options

## Security tasks
### Receive security alerts from various sources, install, configure and run intrusion detection systems and apply security patches and bugfixes.

**Key Knowledge Areas:**

1. Tools and utilities to scan and test ports on a server
1. Locations and organizations that report security alerts as Bugtraq, CERT or other sources
1. Tools and utilities to implement an intrusion detection system (IDS)
1. Awareness of OpenVAS and Snort

Terms and Utilities:

* telnet
* nmap
* fail2ban
* nc
* iptables
 

## OpenVPN
### Configure a VPN (Virtual Private Network) and create secure point-to-point or site-to-site connections.

**Key Knowledge Areas:**

1. OpenVPN

**Terms and Utilities:**

* /etc/openvpn/
* openvpn

# Domain Name Server

## Basic DNS server configuration
### Configure BIND to function as a caching-only DNS server. Manage a running server and configuring logging.

**Key Knowledge Areas:**

1. BIND 9.x configuration files, terms and utilities
1. Defining the location of the BIND zone files in BIND configuration files
1. Reloading modified configuration and zone files
1. Awareness of dnsmasq, djbdns and PowerDNS as alternate name servers

**Terms and utilities:**

* /etc/named.conf
* /var/named/
* /usr/sbin/rndc
* kill
* host
* dig
 

## Create and maintain DNS zones
### Create a zone file for a forward or reverse zone and hints for root level servers. Setting appropriate values for records, adding hosts in zones and adding zones to the DNS. Delegate zones to another DNS server.

**Key Knowledge Areas:**

1. BIND 9 configuration files, terms and utilities
1. Utilities to request information from the DNS server
1. Layout, content and file location of the BIND zone files
1. Various methods to add a new host in the zone files, including reverse zones

**Terms and Utilities:**

* /var/named/
* zone file syntax
* resource record formats
* named-checkzone
* named-compilezone
* masterfile-format
* dig
* nslookup
* host
 

## Securing a DNS server
### Configure a DNS server to run as a non-root user and run in a chroot jail. This objective includes secure exchange of data between DNS servers.

**Key Knowledge Areas:**

1. BIND 9 configuration files
1. Configuring BIND to run in a chroot jail
1. Split configuration of BIND using the forwarders statement
1. Configuring and using transaction signatures (TSIG)
1. Awareness of DNSSEC and basic tools
1. Awareness of DANE and related records

**Terms and Utilities:**

* /etc/named.conf
* /etc/passwd
* DNSSEC
* dnssec-keygen
* dnssec-signzone

# Web Services

## Implementing a web server
### Install and configure a web server. Monitoring the server’s load and performance, restricting client user access, configuring support for scripting languages as modules and setting up client user authentication. Configuring server options to restrict usage of resources. Configure a web server to use virtual hosts and customize file access.

**Key Knowledge Areas:**

1. Apache 2.4 configuration files, terms and utilities
1. Apache log files configuration and content
1. Access restriction methods and files
1. mod_perl and PHP configuration
1. Client user authentication files and utilities
1. Configuration of maximum requests, minimum and maximum servers and clients
1. Apache 2.4 virtual host implementation (with and without dedicated IP addresses)
1. Using redirect statements in Apache’s configuration files to customize file access

**Terms and Utilities:**

* access logs and error logs
* .htaccess
* httpd.conf
* mod_auth_basic, mod_authz_host and mod_access_compat
* htpasswd
* AuthUserFile, AuthGroupFile
* apachectl, apache2ctl
* httpd, apache2
 

## Apache configuration for HTTPS
### Configure a web server to provide HTTPS.

**Key Knowledge Areas:**

1. SSL configuration files, tools and utilities
1. Generate a server private key and CSR for a commercial CA
1. Generate a self-signed Certificate
1. Install the key and certificate, including intermediate CAs
1. Configure Virtual Hosting using SNI
1. Awareness of the issues with Virtual Hosting and use of SSL
1. Security issues in SSL use, disable insecure protocols and ciphers

**Terms and Utilities:**

* Apache2 configuration files
* /etc/ssl/, /etc/pki/
* openssl, CA.pl
* SSLEngine, SSLCertificateKeyFile, SSLCertificateFile
* SSLCACertificateFile, SSLCACertificatePath
* SSLProtocol, SSLCipherSuite, ServerTokens, ServerSignature, TraceEnable
 

## Implementing a proxy server
### Install and configure a proxy server, including access policies, authentication and resource usage.

**Key Knowledge Areas:**

1. Squid 3.x configuration files, terms and utilities
1. Access restriction methods
1. Client user authentication methods
1. Layout and content of ACL in the Squid configuration files

**Terms and Utilities:**

* squid.conf
* acl
* http_access
 
## Implementing Nginx as a web server and a reverse proxy
### Install and configure a reverse proxy server, Nginx. Basic configuration of Nginx as a HTTP server is included.

**Key Knowledge Areas:**

1. Nginx
1. Reverse Proxy
1. Basic Web Server

**Terms and Utilities:**

* /etc/nginx/
* nginx

# File Sharing

## SAMBA Server Configuration
### Set up a Samba server for various clients.  Setting up Samba as a standalone server as well as integrating Samba as a member in an Active Directory. Configuration of simple CIFS and printer shares. Configuring a Linux client to use a Samba server. Troubleshooting installations.

**Key Knowledge Areas:**

1. Samba 4 documentation
1. Samba 4 configuration files
1. Samba 4 tools and utilities and daemons
1. Mounting CIFS shares on Linux
1. Mapping Windows user names to Linux user names
1. User-Level, Share-Level and AD security

**Terms and Utilities:**

* smbd, nmbd, winbindd
* smbcontrol, smbstatus, testparm, smbpasswd, nmblookup
* samba-tool
* net
* smbclient
* mount.cifs
* /etc/samba/
* /var/log/samba/
 
## NFS Server Configuration
### Export filesystems using NFS. This objective includes access restrictions, mounting an NFS filesystem on a client and securing NFS.

**Key Knowledge Areas:**

1. NFS version 3 configuration files
1. NFS tools and utilities
1. Access restrictions to certain hosts and/or subnets
1. Mount options on server and client
1. TCP Wrappers
1. Awareness of NFSv4

**Terms and Utilities:

* /etc/exports
* exportfs
* showmount
* nfsstat
* /proc/mounts
* /etc/fstab
* rpcinfo
* mountd
* portmapper

# Network Client Management

## DHCP configuration
### Configure a DHCP server. Setting default and per client options, adding static hosts and BOOTP hosts. Configuring a DHCP relay agent and maintaining the DHCP server.

**Key Knowledge Areas:**

1. DHCP configuration files, terms and utilities
1. Subnet and dynamically-allocated range setup
1. Awareness of DHCPv6 and IPv6 Router Advertisements

**Terms and Utilities:**

* dhcpd.conf
* dhcpd.leases
* DHCP Log messages in syslog or systemd journal
* arp
* dhcpd
* radvd
* radvd.conf
 

## PAM authentication
### Configure PAM to support authentication using various available methods. Basic SSSD functionality.

**Key Knowledge Areas:**

1. PAM configuration files, terms and utilities
1. passwd and shadow passwords
1. Use sssd for LDAP authentication

**Terms and Utilities:**

* /etc/pam.d/
* pam.conf
* nsswitch.conf
* pam_unix, pam_cracklib, pam_limits, pam_listfile, pam_sss
* sssd.conf
 

## LDAP client usage
### Perform queries and updates to an LDAP server. Importing and adding items, as well as adding and managing users.

**Key Knowledge Areas:**

1. LDAP utilities for data management and queries
1. Change user passwords
1. Querying the LDAP directory

**Terms and Utilities:**

* ldapsearch
* ldappasswd
* ldapadd
* ldapdelete
 

## Configuring an OpenLDAP server
### Configure a basic OpenLDAP server including knowledge of LDIF format and essential access controls.

**Key Knowledge Areas:**

1. OpenLDAP
1. Directory based configuration
1. Access Control
1. Distinguished Names
1. Changetype Operations
1. Schemas and Whitepages
1. Directories
1. Object IDs, Attributes and Classes

**Terms and Utilities:**

* slapd
* slapd-config
* LDIF
* slapadd
* slapcat
* slapindex
* /var/lib/ldap/
* loglevel

# E-Mail Services

## Using e-mail servers
### Manage an e-mail server, including the configuration of e-mail aliases, e-mail quotas and virtual e-mail domains. Configuring internal e-mail relays and monitoring e-mail servers.

**Key Knowledge Areas:**

1. Configuration files for postfix
1. Basic TLS configuration for postfix
1. Basic knowledge of the SMTP protocol
1. Awareness of sendmail and exim

**Terms and Utilities:**

* Configuration files and commands for postfix
* /etc/postfix/
* /var/spool/postfix/
* sendmail emulation layer commands
* /etc/aliases
* mail-related logs in /var/log/
 

## Managing E-Mail Delivery
### Implement client e-mail management software to filter, sort and monitor incoming user e-mail.

**Key Knowledge Areas:**

1. Understanding of Sieve functionality, syntax and operators
1. Use Sieve to filter and sort mail with respect to sender, recipient(s), headers and size
1. Awareness of procmail

**Terms and Utilities:**

* Conditions and comparison operators
* keep, fileinto, redirect, reject, discard, stop
* Dovecot vacation extension
 
## Managing Remote E-Mail Delivery

### Install and configure POP and IMAP daemons.

**Key Knowledge Areas:**

1. Dovecot IMAP and POP3 configuration and administration
1. Basic TLS configuration for Dovecot
1. Awareness of Courier

**Terms and Utilities:**

* /etc/dovecot/
* dovecot.conf
* doveconf
* doveadm
