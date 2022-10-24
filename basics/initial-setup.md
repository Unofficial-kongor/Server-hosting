# Initial setups

In order to ensure the best performance for game servers, enable "high performance" power profile in windows. 

1. Control panel -> Battery -> Power potions. Set plan to "High performance"

This can also be done via the folowing powershell command:

`powercfg /setactive 8c5e7fda-e8bf-4a96-9a85-a6e23a8c635c`

you can verify this with

`powercfg /list`

![image](https://user-images.githubusercontent.com/110408668/197505339-ff555315-2de9-49d2-8004-332248ae6384.png)



After the above step is done, now its time for the game server setup. Extract the downloaded "clean HON" to your preferred location. such as  `C:\Heroes of Newerth`

1. Unpack _wasserver binaries_ like so
   
   1. `hon_x64.exe` `k2_x64.dll` `proxy.exe` `proxymanager.exe` into `C:\Heroes of Newerth`
   2. `cgame_x64.dll` `game_shared_x64.dll` `game_x64.dll` into `C:\Heroes of Newerth\game`

2. Extract  *compel*  into your hon folder.  Start by editing `compel.json` with your preferred text editor and fill out the `Values` for each setting. 
   
   1. The most important values to change is
   
   2. `Username` (Same username as you hon login)
   
   3. `Password` (Same password as you hon login)
   
   4. `Instances` (How many servers you want to run, before you go CRAZY its highly recommended that you "test" with 1 instance)
   
   5. `Location` (Besides the regular locations, you should start with "NEWERTH" to exclude your server from TMM. You "must" do this for testing purposes before you go ham)
   
   6. `ServerNamePrefix` (The server name ID. This will be shown when typing `/gi` and selecting in public servers)
   
   7. `UseProxy` should be set to `true` its a type of anti-cheat and and more.
      
      *highly recommended*
