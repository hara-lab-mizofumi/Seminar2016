#WindowsでCaffeを動かす手順

##Docker の インストールは済んで動作している前提での解説
ユーザフォルダに「docker」というフォルダを作成しておいてください。  
タスクバーのDockerを右クリックし、「Settings」をクリックして「Shared Drive」を開き、  
「C」にチェックをつけて「Apply」を押してDockerの再起動が済んでから次の手順に進んでください。   

###Windows側での操作
Windowsのコマンドプロンプトで次のコマンドを叩いていきます
` docker pull mizofumi0411/seminar2016_complated_trained `

次のコマンドは「/C/Users/ユーザ名/docker」という場所を指定しています。ユーザ名は適時変更してください。
` docker run -it -v /C/Users/mizof/docker:/mnt mizofumi0411/seminar2016_complated_trained `

###Ubuntu側(仮想マシン側)での操作
上のコマンドを叩くと、仮想マシンにログインした状態になります。ログインした状態であれば次のコマンドを順番に叩きます。  
` apt-get install python-pydot `  
` mv /root/caffe/ /mnt/ `  
` echo 'export PYTHONPATH="${PYTHONPATH}:/mnt/caffe/python"' >> ~/.bashrc `  
` source ~/.bashrc `  

以上でCaffeを使用する準備が整いました。
あとは、Caffeをじっくり触ってみましょう。