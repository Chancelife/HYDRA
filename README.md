* 第一次执行：git clone 到本地；
* 第N次执行：git checkout master&& git pull && git branch -d {github帐户} //删除存在的分支
* cd HYDRA

以下是核心,务必按步骤操作

* git branch {github帐户} //创建自己的开发分支
* git checkout {github帐户} //切换到自己的分支上，以后增删改等操作都在自己的分支上进行，新手切记, 老鸟忽略
* cd {题目目录} //提交自己的代码
//愉快的刷题
* git add . && git commit -s -m "{提交注解}"
* git push origin {github帐户}:{github帐户} //提交到远端仓库
* 进入https://github.com/jack1314007/HYDRA 页面; 选择New pull request;

