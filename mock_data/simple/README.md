
### Prototyping the JSON Format for Visualization

This mock data is taken from a 10-second `iperf3` run of ejfat-6 --> ejfat-5 traffic.

The JSON files are for visualization prototyping and the *.data files are the backup of the original format.

The JSON format is (currently) defined as:

```json
[
   { // One timestamp (by second) record
        "timestamp": 1762923213,
        "stats": [
            { // One (src, dst) pair
                "[129.57.177.6, 129.57.177.5]": {
                    "total_bytes": ,
                    "udp_bytes": [ ],   // fine-grained bins within this tick
                    "udp_packets": [ ],
                    "tcp_bytes": [ ],
                    "tcp_packets": [ ],
                }
            }
        ]
   },
   { // No.2 second record.
    "timestamp": 1762923214,
    "stats": []
   },
   ...
]
```
