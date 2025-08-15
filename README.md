1) Is the approach “safe”? (what I do and what I avoid)

Only built-in cmdlets. Scripts use Get/Set/New/Remove-Net* cmdlets from Windows’ NetTCPIP module. No Invoke-Expression, no external downloads, no registry hacks, no scheduled tasks.

Scoped changes. Every action is per-interface using -InterfaceAlias so you don’t accidentally touch the wrong adapter.

Least surprise. When a route is touched, it’s only the default route on that adapter. IP adds are explicit; no wildcards.

PS 5.1–friendly. No UInt64 math or tricky bitwise games; simple loops & dotted-octet handling.

Clear exit. Basic, readable output; errors fail fast with a message you can act on.

2) New “No-Wait” scripts (to avoid Windows “Identifying…” delays)

These are purpose-built so you don’t sit through DHCP timeout screens when you plug into Ethernet/broadband, Wi-Fi, or Cellular.
