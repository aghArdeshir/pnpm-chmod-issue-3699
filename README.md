Make sure your user does not have access to modify `package-a/bin/something`

```
ls -la package-a/bin/ # should be owned by root
```

if its not owned by root:

```
sudo chmod package-a/bin/something
```

Then go to package-b and `pnpm i`:

```
cd package-b; pnpm i
```
