Phishing challenge -- 2 :

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image1.png)

So we've got the SMTP IP , Source address from this alert .

First before doing anything we can have a look at the source's mail
server in mxlook up

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image2.png)

Already suspicious as it is blacklisted .

Then we'll look at the spf lookup.

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image3.png)

Seems spf is enabled but DMARC is not enabled .

No DKIM :

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image4.png)

Meaning we can't verify the integrity of the email as the digital
signature might be forged .

Then we'll check whether the email is delivered or not

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image5.png)

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image5.png)

As we can see action is blocked .

Next we will try to analyze if there are any attachments or not So we
will go to the email security console

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image6.png)

We'll use the hash of the file and go to virus total and anyrun to see
anything malicious .

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image7.png)

As we can see virus total flagged it malicious but this shouldn't be the
basis .

We will go to anyrun and see if there's something we can catch up .

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image8.png)

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image9.png)

As we can see it's a pdf file flagged as malicious with phishing
detected . Also comprehending there is something launching automatically
.

We can conclude that the email is delivered to be phished but the
because the device blocked we can stop our analysis here ending the
playbook .

![A screenshot of a computer AI-generated content may be
incorrect.](images1/media/image10.png)
