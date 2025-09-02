Phishing challenge :

We have a PayPal .eml Thunderbird file. Firstly, we will try to analyze
the SPF, DKIM, and DMARC Details of the email to check if everything's
in place.

I can see SPF enabled, but there are no signs of DKIM or DMARC. This is
not strange .

The SMTP seems to be fine as it is from the Google MX server aswell.

Email header analysis.

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image1.png)

![A screenshot of a computer code AI-generated content may be
incorrect.](images/media/image2.png)

![A computer screen shot of a computer code AI-generated content may be
incorrect.](images/media/image3.png)

The first thing that is a bit suspicious is the return path and from
address . Although its common to have we will run through it WHOIS. I
see no connection between the return path -
<bounce@rjttznyzjjzydnillquh.designclub.uk.com>

And the from address - P.A.Y.P.A.L? . \<IHKH0MFEWW@kodehexa.net .
Clearly a mismatch and case of redirection .

To prove that its actually a redirection

We need to further Analyze the Url attached with this email .

<https://storage.googleapis.com/hqyoqzatqthj/aemmfcylvxeo.html#QORHNZC44FT4.QORHNZC44FT4>.
This is already gibberish and suspicious but we go through the regular
process .

Can clearly see in Virus total that this is a case of phishing .

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image4.png)

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image5.png)

Here you go , this proves that it is a malicious phishing email .

Questions :

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image6.png)

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image7.png)
