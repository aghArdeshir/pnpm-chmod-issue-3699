Make sure your regular user does not have access to modify `package-a/bin/something`

```
sudo chown root:root package-a/bin/something
```

Then go to package-b and `pnpm i`:

```
cd package-b; pnpm i
```

You should get this error:

```
 EPERM  EPERM: operation not permitted, chmod '/home/ardeshir/Workspace/pnpm-chmod-test/package-b/node_modules/package-a/bin/something'
```

For more info see https://github.com/pnpm/pnpm/issues/3699
