# TLS/SSL Telnet Setup

Follow these instructions to configure your 5250 sessions and other applications using TLS/SSL Encryption.

Start by pasting the following URL into your browser:

`http://<IBM i Public Internet IP Address>:2001/QIBM/ICSS/Cert/Admin/qycucm1.ndm/main0`

When prompted, enter your IBM i user name and password:  
![](/assets/TLS/TLS-01.png)Click on Create a Certificate Authority \(CA\):

![](/assets/TLS/TLS-02.png)

Changing the validity period to 7300 days is recommended as is using SHA-256 as the hash algorithm.  Then fill out all required fields, and click Continue.:

![](/assets/TLS/TLS-03.png)

Click Continue:

![](/assets/TLS/TLS-04.png)

Selecting Yes to allow creation of user certificates is recommended as is changing the validity period to 2000 days.  Then click Continue:

![](/assets/TLS/TLS-07.png)

You should receive confirmation that the CA policy data was successfully changed.  Click Continue:

![](/assets/TLS/TLS-08.png)

Fill out all required fields and click Continue:

![](/assets/TLS/TLS-09.png)

You should see a message indicating the your certificate was created successfully.  Select the desired applications or use the recommended selections below,  then click Continue:

![](/assets/TLS/TLS-09-2.png)

You should receive a message indicating the applications selected will use your new certificate.  Then click Continue:

![](/assets/TLS/TLS-10.png)

Since an object signing certificate is not needed, click Select a Certificate Store:

![](/assets/TLS/TLS-11.png)

Select \*SYSTEM and then click Continue:

![](/assets/TLS/TLS-13.png)

Type the password and click Continue:

![](/assets/TLS/TLS-14.png)

Click the Fast Path link to the left of the screen:

![](/assets/TLS/TLS-15.png)

Click the Work with server applications link:

![](/assets/TLS/TLS-16.png)



![](/assets/TLS/TLS-17.png)

![](/assets/TLS/TLS-18.png)

![](/assets/TLS/TLS-19.png)

![](/assets/TLS/TLS-20.png)

![](/assets/TLS/TLS-21.png)

![](/assets/TLS/TLS-22.png)

![](/assets/TLS/TLS-23.png)

![](/assets/TLS/TLS-24.png)

![](/assets/TLS/TLS-27.png)

![](/assets/TLS/TLS-25.png)

![](/assets/TLS/TLS-26.png)

![](/assets/TLS/TLS-28.png)

![](/assets/TLS/TLS-29.png)

![](/assets/TLS/TLS-30.png)

![](/assets/TLS/TLS-31.png)

![](/assets/TLS/TLS-32.png)

