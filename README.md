# React の環境設定

React+TypeScript の環境構築を行い、ESLint と Prettier の設定を行いました。

## React 環境構築

1. Node.js のインストール
2. インストールされているかを確認
   `node -v`
3. React 環境のファイルを作成　
   `npx create-react-app {プロジェクト名} --template typescript`
   \*react-app は任意のファイル名
4. バージョンの変更(18 から 17 へ)
   `npm uninstall react react-dom`
   `npminstall(yarn add) react@17.0.2 react-dom@17.0.2`
5. バージョン変更に伴い、index.js の変更。

```index.js
import React from 'react';
import ReactDOMfrom 'react-dom';
import './index.css';import App from './App';
import reportWebVitalsfrom './reportWebVitals';

ReactDOM.render(
    <React.StrictMode>
    <App />
    </React.StrictMode>,
document.getElementById('root')
);
reportWebVitals();
```

6. 作成したファイルへ移動
   `cd react-ts-app`
7. ブラウザでファイルを表示
   `npm start`
8. http://localhost:3000 で React の Top ページが表示されれば環境構築完了

## ESLint の設定

1. ESLint をインストール
   `npm install eslint --save-dev`
2. ESLint の config ファイルの雛形を作成
   `npm init @eslint/config`
3. 対話形式で登録。.eslintrc.js が作成される

## Prettier の設定

1. prettier をインストール
   `npm install --save-dev --save-exact prettier`
2. eslint-config-prettier をインストール
   `npm install --save-dev eslint-config-prettier`
3. ESLint の設定ファイルに prettier 追記（.eslintrc.js）

## VS コードの設定

1. VScode の拡張機能から ESLint と prettier をインストール
2. .vscode → settings.json に設定の記述

## project の使い方

```

git clone https://github.com/aya030/react-ts-app_setting.git
cd react-ts-app_setting
npm install

```

### 参考資料

#### npm で React(TypeScript) に ESLint と Prettier を導入

> https://zenn.dev/nakashi94/articles/f67fa9b54437da
