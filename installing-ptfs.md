# Installing PTFs
First locate the PTF you need and enter the `SNDPTFORD` command, as shown below.  Hit the `Enter` key to continue.
```
SNDPTFORD PTFID((SF99223))
```

The next screen will prompt you to verify contact info.  **Don't change any values.**  `Enter` key to continue.
```
                          Verify Contact Information                        
                                                            System:   LS999
Type changes, press Enter.                                                  
                                                                            
  Company . . . . . . . . . .   <<Don't change>>
  Contact . . . . . . . . . .   <<Don't change>>
  ```
  On the next page select option `1` and hit `Enter`.
  ```
                             Select Reporting Option                          
                                                            System:   LS999
Problem ID . . . . . . . . . :   9999999999                                 
Current status . . . . . . . :   READY                                      
Problem  . . . . . . . . . . :   Fix request                                
                                                                            
                                                                            
Select one of the following:                                                
                                                                            
     1. Send service request now                                            
     2. Do not send service request                                         
     3. Report service request by voice                                     
                                                                            
                                                                            
                                                                            
Selection                                                                   
     1                                                                      
                                                                            
F3=Exit   F12=Cancel                                                        
Alternate load device not found.                                            
```

You should now see various diagnostic messages displaying in the bottom of your screen and eventually it will convey the percentage left to download.

Once the download is complete run the `GO PTF` command and you see see the following screen.
```
PTF                         Program Temporary Fix                           
                                                            System:   LS999
Select one of the following:                                                
                                                                            
     1. Load a program temporary fix                                        
     2. Apply a program temporary fix                                       
     3. Copy a program temporary fix                                        
     4. Remove a program temporary fix                                      
     5. Display a program temporary fix                                     
     6. Order a program temporary fix                                       
     7. Install a program temporary fix from a list                         
     8. Install program temporary fix package                               
     9. Copy PTF Cover Letter                                               
    10. Display PTF Cover Letter                                            
    11. Delete a program temporary fix                                      
    12. Work with PTF groups                                                
    13. Copy PTF group                                                      
```
Select option `8`, `Install program temporary fix package`.  You should be presented with the following screen.  Enter `*SERVICE` to declare we want to install the PTFs we from IBM's service. Set `Automatic IPL` to `N`; you can restart later if necessary.  Set `Other options` to `Y` because we want to be prompted for one more screen.  Hit the `Enter` key.
```
                 Install Options for Program Temporary Fixes                  
                                                            System:   LS999  
Type choices, press Enter.                                                    
                                                                              
  Device  . . . . . . . . .   *SERVICE     Name, *SERVICE, *NONE              
                                                                              
  Automatic IPL . . . . . .   N            Y=Yes                              
                                           N=No                               
                                                                              
  Prompt for media  . . . .   1            1=Single PTF volume set            
                                           2=Multiple PTF volume sets         
                                           3=Multiple volume sets and *SERVICE
                                                                              
  Restart type  . . . . . .   *SYS         *SYS, *FULL                        
                                                                              
  Other options . . . . . .   Y            Y=Yes                              
                                           N=No                               
```
On the `Other Install Options` screen set the `Apply type` to `2` so PTFs can be applied immediately without an IPL.  Note this is specific to the `5733OPS` PTFs.  Not all PTFs can be applied and be working in this fashion.  Hit the `Enter` key.
```
                            Other Install Options                           
                                                            System:   LS999
Type choices, press Enter.                                                  
                                                                            
  Omit PTFs  . .   N            Y=Yes, N=No                                 
                                                                            
  Apply type . .   2            1=Set all PTFs delayed                      
                                2=Apply immediate, set delayed PTFs         
                                3=Apply only immediate PTFs                 
```
The PTF installation process will now start and you should see a screen similar to the following.
```
                              PTF Load in Progress                              
                                                             System:   LS999
 Product                                                                        
 ID          Description                                                        
 5770SS1     IBM i                                                              
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                         Bottom 
 Loading PTFs for 2 of 23 licensed programs.                                    
```

Once it is complete you should have the updates installed.