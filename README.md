# test_nso_ce

Test if NSO can be brining up by issuing the following commands:

```bash
source ~/nso/ncsrc

ncs-setup --package ~/nso/packages/neds/cisco-ios-cli-6.91/ --dest nso-instance

cd nso-instance
ncs

ncs --version
ncs --status

ncs_cli -C -u admin
```
