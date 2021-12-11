# XRP-Validator ripple.cfg
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

# 20211201. Tweaking in regard of fee-escalation
[transaction_queue]
ledgers_in_queue=2048
minimum_txn_in_ledger = 64
target_txn_in_ledger = 256

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

[path_search_max]
0

[rpc_startup]
{ "command": "log_level", "severity": "warning" }

[ssl_verify]
1

[voting]
# 10 drops
reference_fee = 10
# 10 XRP
account_reserve = 10000000
# 2 XRP
owner_reserve = 2000000
