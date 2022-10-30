# Hosting from a vm / vps server

Hosting from a vm / vps server is a possibility - however there are special things to consider when doing so. Normally alot of vm servers / vps server from different companies share their cpu resources among other customer in order to have as many customers on the same hardware. However this is dangerous when hosting HoN servers, the Hon servers are very sensitive to other applications running on the same cpu cores.

If you however still want to host via a vm / vps server, you **need to ensure** that the the cpu's assigned to your vm / vps server is **dedicated cores**,  meaning those cores are not shared with any other customers on the same server. If not doing so - your servers will generate (*longer server frames*) which is lag. If a server is too unstable, and gets reported as a bad server - It will be **banned** from TMM games by dev's.
