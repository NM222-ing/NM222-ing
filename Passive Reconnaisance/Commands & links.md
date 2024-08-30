# Whois
```whois tryhackme.com```
# Nslookup
```nslookup tryhackme.com``` ```nslookup -type=A tryhackme.com 1.1.1.1``` ```
# DNS dump
https://dnsdumpster.com/ - ex.: tryhackme.com -> find subdomains registered in DNS and all information about them (already running some nslookup and whois)
# Shodan - general:
> Search for host: https://www.shodan.io/search?query=btrl.ro

> Find ASN: https://asnlookup.com/ipv4/194.145.238.48

> Search for items in the specified ASN: https://www.shodan.io/search?query=asn%3AAS34184

This way we can find vulnerable entry points in the network
# Shodan Monitor:
Tool for monitoring your own infrastructure and getting alerts: https://monitor.shodan.io/dashboard
# Shodan Queries:
Ransomware attacked:
> ```has_screenshot:true encrypted attention```

No authentication:
> ```screenshot.label:ics```

Shodan Dorks: https://github.com/lothos612/shodan
> Shodan browser extension: https://chrome.google.com/webstore/detail/shodan/jjalcfnidlmpjhdfepjhjbhnhkbgleap

Shodan API: https://github.com/bee-san/How-I-Hacked-Your-Pi-Hole/blob/master/README.md
