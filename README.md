# AWS Account Billing
毎朝，AWSの料金をサービスごとにSlackに通知する．

<img src="https://img.shields.io/github/license/mashape/apistatus.svg">

こんな感じ
<img width="504" alt="2018-07-31 20 46 36" src="https://user-images.githubusercontent.com/15605155/43458366-0035b202-9505-11e8-95f0-5934ac24f819.png">

# Dependency

- Python:3.6.5
- pip:10.0.1

# 目的

AWSから恐ろしい金額が請求されては困るので，せめて毎日SlackにAWS料金を通知したいと思う．

# Setup

AWSでの準備は以下の参考サイトを参照．

1. 必要なライブラリをインストールする
```
$ pip install lambda-uploader awscli
```
2. AWSの設定を行う
```
$ aws configure
```
3. リポジトリをクローンする
```
$ git clone https://github.com/PiroHiroPiro/aws_account_billing.git
```
4. ディレクトリを移動する
```
$ cd aws_account_billing
```
5. 設定ファイルをコピーする
```
$ cp lambda.json.example ./src/lambda.json
```
6. ディレクトリを移動する
```
cd src
```
7. コピーした設定ファイル`lambda.json`にLambdaの関数名やロール,環境変数等を入力する
8. Lambdaにアップロードする
```
$ lambda-uploader
```
9. LambdaでランタイムをPython3に変更する


# Licence
This software is released under the MIT License, see LICENSE.

# References
- [AWSの昨日までの各サービスの利用料金をSlackに通知させる](https://orebibou.com/2016/11/aws%E3%81%AE%E6%98%A8%E6%97%A5%E3%81%BE%E3%81%A7%E3%81%AE%E5%90%84%E3%82%B5%E3%83%BC%E3%83%93%E3%82%B9%E3%81%AE%E5%88%A9%E7%94%A8%E6%96%99%E9%87%91%E3%82%92slack%E3%81%AB%E9%80%9A%E7%9F%A5%E3%81%95/)
- [AWSの請求を毎日Slackに通知させる](https://qiita.com/ishikun/items/90b766e5555421970e9f)
- [LambdaでAWSの料金を毎日Slackに通知する（Python3）](https://qiita.com/isobecky74/items/88e8e0dcb0ee224a31e4)
