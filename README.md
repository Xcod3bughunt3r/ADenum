<p align="left"><a href="https://www.itsecurity.id/"><img height="150" title="Xcod3bughunt3r" src="face.png"/></a></p>

# `Active Directory Enumeration`
#### **ADEnum.py** `is a pentesting tool that allows to find misconfiguration through the protocol LDAP and exploit some of those weaknesses with Kerberos.`

___

```text

   █████╗ ██████╗     ███████╗███╗   ██╗██╗   ██╗███╗   ███╗
  ██╔══██╗██╔══██╗    ██╔════╝████╗  ██║██║   ██║████╗ ████║
  ███████║██║  ██║    █████╗  ██╔██╗ ██║██║   ██║██╔████╔██║
  ██╔══██║██║  ██║    ██╔══╝  ██║╚██╗██║██║   ██║██║╚██╔╝██║
  ██║  ██║██████╔╝    ███████╗██║ ╚████║╚██████╔╝██║ ╚═╝ ██║
  ╚═╝  ╚═╝╚═════╝     ╚══════╝╚═╝  ╚═══╝ ╚═════╝ ╚═╝     ╚═╝


usage: ADenum.py -d [domain] -u [username] -p [password]

Pentest tool that detect misconfig in AD with LDAP

options:
  -h, --help          show this help message and exit
  -d  [domain]        The name of domain (e.g. "test.local")
  -u  [username]      The user name
  -p  [password]      The user password
  -ip [ipAddress]     The IP address of the server (e.g. "1.1.1.1")
  -j                  Enable hash cracking (john)
  -jp [path]          John binary path
  -w  [wordList]      The path of the wordlist to be used john (Default: /usr/share/seclists/Passwords/Leaked-
                      Databases/rockyou.txt
  -v, --version       Show program's version number and exit
  -s                  Use LDAP with SSL
  -c, --NPUsersCheck  Check with GetNPUsers.py for ASREP Roastable
```

___

## `Requirement`
- [Impacket](https://github.com/SecureAuthCorp/impacket)
- [John](https://github.com/openwall/john)
- [Python 3](https://www.python.org/)
- `If you are using` **debian** `or` **ubuntu** `:`

	```bash
	$ sudo apt-get install libsasl2-dev python-dev libldap2-dev libssl-dev
	```

- `If you are using` **kali** :

	```bash
	$ sudo apt-get install libsasl2-dev python2-dev libldap2-dev libssl-dev
	```

- `pip3:`

	```bash
	$ pip3 install -r requirements.txt
	```

## `Features and Functionality`
### `LDAP`
- Enum Domain Admin users
- Enum Domain Controllers
- Enum Domain users with Password Not Expire
- Enum Domain users with old password
- Enum Domain users with interesting description
- Enum Domain users with not the default encryption
- Enum Domain users with Protecting Privileged Domain Accounts

### `Kerberos`
- AS-REP Roastable
- Kerberoastable
- Password cracking with john  (krb5tgs and krb5asrep)

## `Microsoft Advanced Threat Analytics`
#### `ATA detects two suspicious events but does` **not** `trigger an` **alert** `:`
- The connection with the protocol LDAP without SSL
- The Kerberoastable attack

#### `As shown in this screenshot:`
![ATAdetection.png](ATAdetection.png)

## `Source`
### `Documentation:`
- [F-Secure](https://labs.f-secure.com/blog/attack-detection-fundamentals-discovery-and-lateral-movement-lab-1/)
- [The ITBros](https://theitbros.com/ldap-query-examples-active-directory/)
- [Microsoft](https://docs.microsoft.com/en-us/advanced-threat-analytics/what-is-ata/)

### `Impacket:`
- [Impacket GetNPUsers.py](https://github.com/SecureAuthCorp/impacket/blob/master/examples/GetNPUsers.py)
- [Impacket GetUserSPNs.py](https://github.com/SecureAuthCorp/impacket/blob/master/examples/GetUserSPNs.py)

## `Legal Disclaimer`
#### ```This project is made for educational and ethical testing purposes only. Usage of this software for attacking targets without prior mutual consent is illegal. It is the end user's responsibility to obey all applicable local, state and federal laws. Developers assume no liability and are not responsible for any misuse or damage caused by this program.```

#### ``PLEASE CHECK`` *[LICENSE](LICENSE)*
#### ``DEVELOPERS:``*[Xcod3bughunt3r](https://github.com/Xcod3bughunt3r/Xcod3bughunt3r)*
