# EverPhotoCheckin

[时光相册](https://web.everphoto.cn) 签到助手，利用GitHub Actions每天自动执行

![demo](imgs/checkin.png)

## 食用指南

**首先，Fork本项目到自己的仓库。**

![Fork repository](imgs/fork.png)

**进入自己刚才Fork的仓库，点击 Settings -> Secrets -> New repository Secrets 添加以下Secrets。**

|         Name          |                     Value                      |
| :-------------------: | :--------------------------------------------: |
|  EVER_PHOTO_MOBILE  | 登录手机号，包括国际区号， 如 `+8613800138000` |
| EVER_PHOTO_PASSWORD |                    登录密码                    |
|  EVER_PHOTO_TOKEN   |              Bearer令牌（可选）               |

![Set Secrets](imgs/secrets.png)

> 设置了 `EVER_PHOTO_TOKEN` 的条件下无须再设置 `EVER_PHOTO_MOBILE` 和 `EVER_PHOTO_PASSWORD` 。

**切换至Actions选项卡，开启Actions并触发每日自动执行。**

![Run actions](imgs/actions.png)

**当然，你也可以自行编译程序并在本地手动执行：**

```sh
$ go get github.com/winterssy/EverPhotoCheckin
$ EverPhotoCheckin -mobile YOUR_MOBILE -password YOUR_PASSWORD
```

## 开发计划

由于Actions执行失败时GitHub会自动邮件通知，故程序暂不集成推送相关功能，有需要的话未来会接入 [Server酱](http://sc.ftqq.com) 。

## 赞赏支持

如果你觉得本项目对你有帮助，或者单纯想请开发者喝杯咖啡，可使用微信扫描下方的赞赏码。

<div align="center">
	<img src="imgs/wechat_reward.png" alt="微信赞赏码" width= "320px" />
</div>

