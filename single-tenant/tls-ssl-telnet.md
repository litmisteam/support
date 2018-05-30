# TLS/SSL Telnet

Follow these instructions to configure your 5250 sessions and other applications using TLS/SSL Encryption.

Start by pasting the following URL into your browser:

`http://<IBM i Public Internet IP Address>:2001/QIBM/ICSS/Cert/Admin/qycucm1.ndm/main0`

When prompted, enter your IBM i user name and password:  
![](../.gitbook/assets/tls-01.png)Click on Create a Certificate Authority \(CA\):

![](../.gitbook/assets/tls-02.png)

Changing the validity period to 7300 days is recommended as is using SHA-256 as the hash algorithm. Then fill out all required fields, and click Continue.:

![](../.gitbook/assets/tls-03.png)

Click Continue:

![](../.gitbook/assets/tls-04.png)

Selecting Yes to allow creation of user certificates is recommended as is changing the validity period to 2000 days. Then click Continue:

![](../.gitbook/assets/tls-07.png)

You should receive confirmation that the CA policy data was successfully changed. Click Continue:

![](../.gitbook/assets/tls-08.png)

Fill out all required fields and click Continue:

![](../.gitbook/assets/tls-09.png)

You should see a message indicating the your certificate was created successfully. Select the desired applications or use the recommended selections below, then click Continue:

![](../.gitbook/assets/tls-09-2.png)

You should receive a message indicating the applications selected will use your new certificate. Then click Continue:

![](../.gitbook/assets/tls-10.png)

Since an object signing certificate is not needed, click Select a Certificate Store:

![](../.gitbook/assets/tls-11.png)

Select \*SYSTEM and then click Continue:

![](../.gitbook/assets/tls-13.png)

Type the password and click Continue:

![](../.gitbook/assets/tls-14.png)

Click the Fast Path link to the left of the screen:

![](../.gitbook/assets/tls-15.png)

Click the Work with server applications link:

![](../.gitbook/assets/tls-16.png)

![](../.gitbook/assets/tls-17.png)

![](../.gitbook/assets/tls-18.png)

![](../.gitbook/assets/tls-19.png)

![](../.gitbook/assets/tls-20.png)

![](../.gitbook/assets/tls-21.png)

![](../.gitbook/assets/tls-22.png)

![](../.gitbook/assets/tls-23.png)

![](../.gitbook/assets/tls-24.png)

![](../.gitbook/assets/tls-27.png)

![](../.gitbook/assets/tls-25.png)

![](../.gitbook/assets/tls-26.png)

![](../.gitbook/assets/tls-28.png)

![](../.gitbook/assets/tls-29.png)

![](../.gitbook/assets/tls-30.png)

![](../.gitbook/assets/tls-31.png)

![](../.gitbook/assets/tls-32.png)

