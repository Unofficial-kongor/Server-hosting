# Port forwarding

The server sends and receives packages via the UDP protocol on 2 ranges ("game" and "voice"). So in order for people to be able to connect to your server, you must forward these ports on your computer and on your router.

**With UseProxy set to `true` in COMPEL.json**

* *Game:* `21235-21335`
* *Voice:* `21435-21535`

**With UseProxy set to `false` in COMPEL.json** _(Not recomended)_

* *Game:* `11235-11335`
* *Voice:* `11435-11535`

*PS: The port range may be set to the amount of server instances you wish to run*


### Router guides

#### PfSense
1. Goto `Firewall -> Alias -> Ports`
2. add
3. Enter botrh ranges in format `xxxx:yyyy` and give it a name like `hon_ports`
4. save
5. `Firewall -> Nat -> Add`
6. in _Destination port range_ "From port and To port" via "custom" to `hon_ports` 
7. in _Redirect target IP_ enter your servers IP
8. in _Redirect target port_ enter `hon_ports`
9. SAVE
