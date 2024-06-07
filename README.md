# uoj自动签到

该工具是由llzzmm645小蒟蒻写的FZOIerのuoj的自动签到神器，使用方法如下

1. ~~给我点个赞~~
2. Fork/Import code这个仓库（最好Import code成私有仓库）
3. 打开`uoj_login.py`，将`XXXXXXXX`改为uoj用户名，将`########`改为uoj密码（如果有第二密码，请将`********`改为第二密码，如果不想泄露密码，也可以将第9行改为`password="你的token"`）
4. （你可以去点一下`Actions`，然后点击`uojqiandao`，点一下`run workflows`并选择`run`，如果成功签到，接下来开始设置定时服务，若没有`Actions`，请选择`Settings`>`Actions`>`General`>`Allow all actions and reusable workflows`，并点击`save`）
5. 打开`.github/workflows/main.yml`，将以下代码
   ``` ymal
   on: workflow_dispatch
   ```
   改为
   ``` ymal
   on: 
      workflow_dispatch: 
      schedule:
         - cron: 0 22 * * *
   ```
   从此，你就可以~~走上人生巅峰~~，愉快的使用它了，每天6点他都会帮你签到（由于未知原因，时间可能会有很大的偏差）
