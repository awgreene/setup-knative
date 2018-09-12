# Run KNative in OpenShift
## Prereq
1. Be a cluster admin
2. Have an OpenShift/MiniShift cluster running
3. If you have SELinux, disable it:
```bash
$ sudo setenforce 0
```
You can check to see the status of SELinux with the following command:
```bash
$ sestatus
SELinux status:                 enabled
SELinuxfs mount:                /sys/fs/selinux
SELinux root directory:         /etc/selinux
Loaded policy name:             targeted
Current mode:                   permissive
Mode from config file:          enforcing
Policy MLS status:              enabled
Policy deny_unknown status:     allowed
Memory protection checking:     actual (secure)
Max kernel policy version:      31
```
The output should indicate that `Current mode` is set to `permissive`

## Cleanup
If you disabled SELinux, enable it:
```bash
$ sudo setenforce 1
```
You can once again check that the command worked with `$ sestatus`, `Current Mode` should be set to `enforcing`
