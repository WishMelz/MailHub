# MailHub

MailHub 是一个轻量、自托管、本地优先的统一邮箱管理工具，在同一工作台管理 Microsoft、Google Gmail、IMAP 和 POP3 账户

## 使用教程
```
git clone https://github.com/WishMelz/MailHub.git
cd /MailHub
cp .env.production.example .env
docker compose up -d
```

## 备份/迁移
备份`data`文件夹，在新项目直接运行即可迁移成功


# 谷歌项目配置
[谷歌项目配置](https://github.com/WishMelz/MailHub/blob/docs/docs/GoogleOAuth.md)

# 微软项目配置
[微软项目配置](https://github.com/WishMelz/MailHub/blob/docs/docs/MicrosoftOAuth.md)