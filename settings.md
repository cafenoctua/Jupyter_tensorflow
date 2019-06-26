# コンテナに入る
docker exec -it jupyter_tensorflow /bin/sh -c "[ -e /bin/bash ] && /bin/bash || /bin/sh"

# パスワード設定
- dockerコンテナ内部にexecで入り以下コマンドを実行
``` パスワード設定コマンド
python -c 'from notebook.auth import passwd;print(passwd())'
```

# Jupyter実行
start-notebook.sh \
--NotebookApp.password='sha1:e6256b8f1ca5:865ee064afd6a3090f019a6022c73d85802608c3'