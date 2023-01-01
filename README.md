# ShopifyTakeover
ShopifyTakeover is scanner tool to mass checking if target is vulnerable to [Shopify Subdomain Takeover](https://exploit.linuxsec.org/shopify-custom-domain-subdomain-takeover/).

## Background
Shopify is a popular e-commerce platform that allows users to create and manage online stores. It is possible for a Shopify subdomain to be taken over in the same way as any other subdomain. If an attacker is able to gain control of a Shopify subdomain, they may be able to redirect customers to a malicious website or steal sensitive information, such as login credentials or payment information. It is important for organizations using Shopify to regularly monitor their subdomains and ensure that they are properly configured to prevent subdomain takeovers.

## Requirements
- requests
- urllib3
- argparse
- beautifulsoup4

Tested on **Debian** with **Python 3.10.8**

## How to use
Help menu.
```
nino@nakano:~$ python3 ShopifyTakeover.py --help
usage: ShopifyTakeover.py [-h] [-l list.txt] [-t [5]] [--vuln]

options:
  -h, --help            show this help message and exit
  -l list.txt, --list list.txt
                        File contain lists of domain
  -t [5], --thread [5]  Thread value. Default value is 5
  --vuln                Print only vuln domain
  ```
Check lists.
```
python3 ShopifyTakeover.py -l shop.txt -t 40
```
Print vuln only.
```
python3 ShopifyTakeover.py -l shop.txt -t 40 --vuln
```
## Screenshot
![ShopifyTakeover](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEj2yfEMjGZS8pTuC6zN-bG8RpjBfM9V0BPARz9vF6gWxvJlkylQPhSFtl-4eeZGy9TuK0zrQlHh98w92HOxRsa1atSKc9-aQqdhmTJ5_KVqHmBQww7RNpgnwQP3arqjy-Cdr-P-GGhd5v1P_kdkXbruMnGqOAESuTieXafxJScWqMJGOvR7X8SBcGIrtg/s759/shopifytakeover.png "ShopifyTakeover")

## Disclaimer
Any actions and or activities related to the material contained within this tool is solely your responsibility.The misuse of the information in this tool can result in criminal charges brought against the persons in question.

**Note**: modifications, changes, or changes to this code can be accepted, however, every public release that uses this code must be approved by author of this tool (**yuyudhn**).