# Port forwarding

The server sends and receives packages ("game", "voice", "ping" and "stats resubmission"). So in order for the server to be accepted by PROJECT kongor, you must forward these ports on your computer and on your router.

**With UseProxy set to `true` in COMPEL.json**

* *Game:* `21235-21335` _(UDP)_
* *Voice:* `21435-21535` _(UDP)_
* *Ping* `21234` _(TCP)_
* *Stats resub* `1180` _(TCP)_

**With UseProxy set to `false` in COMPEL.json** _(Not recomended)_

* *Game:* `11235-11335` _(UDP)_
* *Voice:* `11435-11535` _(UDP)_
* *Ping* `11234` _(UDP)_
* *Stats resub* `1180` _(TCP)_

*PS: The port range may be set to the amount of server instances you wish to run*


The new region auto-select feature is based on ping responses, however the masterserver pings COMPEL, not any of the other processes, which then pongs back. The port on which this happens is either 11234 (plus offset from config) if you don't use the proxy or 21234 (plus offset from config) if you do use the proxy, and the reasoning for using these ports is that you can just extend your already existing range of forwarded ports to add one more port at the lower end. if using the above range, everything should be set.

### Router guides

#### PfSense

1. Goto `Firewall -> Alias -> Ports`
2. add
3. Enter *Game* and *Voice* ranges in format `xxxx:yyyy` and new entries for stats *Stats resub* and *Ping*
4. give it a name like `hon_ports`
5. save
6. go to `Firewall -> Nat -> Add`
7. in _Destination port range_ "From port and To port" via "custom" to `hon_ports` 
8. in _Redirect target IP_ enter your servers IP
9. in _Redirect target port_ enter `hon_ports`
10. SAVE

#### Asus Router

1. Go to `WAN` under `Advanced Settings`
2. Go to tab `Virtual Server / Port Forwarding`
3. Activate `Enable Port Forwarding`
4. Click `Add profile` and specify the required ports and internal server ip
