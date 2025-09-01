Phishing Alert 1 :

![A screenshot of a computer error AI-generated content may be
incorrect.](images/media/image1.png){width="6.5in" height="2.9in"}

We have all the information mentioned in the this screenshot in our
investigation channel .

Source - 172.16.17.49 -- lets defend employee

Destination address - 91.189.114.8 -- Internet

User Agent -\
Mozilla/5.0 (Windows NT 6.1; Win64; x64) AppleWebKit/537.36 (KHTML, like
Gecko) Chrome/79.0.3945.88 Safari/537.36

Log Management :

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image2.png){width="6.5in"
height="2.479861111111111in"}

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image3.png){width="6.5in"
height="2.5256944444444445in"}

In the log management console we find 2 logs belonging to the
destination IP address . One a firewall log , the other one a proxy both
belonging to the same URL .

Url analysis :

As this is not a typical email phishing analysis header we just have to
analyze the Url through third party platforms like Virustotal , anyrun ,
Url scanner . Lets do that .

Url -
<http://mogagrocol.ru/wp-content/plugins/akismet/fv/index.php?email=ellie@letsdefend.io>

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image4.png){width="6.5in" height="3.19375in"}

10 out 97 vendors flag this is as a malicious url but blindly believing
on this is naivity . So lets further analyze in different platforms .

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image5.png){width="6.5in"
height="3.1333333333333333in"}

Now this where we can flag this url suspicious as its main Ip is located
in Russian federation and its contacting 6 IPS in 2 countries . Lets
further analyze the Url

This domain appears suspicious because it claims to be part of the
Akismet WordPress plugin (/wp-content/plugins/akismet/), but it's hosted
on a random .ru domain with no connection to the actual Akismet service.
The URL calls a PHP script (index.php) and passes an email parameter,
which is unusual for a legitimate plugin path. In a normal case, Akismet
would process emails only on trusted WordPress sites, not through an
external Russian domain.

Also it seems that anyrun says this Url would download a suspicious
payload to execute .

With all this information I concluded that this is a phishing Url .

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image6.png){width="6.5in"
height="3.5555555555555554in"}

Next part is

![A screenshot of a computer screen AI-generated content may be
incorrect.](images/media/image7.png){width="6.5in"
height="4.0368055555555555in"}

Clearly, we can see the url was accessed by Emily and I've already
listed out the other things . One important factor here is that the
request is not blocked but was allowed . So the url is accessed and we
need to contain the end point .

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image8.png){width="6.5in"
height="2.5722222222222224in"}

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image9.png){width="6.5in"
height="3.1444444444444444in"}

Lets check if the analysis is right or wrong .

![A screenshot of a computer AI-generated content may be
incorrect.](images/media/image10.png){width="6.5in"
height="2.702777777777778in"}

So the analysis is right .
