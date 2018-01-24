What is this
===

This is a couple of script, dirtily adapted from Cisco's support on rancid 2.3.
Rancid 2.3 and 3.7 is supported.

Installation
---

- Copy both scripts to /var/lib/rancid/bin
- `chmod +x /var/lib/rancid/bin/mlnx*`
- Add a router in router.db, using the `mellanox` hardware type
- For rancid 2.3:
  - edit /var/lib/rancid/bin/rancid-fe, you will find a `%vendortable` variable, add the entry `'mellanox'      => 'mlnxrancid'`:
  ```
  %vendortable = (
    'cat5'      => 'cat5rancid',
    'cisco'     => 'rancid',
    'cisco-nx'      => 'nxrancid',
    'cisco-xr'          => 'xrrancid',
    'mellanox'      => 'mlnxrancid',
    'mrtd'      => 'mrancid',
    );
- For rancid 3.7:
    - Edit /etc/rancid/rancid.types.conf, add `mellanox;script;mlnxrancid`
