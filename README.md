# HFUT_AutoSubmit  

# 项目说明

通过使用Github的Actions功能完成的合肥工业大学今日校园疫情信息收集自动打卡签到（针对2021年1月后启用的每日打卡保平安）

## 使用说明

1. **在右上角Fork本项目**  
   ![图示](https://cdn.jsdelivr.net/gh/qdddz/HFUT_AutoSubmit/docs/imgs/fork.jpg)  
2. **启用Actions**  
   1. 点击上方Actions按钮，并且启用
   ![图示](https://cdn.jsdelivr.net/gh/qdddz/HFUT_AutoSubmit/docs/imgs/actions1.jpg)  
   2. 启用Workflow
   ![图示](https://cdn.jsdelivr.net/gh/qdddz/HFUT_AutoSubmit/docs/imgs/actions2.jpg)  
3. **获取sckey，推送每日运行结果**  
   1. 前往 [sct.ftqq.com](https://sct.ftqq.com/login) 点击登入，创建账号。
   2. 获取到生成的 Key。之后会将其增加到 Github Secrets 中，变量名为 `sckey`
4. **点击项目 Settings -> Secrets -> New Secrets 添加以下 4 个 Secrets，其中server酱微信推送的sckey可见上一步**  
   |Name|Value|
   |-----|-----|
   | username | 学号 |
   | password | 新信息门户密码 |
   | address | 具体的填报地址，相当于手机定位地址 |
   | sckey | server酱推送的sckey |  
   ![图示](https://cdn.jsdelivr.net/gh/qdddz/HFUT_AutoSubmit/docs/imgs/secret.jpg)  
5. **运行结果将在每天14-17点左右通过微信的server酱通知给您**  
   ![图示](https://cdn.jsdelivr.net/gh/qdddz/HFUT_AutoSubmit/docs/imgs/result.jpg)

## 后记  
0. **填报信息实际上会和前一日的保持一致，记得返校离校后进App修改**
1. 实在没办法，学校的系统就是很垃圾，所以每天从14-19点每隔一个小时会多次尝试。如果想更改尝试次数，请前往/.github/workflows/python-app.yml中corntab处更改，有时间会更换一套更好的逻辑
2. 如果上面的图片无法正常加载，纯属github被墙了。。
3. 有问题请反馈至QQ：710830913

## 致谢

@JunzhouLiu/BILIBILI-HELPER
@HowardZorn/hfut_auto_check-in
