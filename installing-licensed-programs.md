# Installing Licensed Programs
Your Litmis Space should be loaded with most software.  If you need additional software you can easily load it yourself from the image catalog we've configured.  [Click here](https://www.ibm.com/support/knowledgecenter/en/ssw_ibm_i_72/rzahc/rzaskMediaContent.htm) to learn what is on each IBM i "CD".

The following shows how to install WDS option 60 which is required to do RDi debugging.

Run command `WRKDEVD OPT*` to make sure `OPTVRT01` exists.  Take option 8.

```
                        Work with Device Descriptions                      
                                                            System:   LS0xx
Position to  . . . . .                Starting characters                  
                                                                           
Type options, press Enter.                                                 
  2=Change   3=Copy    4=Delete   5=Display   6=Print   7=Rename           
  8=Work with status   9=Retrieve source                                   
                                                                           
Opt  Device      Type        Text                                          
 8   OPTVRT01    632B                                                      
     OPT01       632C        CREATED BY AUTO-CONFIGURATION                 
```
If `OPTVRT01` is `VARIED OFF` then take option 1.
```
                        Work with Configuration Status                LS0xx
                                                        01/05/18  17:04:31 EST
Position to  . . . . .                Starting characters                     
                                                                              
Type options, press Enter.                                                    
  1=Vary on   2=Vary off   5=Work with job   8=Work with description          
  9=Display mode status    13=Work with APPN status...                        
                                                                              
Opt  Description       Status                -------------Job--------------   
1    OPTVRT01          VARIED OFF                                             
```

Run command `WRKIMGCLG` to make sure `V7R3M0` exists.  Take option 12.

```
                           Work with Image Catalogs                        
                                                            System:   LS0xx
Type options, press Enter.                                                 
  1=Create   2=Change   4=Delete   8=Load   9=Unload   10=Verify           
  12=Work with entries                                                     
                                                                           
     Image                               ASP                 Device        
Opt  Catalog     Status      Type     Threshold  Device      Status        
                                                                           
12   V7R3M0      Not ready   Optical    *CALC                              
     V7R3PTFS    Not ready   Optical    *CALC                              
```

In this scenario we're installing WDS option 60, which exists in `B_GROUP1_05`.  Take option 6.  [Click here](https://www.ibm.com/support/knowledgecenter/en/ssw_ibm_i_72/rzahc/rzaskMediaContent.htm) to learn what is on each IBM i image catalog.
```
                       Work with Image Catalog Entries                     
                                                            System:   LS0xx
Catalog  . . :   V7R3M0                  Status . . . :   Not ready        
Type . . . . :   Optical                 Device . . . :                    
                                                                           
Directory  . . . . :   /V7R3M0                                             
                                                                           
Type options, press Enter.                                                 
  1=Add   2=Change       4=Remove   6=Mount   8=Load   9=Unload            
  10=Initialize volume   12=Work with volume                               
                                                                           
Opt   Index  Status      Image File Name                                   
     *AVAIL                                                                
          1  Mounted     I_BASE_01                                         
          2  Loaded      B_GROUP1_01                                       
          3  Loaded      B_GROUP1_02                                       
          4  Loaded      B_GROUP1_03                                       
          5  Loaded      B_GROUP1_04                                       
6         6  Loaded      B_GROUP1_05                                       
```
Return to the previous screen and take option 8 to load this image catalog.
```
                           Work with Image Catalogs                        
                                                            System:   LS0xx
Type options, press Enter.                                                 
  1=Create   2=Change   4=Delete   8=Load   9=Unload   10=Verify           
  12=Work with entries                                                     
                                                                           
     Image                               ASP                 Device        
Opt  Catalog     Status      Type     Threshold  Device      Status        
                                                                           
8    V7R3M0      Not ready   Optical    *CALC                              
     V7R3PTFS    Not ready   Optical    *CALC                              
```
On the next screen specify `OPTVRT01` for the virtual device and hit Enter.  This device should already exist.
```
                   Load or Unload Image Catalog (LODIMGCLG)       
                                                                  
Type choices, press Enter.                                        
                                                                  
Image catalog  . . . . . . . . . > V7R3M0        Name             
Option . . . . . . . . . . . . . > *LOAD         *LOAD, *UNLOAD   
Virtual device . . . . . . . . .   OPTVRT01      Name             
Write protect  . . . . . . . . .   *DFT          *DFT, *ALL, *NONE
Library mode . . . . . . . . . .   *NO           *NO, *YES        
```
At this point the image catalog has been loaded as if it was a DVD. 

Proceed to install the licensed program by running command `GO LICPGM`. Take option 11.

```
LICPGM                   Work with Licensed Programs                       
                                                            System:   LS0xx
Select one of the following:                                               
                                                                           
  Manual Install                                                           
     1. Install all                                                        
                                                                           
  Preparation                                                              
     5. Prepare for install                                                
                                                                           
  Licensed Programs                                                        
    10. Display installed licensed programs                                
    11. Install licensed programs                                          
    12. Delete licensed programs                                           
    13. Save licensed programs                                             
```
Scroll down until you see the product and option you wish to install and enter `1` next to it.
```
                          Install Licensed Programs                        
                                                            System:   LS0xx
Type options, press Enter.                                                 
  1=Install                                                                
                                                                           
        Licensed  Product                                                  
Option  Program   Option   Description                                     
                                                                           
        5770WDS    45      ILE COBOL *PRV Compiler                         
        5770WDS    51      ILE C                                           
        5770WDS    52      ILE C++                                         
        5770WDS    56      IXLC for C/C++                                  
  1     5770WDS    60      Workstation Tools - Base                        
        5770XE1    *BASE   IBM i Access for Windows                        
        5770XH2    *BASE   IBM i Access for Web                            
        5770XW1    *BASE   IBM i Access Family                             
        5770XW1    1       IBM i Access Enablement Support                 
```
Press Enter to confirm.
```
                     Confirm Install of Licensed Programs                  
                                                            System:   LS0xx
Press Enter to confirm your choices for 1=Install.                         
Press F12 to return to change your choices.                                
                                                                           
Licensed  Product                                                          
Program   Option   Description                                             
5770WDS    60      Workstation Tools - Base                                
```
Specify the options as shown below and hit enter.
```
                               Install Options                               
                                                            System:   LS0xx 
Type choices, press Enter.                                                   
                                                                             
  Installation device  . . .   OPTVRT01     Name                             
                                                                             
  Objects to install . . . .   1            1=Programs and language objects  
                                            2=Programs                       
                                            3=Language objects               
                                                                             
  Nonaccepted agreement  . .   2            1=Do not install licensed program
                                            2=Display software agreement     
                                                                             
  Automatic IPL  . . . . . .   N            Y=Yes                            
                                            N=No                             
```
You will then see the installation commence.
```
                       Installing Licensed Programs                         
                                                             System:   LS0xx
                                                                            
                                                                            
 Licensed programs processed . . . . . . . . . . :        0 of 1            
                                                                            
                                                                            
                                                                            
                 Licensed program install in progress                       
```
Upon completion you should see this in your joblog.
```
3>> go licpgm                                                           
    Security changes occurred for 1 objects.                            
    Security changes occurred for 1 objects.                            
    *PGM objects for product 5770WDS option 60 release V7R3M0 restored. 
    Work with licensed programs function has completed.                 
```                                                               

Contact team@litmis.com with additional questions!