# XRP-Validator ripple.cfg
```
port_ws_admin_local
[port_rpc_admin_local]
port = 5005
ip = 127.0.0.1
admin = 127.0.0.1
protocol = http

[port_peer]
port = 51235
ip = 0.0.0.0
protocol = peer

[port_ws_admin_local]
port = 6006
ip = 127.0.0.1
admin = 127.0.0.1
protocol = ws

[node_size]
small

[node_db]
type=NuDB
path=/var/lib/rippled/db/nudb
online_delete=2000
advisory_delete=0

[database_path]
/var/lib/rippled/db

[debug_logfile]
/var/log/rippled/debug.log

[sntp_servers]
time.windows.com
time.apple.com
time.nist.gov
pool.ntp.org

[validators_file]
/opt/ripple/etc/validators.txt

[validator_token]
xxxxxxxxxxxxxxxxxx

[rpc_startup]
{ "command": "log_level", "severity": "warning" }

[ssl_verify]
1
```
