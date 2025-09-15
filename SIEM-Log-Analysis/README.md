index=security sourcetype=wineventlog:security EventCode=4625
| stats count by Account_Name, src_ip
| where count > 5
