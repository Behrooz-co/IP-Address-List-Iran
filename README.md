## Get IP Iran
This script is for get iran ip subnet and added to address list Mikrotik

## How to use script
```bash
foreach i in={"IR"} do={
  /tool fetch url="https://github.com/Behrooz-co/IP-Address-List-Iran/blob/main/Address-List.rsc" dst-path=IR
  /ip firewall address-list remove [/ip firewall address-list find list=IR]
  /import file-name=IR
  /file remove IR
}
```

## Author
[Behrooz Kheirabadi](https://github.com/Behrooz-co/)

