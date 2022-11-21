# WireGuard listening UDP port Schema

```txt
http://schema.nethserver.org/cluster/join-node-input.json#/properties/listen_port
```

Listening UDP port for incoming WireGuard VPN packets

| Abstract            | Extensible | Status         | Identifiable            | Custom Properties | Additional Properties | Access Restrictions | Defined In                                                                    |
| :------------------ | :--------- | :------------- | :---------------------- | :---------------- | :-------------------- | :------------------ | :---------------------------------------------------------------------------- |
| Can be instantiated | No         | Unknown status | Unknown identifiability | Forbidden         | Allowed               | none                | [join-node-input.json\*](cluster/join-node-input.json "open original schema") |

## listen\_port Type

`integer` ([WireGuard listening UDP port](join-node-input-properties-wireguard-listening-udp-port.md))

## listen\_port Constraints

**minimum (exclusive)**: the value of this number must be greater than: `1024`
