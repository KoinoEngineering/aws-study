# aws-study
AWSの勉強用のリポジトリ
基本的にリージョンはロンドンとする
## step3
以下のものを実現する
- VPC
  - IGW
  - NGW(MySql等インストール用)
  - Subnet (public)
    - EC2  踏み台
      - 固定IPからのSSHのみ許可
      - 他のEC2インスタンスのSSHはここからのみの許可
    - EC2  nginxサーバー
  - Subnet (private)
    - EC2  MySql
      - NGWを介してのみ外部との接続が可能