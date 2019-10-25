# git

+ `git log` => `查看log`

## `取消上一次提交`
+ `先git log , 查看上次的提交id ，即commit 78a40f59ac819fee1b5183aee0f2acec81f9e4e1 (HEAD -> test) 中的那一串字符串`
+ `然后 git reset --hard 78a40f59ac819fee1b5183aee0f2acec81f9e4e1`

+ `再执行 git push self_rep HEAD --force`  `此时工作区被清空，但还未将修改提交到仓库`

## `merg`
+ `test merg 到 master`
   
`先 git checkout master , 然后git merg test`
`然后提交`


