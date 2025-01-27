## Get IP Iran
This Script is for get Iran ip Subnet and added to Address list Mikrotik

## Update
2025/01/27

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

