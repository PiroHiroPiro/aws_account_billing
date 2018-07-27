# AWS Account Billing

## 目的
AWSから恐ろしい金額が請求されては困るので，せめて毎日SlackにAWS料金を通知したいと思う．

## 準備

AWSでの準備は以下の参考サイトを参照．

```
$ pip install lambda-uploader awscli
$ aws configure
$ git clone https://github.com/PiroHiroPiro/aws_account_billing.git
$ cd aws_account_billing
$ cp lambda.json.example ./src/lambda.json # 環境変数等を入力
$ cd src
$ lambda-uploader
```

## 参考
- [AWSの昨日までの各サービスの利用料金をSlackに通知させる](https://orebibou.com/2016/11/aws%E3%81%AE%E6%98%A8%E6%97%A5%E3%81%BE%E3%81%A7%E3%81%AE%E5%90%84%E3%82%B5%E3%83%BC%E3%83%93%E3%82%B9%E3%81%AE%E5%88%A9%E7%94%A8%E6%96%99%E9%87%91%E3%82%92slack%E3%81%AB%E9%80%9A%E7%9F%A5%E3%81%95/)
- [AWSの請求を毎日Slackに通知させる](https://qiita.com/ishikun/items/90b766e5555421970e9f)
- [LambdaでAWSの料金を毎日Slackに通知する（Python3）](https://qiita.com/isobecky74/items/88e8e0dcb0ee224a31e4)
