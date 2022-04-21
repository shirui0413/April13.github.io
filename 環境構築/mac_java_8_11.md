# mac - java - 複数バージョン



1. Javaをダウンロード

   ```
   https://www.oracle.com/java/technologies/downloads/
   ```

   ![image-20220421232456511](https://s2.loli.net/2022/04/21/O5CVM41ALqxKdUe.png)

2. インストール確認

   ```iterm2
   java -version
   ```

   

3. JAVA_HOME設定

   ① profile作成し開く

   ```iterm2
   sudo -i vi /etc/.bash_profile
   ```

   ② iを押して、編集モードに変更、下記内容を入力

   ```vim
   JAVA_8_HOME="/Library/Java/JavaVirtualMachines/jdk1.8.0_331.jdk/Contents/Home"
   JAVA_11_HOME="/Library/Java/JavaVirtualMachines/jdk-11.0.15.jdk/Contents/Home"
   alias jdk8="export JAVA_HOME=$JAVA_8_HOME" #编辑一个命令jdk8，输入则转至jdk1.8
   alias jdk11="export JAVA_HOME=$JAVA_11_HOME" #编辑一个命令jdk11，输入则转至jdk1.11
   export JAVA_HOME
   CLASS_PATH="$JAVA_HOME/lib"
   PATH=".$PATH:$JAVA_HOME/bin"
   ```

   ③ escを押して、:wqを入力して保存

   

4. 設定を有効にする

   ```iterm2
   source /etc/.bash_profile
   ```

   

5. javaバージョンを切り替え

   ```iterm2
   jdk8				// java8を利用
   jdk11				// java11を利用
   ```

   
