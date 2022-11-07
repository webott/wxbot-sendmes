# wxbot-sendmes
Windows下PC企业微信机器人自动定时发送消息提醒
Windows下PC企业微信机器人自动定时发送消息提醒
由于业务需要，我的老板小亮是一个到点就下班的人，有一天我的老板小亮已经下班半小时了突然站起来说：“谁能在企业微信群众做一个定时发送消息的功能！！？”大家一脸茫然看着老板小亮，企业微信机器人还能控制？我赶紧上网查了一下。也查了官方文档
1、	企业微信添加机器人，记住接口机器人webhook地址
企业微信APP——选择群聊——点击右上角——选择群机器人（创建）
![image](https://user-images.githubusercontent.com/73727649/200246949-ac45f22a-8113-4646-92fb-587a65af5662.png)
2、	在电脑开始搜索并运行powershell ise
![image](https://user-images.githubusercontent.com/73727649/200246995-3e693985-4fe0-4ed8-b13d-cc980754fc2c.png)
3、	输入以下命令并运行，正常运行后可收到机器人发送的消息
注意：$url中的地址为你的机器人地址；content中的内容为你想发送的内容
4、	$url = "https://qyapi.weixin.qq.com/cgi-bin/webhook/send?key=3e4646656667cf"
5、	Invoke-WebRequest $url -Method POST -ContentType "application/json;charset=utf-8" -Body '{"msgtype": "text","text": {"content": "[太阳]各位小伙伴，健康申报天天有约！[呲牙]\n [爱心]请点击以下链接\nhttps://www.wjx.cn/jq/55555555555357.aspx\n[嘿哈][嘿哈]","mentioned_list":["@all"]}}'
![image](https://user-images.githubusercontent.com/73727649/200247291-51426b44-e3fb-4b17-ad79-d8126451a230.png)
4、能正常收到消息后，将命令另存为tixing.ps1（文件名自定义，记住保存路径）
![image](https://user-images.githubusercontent.com/73727649/200247326-15eb429b-8d95-4e51-854d-625efec6d78c.png)
![image](https://user-images.githubusercontent.com/73727649/200247341-12c09f69-bf36-4a9a-9228-2fdf07e15365.png)
•	5、搜索并打开powershell并执行如下命令，并输入y
•	Set-ExecutionPolicy Unrestricted
![image](https://user-images.githubusercontent.com/73727649/200247399-8907e219-9aff-48f6-a3ff-8f78c8a2715e.png)
•	6、打开计算机管理器
![image](https://user-images.githubusercontent.com/73727649/200247425-ff69dac7-4266-45af-9520-7ff47af30b98.png)
6、	创建计划任务 
![image](https://user-images.githubusercontent.com/73727649/200247464-4e012df9-36ce-41a9-b03b-4e0fc676c311.png)
![image](https://user-images.githubusercontent.com/73727649/200247479-a65b86b7-cdfe-4c9f-ac33-8e4f2560e30f.png)
![image](https://user-images.githubusercontent.com/73727649/200247501-1f3d3b8d-041c-46d8-a75b-421839b5ddc3.png)
![image](https://user-images.githubusercontent.com/73727649/200247515-b03084fc-17c3-4426-8188-65feedb7cfa9.png)
程序或脚本地址为C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
添加参数为第4步中保存的文件的，具体地址自行查看
定时发送企业微信消息完成，需保证每天此时间段，该电脑为开机状态
如需调试，可编辑最后一张图中的计划任务，将时间修改到最近的时间，观察是否可正常执行，可正常执行后再将时间调整至指定时间

企业微信：
目前已经实现了大部分功能，运行稳定，比如：发各种消息，
接收各种消息，外部群内部群管理，下载文件，加好友等等功能，
可提供接口，方便各种语言二次开发，欢迎技术交流。
Q：2645542961
![image](https://user-images.githubusercontent.com/73727649/200247933-3d196c8f-2361-493b-8feb-79b484849cd1.png)


