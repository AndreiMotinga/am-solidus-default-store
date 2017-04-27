#### [default solidus store](https://am-solidus-default-store.herokuapp.com/)

* Rails 5
* Solidus 2.2
* aws S3
* aws cloudfront
* Heroku

[/admin](https://am-solidus-default-store.herokuapp.com/admin) credentials
```
login: admin@example.com
passowrd: test123
```

#### SETUP
  * git clone git@github.com:AndreiMotinga/am-solidus-default-store.git
  * cd am-solidus-default-store
  * create aws s3 bucket
  * create cloudfront (origin domain name should point to bucket)
  * create .env.local with
  ```
    # https://github.com/ddollar/forego
    ASSET_HOST=localhost:3000
    APPLICATION_HOST=localhost:3000
    PORT=3000
    RACK_ENV=development
    RACK_MINI_PROFILER=0
    SECRET_KEY_BASE=development_secret
    EXECJS_RUNTIME=Node
    SMTP_ADDRESS=smtp.example.com
    SMTP_DOMAIN=example.com
    SMTP_PASSWORD=password
    SMTP_USERNAME=username
    WEB_CONCURRENCY=1

    S3_ACCESS_KEY=xxx
    S3_SECRET=xxx
    S3_BUCKET=xxx
    S3_REGION=xxx
    S3_HOST=xxx.cloudfront.net
  ```
  * bundle install
  * rake db:create
  * rake db:seed ( press Enter when prompted )
  * rake spree_sample:load ( to seed db with sample data. at this point image should get uploaded to s3 )
  * rails start
  * visit [localhost:3000](//localhost:3000)
