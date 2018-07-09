---
description: >-
  This page will show you how to install the Yum package manger which can be
  used to install many different software packages like bash, Node.js, Nginx,
  GNU compilers, etc.
---

# Open Source Installation

First, [download ACS \(Access Client Solutions\)](http://www-01.ibm.com/support/docview.wss?uid=isg3T1026805) and install it on your laptop.  `Select Tools->Open Source Package Management`, as shown below.

![](../.gitbook/assets/oss1.png)

Select your system from the drop-down \(you'll need to configure it first if you haven't already done so\).  Best to use a QSECOFR profile.  

![](../.gitbook/assets/oss2%20%281%29.png)

Accept the RSA key.

![](../.gitbook/assets/oss3.png)

Select `Yes`

![](../.gitbook/assets/oss4.png)

Wait while it installs.

![](../.gitbook/assets/oss5.png)

Wait some more.  You should see a window similar to the below.

![](../.gitbook/assets/oss6.png)

Installation is complete!

![](../.gitbook/assets/oss7.png)



You can kick the tires by first starting the SSH server on IBM i using the following command from a 5250 telnet session.

`STRTCPSVR *SSHD`

Run the following to set the default shell to Bash.  Use STRSQL or the Run SQL Scripts feature in ACS.

```text
CALL QSYS2.SET_PASE_SHELL_INFO('*DEFAULT', '/QOpenSys/pkgs/bin/bash')
```

Next, download a shell client, like [putty](https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html).

Enter your profile \(doesn't need to be QSECOFR\) an @ sign, and the IP of your machine and select **Open**, as shown below.

![](../.gitbook/assets/oss8.png)

Accept the server by selecting **Yes**, as shown below.

![](../.gitbook/assets/oss9.png)

You will be prompted for your password.  The open source software isn't in your `PATH` environment variable by default so you'll need to add it, as shown below.

![](../.gitbook/assets/oss10.png)

At this point the base Yum package manager and supporting software \(i.e. bash, python\) is installed.  You can now run `yum` commands to install additional software.  Some examples are below.

```text
yum install nodejs8

yum install '*gcc*'
```

