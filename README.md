Modded ContactsProvider.apk for CM10.1	
*Adds Facebook sync functions	
File came from stable build for Sprint Samsung Galaxy S3 (D2SPR)... try on your device at your own risk		
If your following the guide at the bottom to apply this yourself, view this as raw format to view entire content

Instructions:		

Using root explorer or android commander, delete original file and copy over mine.		
Clear data for contactsprovider and facebook and reboot.		
Using either ADB shell or terminal emulator execute this command:   
sqlite3 /data/data/com.android.providers.contacts/databases/contacts2.db 'ALTER TABLE raw_contacts ADD COLUMN is_restricted VARCHAR';		


Reboot again, sign back into facebook, and then enable sync functions and all should be good.		
If you also want calendar sync for facebook events; install haxsync and haxsync jb workaround.		

If you would like to apply this patch to your ContactProvider.apk follow these steps below: 
decompile the apk using either apktools, apkmultitools, or smali. navigate to "/ContactsProvider.apk/res/value/"    
in the folder used to decompile, and move the included "arrays.xml" file into that folder.      
Save the file. Recompile the apk. Then follow the other instructions above about the final steps.

