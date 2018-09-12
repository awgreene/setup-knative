# Run KNative in OpenShift
## Prereq
1. Be a cluster admin
2. Have an OpenShift/MiniShift cluster running
3. If you have SELinux, disable it:
```bash
$ setenforce 0
```

## Cleanup
If you disabled SELinux, enable it:
```bash
$ setenforce 1
```
