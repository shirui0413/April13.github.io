オンプレミス　クロードサービス



VPC　Virtual private cloud

​	subnet1

​	subnet2

​	ルートテーブル　（public(default) / private）

サブネットと通信のため、カスタマイズルートテーブル作成



AMI →OS、アプリケーション、設定、データなど含まれてる仮想マシンのイメージ

インスタンスタイプ→CPU、メモリ、ストレージなど。ハードウエアーの配置にって、料金が違う

EBS→ブロックストレージサービス（相当于硬盘）である。EC2にアタッチして使用する。シャットダウン後、データも保持するためEBS必要。



EC2 とセキュリティグループ関連つける、自分のセキュリティーグループアップロードおすすめ（必要）



EIP（elastic ip address）

EC２が停止、終了、再起動した場合、IPアドレスが変わるため、EIP必要。EIPのアドレスは静的である。

アタッチ、デダッチ？





什么是 CIDR？CIDR（无类域间路由）是一种用于 **IP地址划分和路由** 的方法，格式为：`コピーする編集するIP地址/子网前缀长度`例如：`コピーする編集する10.0.0.0/16`这里：`10.0.0.0` 是起始 IP 地址`/16` 表示子网掩码为 255.255.0.0，也就是前 16 位是网络部分🟡 在 AWS 中的用途在 AWS 中，CIDR 用于划分虚拟网络（VPC）和子网（Subnet），控制 IP 地址的分配范围。🔸 VPC 的 CIDR 范围（例如）：`コピーする編集する10.0.0.0/16 → 允许使用的 IP 总数：2^16 = 65,536 个 IP 地址（包含 VPC 内所有子网）`🔸 子网的 CIDR 范围（例如）：`コピーする編集する10.0.1.0/24 → 允许使用的 IP 总数：2^8 = 256 个 IP 地址`其中 5 个 IP 地址保留给 AWS（如网络地址、广播地址、VPC 网关等），可用 IP 为 251 个。✅ 常用 CIDR 范围（适合 VPC/Subnet） CIDR 范围子网大小可用 IP 数/281611/24256251/1665,53665,531





https://aws.amazon.com/jp/free/?trk=58ef6015-6519-450b-96ea-258378c321895&sc_channel=ps&ef_id=EAIaIQobChMIlqXgot2_jAMVhdBMAh0WRxziEAAYASAAEgKHy_D_BwE:G:s&s_kwcid=AL!4422!3!618145042463!p!!g!!aws!18137558856!140477907517&gclid=EAIaIQobChMIlqXgot2_jAMVhdBMAh0WRxziEAAYASAAEgKHy_D_BwE&all-free-tier.sort-by=item.additionalFields.SortRank&all-free-tier.sort-order=asc&awsf.Free%20Tier%20Types=*all&awsf.Free%20Tier%20Categories=*all



keyファイル格納フォルダに移動

```
cd %path%(keyファイル格納)
```



パブリクEC2と接続

```
ssh -i serverKey.pem ec2-user@43.206.242.155
```

**serverKey.pem**作成したペアキーファイル

**43.206.242.155**パブリック IPv4 アドレス



EC2にフィアルアップロード  (別のWindowから)

```
scp -i serverKey.pem serverKey.pem ec2-user@43.206.242.155:/tmp
```

**-i**  

identity_file： 指定ファイルからキーファイル読む

**serverKey.pem**※１

指定ファイル

**serverKey.pem**※２

転送ファイル

**ec2-user@43.206.242.155:/tmp**

Path



EC2接続のwindowからアップロードしたファイルの確認

```
cd /tmp    // パスへ移動
ls -l      // 詳細表示
```



https://483398567449.signin.aws.amazon.com/console

https://483398567449.signin.aws.amazon.com/console

