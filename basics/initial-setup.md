# Initial setup

These steps assumes you have created `C:\H O N` _(Including spaces)_ you may however use whatever directory you like, but its required to have at least one space because of [this bug](#no-link-yet)

1. Control panel -> Battery -> Power potions. Set plan to "High performance"
2. Extract the clean HON into `C:\H O N` or something. Its important to have spaces in the path name, otherwise you will get an error later.
3. Unpack _wasserver binaries_ like so
   1. `hon_x64.exe` `k2_x64.dll` `proxy.exe` `proxymanager.exe` into `C:\H O N`
   2. `cgame_x64.dll` `game_shared_x64.dll` `game_x64.dll` into `C:\H O N\game`
4. edit `COMPEL.json` and fill out the `Value` for each setting. 
   1. The most important values to change is
   2.  `Username` (Same username as you login with)
   3. `Password` (Same password as you login with)
   4.  `Instances` (How many servers you want to run, before you go CRAZY its highly recommended that you "test" with 1 instance)
   5. `Location` (Besides the regular locations, you should start with "NEWERTH" to exclude your server from TMM. You "must" do this for testing purposes before you go ham)
   6. `ServerNamePrefix` (The server name ID. This will be shown when typing `/gi` and selecting in public servers)
   7. `UseProxy` should be set to `true` its a type of anti-cheat and and more.
