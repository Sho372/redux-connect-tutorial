# Simple React Todo App

このプロジェクトはReactとReduxを使用したシンプルなTodoアプリケーションです。

## 必要条件

- Node.js (v14.0.0以上)
- npm (v6.0.0以上)

## 使用技術

- React v19.1.0
- Redux v5.0.1
- React Redux v9.2.0
- React Scripts v5.0.1
- classnames v2.5.1

## プロジェクト構成

```
src/
├── components/       # UIコンポーネント
│   ├── AddTodo.js    # 新しいTodoを追加するフォーム
│   ├── Todo.js       # 個々のTodoアイテム
│   ├── TodoList.js   # Todoリスト全体
│   └── VisibilityFilters.js  # フィルタリングUI
├── redux/            # Reduxの状態管理
│   ├── actions.js    # アクションクリエーター
│   ├── actionTypes.js # アクションタイプの定義
│   ├── reducers/     # リデューサー
│   ├── selectors.js  # ステート選択関数
│   └── store.js      # Reduxストア設定
├── App.js            # メインアプリケーションコンポーネント
├── TodoApp.js        # Todo機能のメインコンポーネント
├── index.js          # アプリケーションのエントリーポイント
├── constants.js      # 定数定義
└── styles.css        # スタイル定義
```

## セットアップ

リポジトリをクローンした後、以下の手順でアプリケーションをセットアップしてください。

### 依存関係のインストール

```bash
npm install
```

### 開発サーバーの起動

```bash
npm start
```

このコマンドを実行すると、開発モードでアプリが起動します。  
ブラウザで [http://localhost:3000](http://localhost:3000) を開くとアプリケーションが表示されます。

コードを変更すると、ページは自動的にリロードされます。  
また、コンソールにはlintエラーも表示されます。

### ビルド

```bash
npm run build
```

このコマンドは、本番用のアプリケーションを `build` フォルダにビルドします。  
Reactは本番モードで正しくバンドルされ、最適化されたビルドが生成されます。

ビルドはミニファイされ、ファイル名にはハッシュが含まれます。  
これでアプリケーションをデプロイする準備が整いました！

## 機能

- Todoの追加
- Todoの完了/未完了の切り替え
- フィルタリング（全て、完了済み、未完了）

## Redux Flow

このアプリケーションでは、以下のようなReduxのデータフローを実装しています：

1. ユーザーがUIでアクションを実行（例：Todoの追加）
2. コンポーネントがアクションをディスパッチ
3. リデューサーがアクションに基づいて状態を更新
4. 更新された状態が関連コンポーネントに反映される
