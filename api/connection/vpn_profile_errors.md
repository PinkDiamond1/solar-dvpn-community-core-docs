## VPN system errors

### Profile creation

| Error Code | Error Message                      |
|------------|------------------------------------|
| 500        | "empty_name"                       |
| 500        | "name_already_exists"              |
| 500        | "load_tunnels_failed"              |
| 500        | "add_tunnel_failed"                |
| 500        | "invalid_interface"                |
| 500        | "invalid_peer"                     |

### Profile saving

| Error Code | Error Message                      |
|------------|------------------------------------|
| 500        | "name_required"                    |
| 500        | "private_key_required"             |
| 500        | "private_key_invalid"              |
| 500        | "address_invalid"                  |
| 500        | "name_required"                    |
| 500        | "listen_port_invalid"              |
| 500        | "mtu_invalid"                      |
| 500        | "public_key_required"              |
| 500        | "public_key_invalid"               |
| 500        | "pre_shared_key_invalid"           |
| 500        | "allowed_ips_invalid"              |
| 500        | "endpoint_invalid"                 |
| 500        | "pre_shared_key_invalid"           |
| 500        | "persistent_keep_alive_invalid"    |
| 500        | "public_key_duplicated"            |

### Profile removing

| Error Code | Error Message                      |
|------------|------------------------------------|
| 500        | "remove_tunnel_failed"             |

### Profile activation

| Error Code | Error Message                                           |
|------------|---------------------------------------------------------|
| 500        | "inactive"                                              |
| 500        | "starting_failed: `system error description`"           |
| 500        | "saving_failed: `system error description`"             |
| 500        | "loading_failed: `system error description`"            |
| 500        | "retry_limit_reached: `system error description`"       |
