# FAQ for Litmis Spaces Single Tenant

This page will serve to answer the questions we get most often. Don't see your question? Contact us at [team@litmis.com](mailto:team@litmis.com).

**Q: Do I install my own PTFs?**

A: Yes. We will show you how to do this at no additional cost.



**Q: How many users are licensed on the machine?**

A: You have unlimited IBM i profiles.

**Q: Do we have the ability to IPL the single tenant system on demand?**

A: Yes, you can IPL to your heart's content.  Note that only our staff has access to the HMC, so will be a bit of a blind IPL - you won't be able to see the current progress.  Make sure to specify `RESTART(*YES)` on the `PWRDWNSYS` command.

**Q: What processor group does Litmis Spaces have?**

A: P20

**Q: Do you also offer Windows and Linux hosting?**

A: Yes, please contact [team@litmis.com](mailto:team@litmis.com) to learn more.

**Q: Can I install a secondary language?**

A: Yes.  Each machine has a folder named /v7r3xxxx in the root of the IFS that contains the DVD images for the operating system components.  This allows you to install a number of things including secondary languages.

[Here](https://www.ibm.com/support/knowledgecenter/en/ssw_ibm_i_73/rzahc/seclmnu.htm) are the instructions for installing a secondary language for v7.3.  When prompted for the Installation Device you will specify `OPTVRT01`, which is the default optical device we've setup.

**Q: Can you restore my system save onto my Litmis Space server?**

A: Yes. You can mail us your system save and we can restore it at no cost.