# Navigator for i

The [_IBM Navigator for i_](https://www.ibm.com/support/knowledgecenter/ssw_ibm_i_73/rzat10/rzatgdirectoroverview.htm) is a browser-based administration tool for your IBM i instance. Here you will find information on things mostly related to troubleshooting.

## Setup Checklist

There are a few things you should be aware of as it relates to Navigator for i running successfully. See below for things that you might want to add.

### DNS

Add a host table entry for `LS999.domain.com`. The name needs to resolvable from a public domain DNS server or the local host table. In this case we're going to resolve it locally because a domain isn't yet associated with a new Litmis Space Single Tenant server.

First issue the `CFGTCP` command and take option 10. You should see something similar to the following. Do an option `1` to add a new entry.

```text
                      Work with TCP/IP Host Table Entries                   
                                                             System:   LS999
 Type options, press Enter.                                                 
   1=Add   2=Change   4=Remove   5=Display   7=Rename                       

      Internet                          Host                                
 Opt  Address                           Name                                

      ::1                               IPV6-LOOPBACK
                                        IPV6-LOCALHOST
      127.0.0.1                         LOOPBACK
                                        LOCALHOST
```

Enter the information as shown below and replace `192.168.0.2` and `LS999` with the information we provided via email.

```text
                  Change TCP/IP Host Table Entry (CHGTCPHTE)

Type choices, press Enter.                                  

Internet address . . . . . . . . > '192.168.0.2'            
Host names:
  Name . . . . . . . . . . . . .   'LS999.DOMAINE.COM'

  Name . . . . . . . . . . . . .   'LS999'
```

Returning back to the previous screen will show the new entry.

```text
                      Work with TCP/IP Host Table Entries                   
                                                             System:   LS999
 Type options, press Enter.                                                 
   1=Add   2=Change   4=Remove   5=Display   7=Rename                       

      Internet                          Host                                
 Opt  Address                           Name                                

      ::1                               IPV6-LOOPBACK
                                        IPV6-LOCALHOST
      127.0.0.1                         LOOPBACK
                                        LOCALHOST
      192.168.0.2                       LS999.DOMAIN.COM
                                        LS999
```

Now return to the `CFGTCP` menu and take option 12 and enter the following information.

```text
                       Change TCP/IP Domain (CHGTCPDMN)

Type choices, press Enter.                             

Host name  . . . . . . . . . . .   'LS999'

Domain name  . . . . . . . . . .   'DOMAIN.COM'
```

