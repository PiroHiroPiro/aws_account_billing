# AWS Account Billing

This is a bot that notifies AWS account billing every morning.

<img width="504" alt="2018-07-31 20 46 36" src="https://user-images.githubusercontent.com/15605155/43458366-0035b202-9505-11e8-95f0-5934ac24f819.png">

# Requirement

- Python:3.6
- Pipenv:2018.11.26 or later

# Install

Setup AWS:

refs(Japanese only)
- [AWSの昨日までの各サービスの利用料金をSlackに通知させる](https://orebibou.com/2016/11/aws%E3%81%AE%E6%98%A8%E6%97%A5%E3%81%BE%E3%81%A7%E3%81%AE%E5%90%84%E3%82%B5%E3%83%BC%E3%83%93%E3%82%B9%E3%81%AE%E5%88%A9%E7%94%A8%E6%96%99%E9%87%91%E3%82%92slack%E3%81%AB%E9%80%9A%E7%9F%A5%E3%81%95/)
- [AWSの請求を毎日Slackに通知させる](https://qiita.com/ishikun/items/90b766e5555421970e9f)
- [LambdaでAWSの料金を毎日Slackに通知する（Python3）](https://qiita.com/isobecky74/items/88e8e0dcb0ee224a31e4)

Clone repository:

```console
$ git clone https://github.com/PiroHiroPiro/aws_account_billing.git
$ cd aws_account_billing
```

Install libraries:

```console
$ pipenv install
$ pipenv shell
```

Copy configuration file:

```console
$ cp lambda.json.example ./src/lambda.json
```

Enter the Lambda function name, roles, environment variables, etc. in the copied configuration file `lambda.json`:

Upload to Lambda:

```console
$ cd src
$ lambda-uploader
```

## Licence

This software is released under the MIT License, see [LICENSE](https://github.com/PiroHiroPiro/aws_account_billing/blob/master/LICENSE).

## Author

[Hiroyuki Nishizawa](https://github.com/PiroHiroPiro)
