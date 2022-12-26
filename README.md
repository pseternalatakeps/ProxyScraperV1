# Proxy Scraper & Checker [V1]

Allows you to scrape more than **1K HTTP proxies in under 2 minutes**.

**Fresh public proxies** are scraped from these sources:

* [sslproxies.org](http://sslproxies.org) (HTTP, HTTPS)
* [free-proxy-list.net](http://free-proxy-list.net) (HTTP, HTTPS)
* [us-proxy.org](http://us-proxy.org) (HTTP, HTTPS)
* [socks-proxy.net](http://socks-proxy.net) (Socks4, Socks5)
* [proxyscrape.com](https://proxyscrape.com) (HTTP, Socks4, Socks5)
* [proxy-list.download](https://www.proxy-list.download) (HTTP, HTTPS, Socks4, Socks5)

## Installation
Use these commands to ensure you have the default requirements.
```bash
sudo apt install git -y
sudo apt install python -y
sudo apt install python3 -y
```

Use this command to download this repository.
```bash
git clone https://github.com/pseternalatakeps/ProxyScraperV1.git
```

Use this command to install dependencies.


```bash
pip3 install -r requirements.txt
```

## Usage

**For scraping:**

```bash
python3 scraper.py -p http
```
* With `-p` or `--proxy`, You can choose your proxy type. Supported proxy types are: **HTTP - HTTPS - Socks (Both 4 and 5) - Socks4 - Socks5** 
* With `-o` or `--output`, create and write to a .txt file. (Default is **output.txt**)
* With `-v` or `--verbose`, more details.
* With `-h` or `--help`, Show help to who did't read this README.

**For checking:**

```bash
python3 checker.py -t 20 -s google.com -l output.txt
```

* With `-t` or `--timeout`, dismiss the proxy after -t seconds (Default is **20**)
* With `-p` or `--proxy`, check HTTPS or HTTP proxies (Default is **HTTP**)
* With `-l` or `--list`, path to your list.txt. (Default is **output.txt**)
* With `-s` or `--site`, check with specific website like google.com. (Default is **google.com**)
* With `-r` or `--random_agent`, it will use a random user agent per proxy.
* With `-v` or `--verbose`, more details.
* With `-h` or `--help`, Show help to who did't read this README.

## Good to know
* Dead proxies will be **automatically** removed.
* This specific script is able to scrape socks proxies but the checker can **only check HTTP(S) proxies**.

## Contributing
Pull requests are allowed. You are welcome to discuss major changes to this project by opening an issue.

### Issues
Submit issues and enhancement requests by opening an issue.
