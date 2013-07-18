Modded ContactsProvider.apk for CM10.1  
*Adds Facebook sync functions   
file came from stable build for Sprint Samsung Galaxy S3 (D2SPR)... try on your device at your own risk 
if your following the guide at the bottom to apply this yourself, view this as raw format to view entire content

Instructions:   
Using root explorer or android commander;   
delete original file and copy over mine;    
clear data for contactsprover and facebook and reboot
using either ADB shell or terminal emulator execute this command:   
sqlite3 /data/data/com.android.providers.contacts/databases/contacts2.db 'ALTER TABLE raw_contacts ADD COLUMN is_restricted VARCHAR';       

    
reboot again and then sign back into facebook and enable sync functions and all should be good    
if you also want calendar sync for facebook events; install haxsync and haxsync jb workaround       


if you would like to apply this patch to your ContactProvider.apk follow these steps below: 
decompile the apk using either apktools, apkmultitools, or smali. navigate to "/ContactsProvider.apk/res/value/"    
in the folder used to decompile. create a new file in that folder called  "arrays.xml"

<?xml version="1.0" encoding="UTF-8"?>
<resources>
    <string-array name="unrestricted_packages">
        <item>com.facebook.katana</item>
    </string-array>
</resources>

