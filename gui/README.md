git clone -b beta https://github.com/Nimdy/Dedicated_Valheim_Server_Script.git

after install use option 1337 (it will show up after Valheim installation is detected)

Launch in the web browser

ENjoy....

Future pulls for GUI will come from a seperate repo but until we have it all ironed out... it will be combined. 

TO-DO!

Work server functions
--outline completed - working 100% with correct sudoers entry - might be a better way

Work player controls edit for ban,admin,block 
-outline completed - kinda working

Work Valheim+ information (if using)

Work Bepindex install, remove, display mods (if using)
-outline completed - not working 100%

Work display logs
-outline complete - Working only with www-data being added to adm group.  adm group has permissions to read all logs. 
-- has to be a way to have sudoers file execute better without exposing the server to exploits
-- maybe edit start_valheim.sh and dump valheim logs to /home/steam/valheimserver/worldName/logs 

Work map generation for seed
-outline complete - 100% working

Work notification area
-outline complete - 100% working... maybe add different news related sections?



# Is this be best way to secure it?? NO its a huge security punching bag... but we need to do something
# Valheim www-data entry for sudoers


Make sure php functions are secured to the best it can be.  Review GTFOBINS for common shell hacks and test.

escapeshellcmd(string $command): string

exec(escapeshellcmd("ping -c 4 " . escapeshellarg($_GET['host'])), $output);

Open to anything else and @Peabo gets 100% for getting us started! Thanks Peabo!!!!!
