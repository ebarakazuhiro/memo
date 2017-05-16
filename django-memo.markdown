# Djangoに関するメモ

## virtualenvのセットアップ手順


virtualenvはPythonのいろいろな実行環境を仮想的に提供する仮想環境です。

### pythonzインストール

```

## インストール
curl -kL https://raw.github.com/saghul/pythonz/master/pythonz-install | bash

```

```

## zshrc 設定追加 (bash なら bashrc)
echo "[[ -s $HOME/.pythonz/etc/bashrc ]] && source $HOME/.pythonz/etc/bashrc" >> ~/.zshrc

```

```

## python インストール
pythonz install <version>

pythonz list

```


### virtualenv & virtualenvwrapper インストール


```

## pipインストール
sudo easy_install pip

```

```

## virtualenv & virtualenvwrapper イントール
sudo pip install virtualenv virtualenvwrapper

```


```

## zshrc 設定追加 (bash なら bashrc)
cat << EOF >> ~/zshrc
source `which virtualenvwrapper.sh`
export WORKON_HOME=$HOME/.virtualenvs
export PIP_RESPECT_VIRTUALENV=true
EOF

```

```

## スクリプトファイルを実行
source ~/.zshrc

```

```

## 指定の Python version で仮想環境作成
mkvirtualenv -p $HOME/.pythonz/pythons/CPython-<version>/bin/python venv

```


## QuerySet

QuerySetの確認は[こちら](http://docs.djangoproject.jp/en/latest/ref/models/querysets.html#django.db.models.query.QuerySet.get)


## modelのテスト


テストコードの確認は以下のスクリプトを実行


```

## テストコードの確認
python manage.py test

## 特定のディレクトリ内のテストコードの確認
python manage.py test ディレクトリ名

```

## 参照

・Django ドキュメント [https://docs.djangoproject.com/ja/1.11/](https://docs.djangoproject.com/ja/1.11/)


・Django チュートリアル [http://qiita.com/gcfuji/items/bff55a0b8ae1b76c0ca1](http://qiita.com/gcfuji/items/bff55a0b8ae1b76c0ca1)


・Django チートシート [https://ehmatthes.github.io/pcc/cheatsheets/README.html](https://ehmatthes.github.io/pcc/cheatsheets/README.html)