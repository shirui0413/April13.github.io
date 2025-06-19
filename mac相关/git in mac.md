

Git に利用者情報登録

```
git config --global user.name "yourname"
git config --global user.email "youremail"

// 設定の確認
cat ~/.gitconfig
```



#### SSHキーにてGithubの接続手順

既存SSHキーを確認する

```
ls -al ~/.ssh
```

#### 新しいSSHキーを生成する

```
ssh-keygen -t ed25519 -C "shirui0413@gmail.com"

参照：https://qiita.com/generosity_hiroto_taniguchi/items/8fcb70b24d4249b3674c
```

