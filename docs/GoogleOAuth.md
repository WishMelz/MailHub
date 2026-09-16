# MailHub-GoogleOauth
首选确定你的域名是什么？

比如是：https://mailhub.xxx.com 。下面的所有地址都会使用此域名

```
#谷歌项目ID
GOOGLE_CLOUD_PROJECT_ID=

#OAuth客户端ID
GOOGLE_CLIENT_ID=
#OAuth客户端密钥
GOOGLE_CLIENT_SECRET=
#OAuth客户端回调地址
GOOGLE_REDIRECT_URI=https://mailhub.xxxx.com/oauth/callback

#是否开通谷歌订阅推送
GOOGLE_GMAIL_WATCH_ENABLED=false
#Pub/Sub 主题名字
GOOGLE_GMAIL_PUBSUB_TOPIC=

#服务号电子邮件
GOOGLE_GMAIL_PUBSUB_SERVICE_ACCOUNT=
#订阅名称
GOOGLE_GMAIL_PUBSUB_SUBSCRIPTION=
#Pub/Sub 订阅推送地址
GOOGLE_GMAIL_PUBSUB_AUDIENCE=https://mailhub.xxxx.com/api/webhooks/google/gmail

GOOGLE_OAUTH_SCOPES=openid email profile https://www.googleapis.com/auth/gmail.readonly
GMAIL_API_BASE_URL=https://gmail.googleapis.com/gmail/v1
```

## 1、创建项目

应用创建入口：[https://console.cloud.google.com/](https://console.cloud.google.com/)

<figure class="image"><img style="aspect-ratio:755/495;" src="images/GoogleOauth/2_MailHub-GoogleOauth_image.png" width="755" height="495"></figure>

**这一步可以获得** `**GOOGLE_CLOUD_PROJECT_ID**` 

## 2、服务账号

顶部搜索“”服务账号”

<figure class="image"><img style="aspect-ratio:1561/726;" src="images/GoogleOauth/16_MailHub-GoogleOauth_image.png" width="1561" height="726"></figure><figure class="image"><img style="aspect-ratio:649/626;" src="images/GoogleOauth/17_MailHub-GoogleOauth_image.png" width="649" height="626"></figure>

其他全部默认

<figure class="image"><img style="aspect-ratio:1056/375;" src="images/GoogleOauth/7_MailHub-GoogleOauth_image.png" width="1056" height="375"></figure>

**这一步可以获取：**`**GOOGLE_GMAIL_PUBSUB_SERVICE_ACCOUNT**`

## 3、API 和服务

搜索：API 和服务

<figure class="image"><img style="aspect-ratio:1320/359;" src="images/GoogleOauth/27_MailHub-GoogleOauth_image.png" width="1320" height="359"></figure>

点击启动API和服务

<figure class="image"><img style="aspect-ratio:928/519;" src="images/GoogleOauth/11_MailHub-GoogleOauth_image.png" width="928" height="519"></figure>

搜索启用 `Gmail API`和`Pub/Sub`

<figure class="image"><img style="aspect-ratio:1546/674;" src="images/GoogleOauth/3_MailHub-GoogleOauth_image.png" width="1546" height="674"></figure><figure class="image"><img style="aspect-ratio:1394/577;" src="images/GoogleOauth/19_MailHub-GoogleOauth_image.png" width="1394" height="577"></figure>

## 4、配置 oauth

<figure class="image"><img style="aspect-ratio:553/426;" src="images/GoogleOauth/14_MailHub-GoogleOauth_image.png" width="553" height="426"></figure><figure class="image"><img style="aspect-ratio:587/605;" src="images/GoogleOauth/20_MailHub-GoogleOauth_image.png" width="587" height="605"></figure><figure class="image"><img style="aspect-ratio:583/402;" src="images/GoogleOauth/15_MailHub-GoogleOauth_image.png" width="583" height="402"></figure><figure class="image"><img style="aspect-ratio:1599/497;" src="images/GoogleOauth/13_MailHub-GoogleOauth_image.png" width="1599" height="497"></figure><figure class="image"><img style="aspect-ratio:621/712;" src="images/GoogleOauth/21_MailHub-GoogleOauth_image.png" width="621" height="712"></figure><figure class="image"><img style="aspect-ratio:513/608;" src="images/GoogleOauth/28_MailHub-GoogleOauth_image.png" width="513" height="608"></figure>

**这一步获取了：**`**GOOGLE_CLIENT_ID**`**,**`**GOOGLE_CLIENT_SECRET**`

## 5、配置应用信息

<figure class="image"><img style="aspect-ratio:285/390;" src="images/GoogleOauth/24_MailHub-GoogleOauth_image.png" width="285" height="390"></figure>

<figure class="image"><img style="aspect-ratio:401/969;" src="images/GoogleOauth/5_MailHub-GoogleOauth_image.png" width="401" height="969"></figure>

## 6、发布应用

<figure class="image"><img style="aspect-ratio:854/522;" src="images/GoogleOauth/9_MailHub-GoogleOauth_image.png" width="854" height="522"></figure>

他会提示如下

<figure class="image"><img style="aspect-ratio:1306/91;" src="images/GoogleOauth/12_MailHub-GoogleOauth_image.png" width="1306" height="91"></figure>

不用理会，自己使用不影响

## 7、配置 Pub/Sub

<figure class="image"><img style="aspect-ratio:537/296;" src="images/GoogleOauth/18_MailHub-GoogleOauth_image.png" width="537" height="296"></figure><figure class="image"><img style="aspect-ratio:899/525;" src="images/GoogleOauth/8_MailHub-GoogleOauth_image.png" width="899" height="525"></figure><figure class="image"><img style="aspect-ratio:642/445;" src="images/GoogleOauth/1_MailHub-GoogleOauth_image.png" width="642" height="445"></figure><figure class="image"><img style="aspect-ratio:642/341;" src="images/GoogleOauth/23_MailHub-GoogleOauth_image.png" width="642" height="341"></figure>

**这一步获取了：**`**GOOGLE_GMAIL_PUBSUB_TOPIC**`

### 配置权限

<figure class="image"><img style="aspect-ratio:1058/542;" src="images/GoogleOauth/22_MailHub-GoogleOauth_image.png" width="1058" height="542"></figure>

主体配置：`gmail-api-push@system.gserviceaccount.com`

如果提示没有，等一等刷新页面

<figure class="image"><img style="aspect-ratio:676/816;" src="images/GoogleOauth/MailHub-GoogleOauth_image.png" width="676" height="816"></figure>

## 8、配置订阅

<figure class="image"><img style="aspect-ratio:900/488;" src="images/GoogleOauth/4_MailHub-GoogleOauth_image.png" width="900" height="488"></figure><figure class="image"><img style="aspect-ratio:593/749;" src="images/GoogleOauth/26_MailHub-GoogleOauth_image.png" width="593" height="749"></figure><figure class="image"><img style="aspect-ratio:720/752;" src="images/GoogleOauth/6_MailHub-GoogleOauth_image.png" width="720" height="752"></figure><figure class="image"><img style="aspect-ratio:1213/488;" src="images/GoogleOauth/25_MailHub-GoogleOauth_image.png" width="1213" height="488"></figure>

**这一步获取了：**`GOOGLE_GMAIL_PUBSUB_SUBSCRIPTION`

## 谷歌应用配置已完成！