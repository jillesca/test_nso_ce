# test_nso_ce

Test if NSO can be brining up by issuing the following commands:

Based on https://developer.cisco.com/learning/labs/nso-intro/introduction/

```bash

source $NCS_DIR/ncsrc
ncs-netsim --dir ~/example/netsim create-network cisco-ios-cli-3.8 2 ios
ncs-setup --dest ~/example --netsim-dir ~/example/netsim
cd ~/example/
ncs-netsim start

ncs

ncs --version
ncs --status
```

from inside NSO
```bash
ncs_cli -C -u admin
devices sync-from
devices device ios1 check-sync
config
show full-configuration devices device ios1 config | nomore
devices device ios0 config
ios:hostname nso.cisco.com
top
commit dry-run outformat native
commit
```

