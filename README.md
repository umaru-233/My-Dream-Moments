![ATRI.jpg](img%2FATRI.jpg)
- 警告：2025年2月5日起腾讯突然更新了相关检测机制，导致所有使用itchat库的项目均拉闸。使用itchat项目的库均出现了无法登录<code>错误码1102</code>的问题，并且登陆过itchat的微信号会导致不同程度的封号。事发突然，确实没有办法。在可以遇见的未来，itchat库预计将不会再可用，因此此分支放弃维护，接入微信的方案转而操作真实客户端完全安全的<code>wxauto</code>。请您转换到<code>WeChat-wxauto</code>分支以继续。
- 如果您有提供更好的方案，请提交PR!
---
## 简介
简体中文 · [English](./README_EN.md) 
- 使用教程：[90秒让DeepSeek沉浸式接入微信变成你的Ai老婆](https://www.bilibili.com/video/BV1QFPfeQE5m/)
- My Dream Moments 是一个基于大型语言模型（LLM）的情感陪伴程序，能够接入微信，提供更真实的情感交互体验。内置了 Atri-My dear moments 的 prompt，并且解决了传统人机对话程序一问一答的死板效果，提供沉浸式角色扮演和多轮对话支持。项目名字来源是运行在该程序上的第一个智能体的原作名称+项目价值观混合而来。
- 推荐使用DeepSeek V3 模型。<br>
![demo.png](img%2Fdemo.png)
---
## 声明
- 本项目仅用于交流学习，LLM发言不代表作者本人立场。prompt所模仿角色版权归属原作者。任何未经许可进行的限制级行为均由使用者个人承担。
---

## 已实现的功能
- [x] 对接微信，沉浸式角色扮演
- [x] 聊天分段响应，消除人机感
- [x] 多轮对话
- [x] 多用户支持
- [x] 由 DeepSeek R1 利用游戏文本生成的 Prompt
- [x] 无需联网的时间感知

---

## 待实现功能，期待您的加入
- [ ] 定时任务与智能定时任务
- [ ] 利用 8B 小模型实时生成记忆并定期整理，实现持久记忆
- [ ] WebUI，方便不理解代码的用户配置项目
- [ ] 负载均衡
- [ ] Releases

---

## 如何运行项目

### 1. 前期准备
1. **备用手机/安卓模拟器**  
   - 微信电脑端登录必须有一个移动设备同时登录，因此不能使用您的主要设备。
   
2. **微信小号**  
   - 需要注册时间较久的微信号（新注册的账号可能无法登录为 bot）。如果扫码后报错，请检查此项。

3. **DeepSeek API Key**  
   - 推荐使用：[获取 API Key（15元免费额度）](https://cloud.siliconflow.cn/i/aQXU6eC5)

---

### 2. 部署项目
1. **克隆本仓库**  
   ```bash
   git clone <仓库地址>
2. **安装依赖**  
   ```bash
   pip install -r requirements.txt
3. **配置<code>config.py</code>**  
修改<code>DEEPSEEK_API_URL</code>和<code>DEEPSEEK_API_KEY</code>。
按需调整<code>MAX_TOKEN</code>、<code>TEMPERATURE</code>和<code>MODEL</code>。
4. 运行<code>bot.py</code>
   ```bash
   python bot.py
### 3. 如何使用
1. **项目运行后，根目录下会生成 <code>QR.png</code>。**
   - 使用您想作为 bot 的微信号扫码登录。
   - 如果控制台没有响应，请重启项目以刷新二维码并重新登录。
2. **当控制台提示 <code>Start auto replying.</code> 时，表示程序已成功运行。您可以在微信上与 bot 对话测试效果。**
## 如果您想修改prompt
- 项目根目录下的 <code>prompt.md</code> 可以编辑，修改后重启项目生效。
- 注意：请不要修改与反斜线 <code> \ </code>相关的 prompt，因为它们被用于分段回复消息。
## 赞助
此项目欢迎赞助。您的支持对我非常重要！
- 赞助用户如需远程部署或定制 prompt，请联系我。
- E-Mail: yangchenglin2004@foxmail.com 
- Bilibili: [umaru今天吃什么](https://space.bilibili.com/209397245)
- 感谢您的支持与使用！!<br>
![qrcode.jpg](img%2Fqrcode.jpg)
