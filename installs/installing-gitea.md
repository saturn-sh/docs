External resources:

- https://dev.to/nabbisen/gitea-on-openbsd-using-official-package-2ogl
- https://wiki.archlinux.org/index.php/Gitea

```sh
pkg_add gitea
```

Notes:

- Configuration files: `/etc/gitea/app.ini`
- `GITEA_CUSTOM`: `/var/gitea/custom`
- `ROOT_PATH` for logs: `/var/log/gitea`
