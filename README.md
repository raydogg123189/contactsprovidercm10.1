Modded ContactsProvider.apk for CM10.1  
*Adds Facebook sync functions   
file came from stable build for Sprint Samsung Galaxy S3 (D2SPR)... try on your device at your own risk

Instructions:   
Using root explorer or android commander;   
delete original file and copy over mine;    
clear data for contactsprover and facebook and reboot
using either ADB shell or terminal emulator execute this command:   
sqlite3 /data/data/com.android.providers.contacts/databases/contacts2.db 'ALTER TABLE raw_contacts ADD COLUMN is_restricted VARCHAR';       

    
reboot again and then sign back into facebook and enable sync functions and all should be good    
if you also want calendar sync for facebook events; install haxsync and haxsync jb workaround
