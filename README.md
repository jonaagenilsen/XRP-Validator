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

# 32 GB memory
[node_size]
huge

[ledger_history]  # This must be less than or equal to online_delete (if online_delete is used). The default is: 256
20000

# SSD
[node_db]
type=NuDB
path=/var/lib/rippled/db/nudb
online_delete=20000
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
XXXXXXXXXXXXXXXXXXXXXXXX

[rpc_startup]
{ "command": "log_level", "severity": "warning" }

[ssl_verify]
1


```
