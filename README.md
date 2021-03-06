## OPNsense starterkit

You want to either quickly 

1. Try [OPNsense](https://opnsense.org). See below 'Trying OPNsense'.
2. Or build an image for your infrastructure right from the ISO / from scratch. See [the build guide](build/README.md).
3. Or start developing opnsense with one line, see [the development quicksetup guide](development/README.md)
4. Test the current most resent OPNsense development version without any effort? Check [the development quicksetup guide](development/README.md) - you get a "from source" version after running 1 command.

## Trying OPNsense

 - Install vagrant https://www.vagrantup.com/downloads.html
 
 ```
mkdir /tmp/mytest && cd /tmp/mytest
curl -o Vagrantfile https://raw.githubusercontent.com/naturalis/opnsense-starterkit/master/Vagrantfile
vagrant up firewall
```

Now you can either access OPNsense using `https://localhost:10443` or by `ssh -p 10022 root@localhost`

Username: root
Password: opnsense

To see which versions are available, check https://app.vagrantup.com/rudibroekhuizen/boxes/opnsense
