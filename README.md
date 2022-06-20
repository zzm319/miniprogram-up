# miniprogram-up
小程序学习记录

遇到的第一个问题：
（1）版本管理：
遇到的问题：
1、使用https的形式，认证方式使用密码一直报认证方式不对或者一直转圈。
2、使用ssh的形式，密钥算法rsa已变成ed25519算法，需要重新生成密钥和配置github。
见images文件夹下的ssh-question.png

3、使用ssh的方式，用微信开发者工具的可视化工具与远程项目关联，会报错：
见images文件夹下的push-fail.png
然后先拉取代码，又报错误：
见images文件夹下的pull-fail.png

最终解决：还是使用终端指令解决：
①连接到远程仓库：
git remote add origin 远程仓库地址（https形式）

②将项目推送到远程仓库：
git push -u origin master
会出现错误：看图images文件夹下的success-flow.png，如果出现这个错误可能是因为远程仓库的README.md文件没有pull到本地仓库而导致的冲突。

③若出现错误先将文件拉到本地再执行第②点
输入git pull --rebase origin master 


