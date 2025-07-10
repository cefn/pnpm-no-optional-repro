# pnpm-no-optional-repro

To reproduce the failure, run `pnpm install` edit the .npmrc to enable `node-linker=hoisted`, then run `pnpm install --no-optional --frozen-lockfile`

On Mac at least it will error out with...

```
$ pnpm install --no-optional --frozen-lockfile 
Lockfile is up to date, resolution step is skipped
 ERR_PNPM_LOCKFILE_MISSING_DEPENDENCY  Broken lockfile: no entry for '@esbuild/aix-ppc64@0.25.6' in pnpm-lock.yaml
```
