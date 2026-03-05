
## requirement

* golang
* [nats-server](https://docs.nats.io/running-a-nats-service/introduction/installation)

## how to use

### 1. Unityにプロジェクト(Unity)を読み込む

シーンを選択する（D-SoSまたはC-SoS）

### 2. nats-serverを起動

``` sh
nats-server
```

### 3. ターミナルで調停アプリケーションを起動
道路の空き状況と道路の利用状況を管理する

D-SoSの場合
``` sh
cd D-SoS/main
```
C-SoSの場合
``` sh
cd C-SoS/main
```
に移動しビルド後、実行
``` sh
go build
./main
```

### 4. UnityのSceneビューで再生

## appendix

### ゴール回数のカウント方法

unityのコンソールで `[Goal]` などでフィルタリングすれば取得できる

**例**

```
[Goal] RM: Purple Goal_count: 1 time[s]: 25.08
[Goal] RM: Green Goal_count: 1 time[s]: 28.28
[Goal] RM: Yellow Goal_count: 1 time[s]: 34.22
```

### 衝突回数のカウント方法

unityのコンソールで `[Collision]` などでフィルタリングすれば取得できる

**例**

```
[Collision] RM: Purple time[s]: 65.22494
[Collision] RM: Yellow time[s]: 65.22494
[Collision] RM: Green time[s]: 65.52103
```

### Githubからのダウンロード法

ローカル環境にダウンロード時：git clone -b ブランチ名 --recurse-submodules URL


### Githubへのアップロード法

```
リモートリポジトリに登録時：
(git remote -v,git branchで要確認　及び　git remote set-url origin <URL>)
①親ディレクトリをgit init 　　　　　　　　　　
②サブモジュールをgit add . 及び　git commit 　　　(git commit -m ""で変更追記が求められる)　　　　　　　
③git push origin　リポジトリ名 (本当にそのリポジトリは存在する？　git checkout -b <ブランチ名> )　　
④親ディレクトリに戻りgit add <git push したいファイル全て>　及び　git commit 　　　　　　　　　　
⑤git remote (add) origin URL 　　　　　　　　　　
⑥git push (-u) origin リポジトリ名
```

### このリポジトリの仕様
道路が故障し、その道路をAgentは通行不可



# editor version

- 2021.3.4f1 (Intel)
- 2022.3.27f1 (macOS)
