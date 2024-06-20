#  SMB
SMB - Server Message Block Protocol - is a client-server communication protocol used for sharing access to files, printers, serial ports and other resources on a network. 
Servers make file systems and other resources (printers, named pipes, APIs) available to clients on the network.
Client computers may have their own hard disks, but they also want access to the shared file systems and printers on the servers.
The SMB protocol is known as a response-request protocol, meaning that it transmits multiple messages between the client and server to establish a connection.
Clients connect to servers using TCP/IP (actually NetBIOS over TCP/IP as specified in RFC1001 and RFC1002), NetBEUI or IPX/SPX.

###  Enumerating SMB
Typically, there are SMB share drives on a server that can be connected to and used to view or transfer files.
SMB can often be a great starting point for an attacker looking to discover sensitive information — you'd be surprised what is sometimes included on these shares.

- Enum4linux
Enum4linux is a tool used to enumerate SMB shares on both Windows and Linux systems.
It is basically a wrapper around the tools in the Samba package and makes it easy to quickly extract information from the target pertaining to SMB.

Performs all possible enumeration (shares, users, groups, sessions, etc.).
- `enum4linux -A TARGET_IP`

If the SMB server is part of a domain, you can specify the domain.
- `enum4linux -A -d DOMAIN_NAME TARGET_IP`

To list only the users on an SMB server.
- `enum4linux -U TARGET_IP`

To list only the shares available on an SMB server.
- `enum4linux -S TARGET_IP`

To list only the groups on an SMB server.
- `enum4linux -G TARGET_IP`


###  SMBClient & SMBmap
We will be using SMBClient because it's part of the default samba suite. We can remotely access the SMB share using SMBClient and SMBmap.

Connect to smb server.
- `smbclient //<SERVER_IP>/<SHARE_NAME> -U <USERNAME>`

List available shares on remote IP.
- `smbclient -L IP`

Access remote shares with anonymous login.
- `smbclient //IP/<path> -N`

Map available shares on remote server.
- `smbmap -H IP`

Access remote shares.
- `smbmap -H IP -u 'username' -p 'pass'`

After accessed on the remote share you can retrieve system information.
```
smb: \> showconfig
smb: \> showversion
smb: \> showcap
```

