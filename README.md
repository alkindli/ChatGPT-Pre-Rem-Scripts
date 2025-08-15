# ChatGPT-Pre-Rem-Scripts
Index. Hardware.

  
  
  Set-StaticAllRanges.ps1 — 

  
  probes .1/.254 gateways across:

  
  192.168.0.0/16

  
  172.10.0.0–172.40.255.255


  100.0.0.0/8

  
  10.0.0.0–31.255.255.255


  then assigns x.y.z.<HostOctet>/24 and installs a default route on the first interface that works (tries Wi-Fi → Cellular → Ethernet unless you override).


   
   PreAdd-AliasesAllRanges.ps1 — pre-adds a sampled set of /24 aliases with -SkipAsSource (no routes) across the same ranges.
