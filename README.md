Bare bones repo to reproduce a ts-node bug in yarn workspaces

```
yarn
cd proj/workspace-a && yarn tsc
cd ../workspace-b
# run script b to print "hello world"
yarn ts-node index.ts

# modify script a to return something other than "hello world"
yarn tsc

# script b still outputs "hello world"
yarn ts-node index.ts
```