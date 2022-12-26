# ShopifyTakeover
ShopifyTakeover is mass scan tool to check if target is vulnerable to [Shopify Subdomain Takeover](https://exploit.linuxsec.org/shopify-custom-domain-subdomain-takeover/).

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
![ShopifyTakeover](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgif8q9LaPDXKDlqUaoUk9VbAHnKKL9-N9AGJFwG-rOkUIeYR5MJL5IiBmtud9EW7RU-dqd1GxveRzZ1F9l-I2GBH8L3fd6YT9Ai0MH3JPZ96bTj1nsvPEWfbVB_4723svfNigk9eLCzT3EkSmbl0-7uRWwBMr205CANQ0ozjeCYZ2zexhv0BuVRPjFNQ/s884/shopifytakeover.png "ShopifyTakeover")
