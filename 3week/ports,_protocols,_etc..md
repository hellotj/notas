##Ports, Protocols, Etc.
##Telnet
##OpenSSL
##Curl
##TCP/IP

## // 4.21.14 // Lorin

<br />

HTTP - 80

FTP - 20 21

HTTPS - 443

// From Yahoo.com - Remote Address:216.115.100.102:443

Here's how to see an SSL page from Bank Of America

		openssl s_client -connect www.bankofamerica.com:443
		
	Then type this *exactly*
		GET / HTML/1.1

	Then 2 carriage returns


###Curl 

So when you use CURL, it does all this authentication nonsense for us!
from terminal 
		
		curl https://api.github.com
		
Go to github.com and go to account settings then applications. 

Generate new token. 

Symetric key - encrypt and decrypt. 

*Operate much faster than public/private keys

Put in terminal to get all your repos come across: 
	
	curl https://api.github.com/users/hellotj/repos?a_token=608b8d3a6563ed96b2ac23956680bd00f59ccda0
	
https://developer.github.com/guides/getting-started/