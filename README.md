1. 本地创建一个文件夹
2. 运行 npm init -y
3. 运行 npm i lerna lerna-changelog --save-dev 
4. 运行lerna init --i
5. cd packages
6. mkdir package1 package2 package3或者使用lerna create package5
7. 分别在package1 package2, package3中运行npm init -y
8. 在 Issues那边新增一个label,名为feat

   9.从master拉取一个分支fixbug,修改完成后，并把fixbug  push到github上

  10.在github上找到fixbug，然后创建一个pr，在创建pr时，选择labels

![1569724959166](README.assets/1569724959166.png)

11.提交pr后，会看到

![1569725050380](README.assets/1569725050380.png)

12.在merge的时候，可以再选择labels，进行merge

![1569725142158](README.assets/1569725142158.png)



13.git pull origin master

14.执行 lerna-changelog，会报错must private github_auth

15.在自己的github上创建token：

e171896f9ac3df0d4e8a195bde8dae4c41199a2f

![1569726187227](README.assets/1569726187227.png)



把这个token值，以环境变量的形式暴露，常用的，可以添加到~/.bash_profile里

export GITHUB_AUTH="..."



参考：<https://github.com/frontend9/fe9-library/issues/243

><https://github.com/lerna/lerna-changelog#github-token>