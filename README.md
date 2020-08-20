# XRP-Validator ripple.cfg
```
[server]
port_rpc_admin_local
port_ws_admin_local

[port_rpc_admin_local]
port = 5005
ip = 127.0.0.1
admin = 127.0.0.1
protocol = http

[port_ws_admin_local]
port = 6006
ip = 127.0.0.1
admin = 127.0.0.1
protocol = ws

# https://xrpl.org/capacity-planning.html
[node_size]
huge

#[peer_private]
#1

#[ips_fixed]
# Need to get this party started :)

# This must be less than or equal to online_delete (if online_delete is used). The default is: 256
[ledger_history]
50000

[node_db]
type=NuDB
path=/var/lib/rippled/db/nudb
online_delete=50000
advisory_delete=0

[fetch_depth]
500

[database_path]
/var/lib/rippled/db

[debug_logfile]
/var/log/rippled/debug.log

[sntp_servers]
pool.ntp.org
time.windows.com
time.apple.com
time.nist.gov

[validators_file]
/opt/ripple/etc/validators.txt

[validator_token]
XXXXXXXXXXXXXX

[rpc_startup]
{ "command": "log_level", "severity": "warning" }

[ssl_verify]
1

[amendments]
30CD365592B8EE40489BA01AE2F7555CAC9C983145871DC82A42A31CF5BAE7D9 DeletableAccounts
8F81B066ED20DAECA20DF57187767685EEF3980B228E0667A650BAF24426D3B4 fixCheckThreading
621A0B264970359869E3C0363A899909AAB7A887C8B73519E4ECF952D33258A8 fixPayChanRecipientOwnerDir
157D2D480E006395B76F948E3E07A45A05FE10230D88A7993C71F97AE4B1F2D1 Checks
3012E8230864E95A58C60FD61430D7E1B4D3353195F2981DC12B0C7C0950FFAC FlowCross
00C1FC4A53E60AB02C864641002B3172F38677E29C26C5406685179B37E1EDAC RequireFullyCanonicalSig
89308AF3B8B10B7192C4E613E1D2E4D9BA64B2EE2D5232402AE82A6A7220D953 fixQualityUpperBound

```
