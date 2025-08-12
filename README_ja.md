# Firefox Quietbar

あなたのブラウザの上部には, きっとたくさんの開きっぱなしのタブや拡張機能のアイコンが並んでいることでしょう.
魅力的なアイコンは時に私たちの集中を邪魔します.

`firefox-quietbar` が提供する CSS のスニペットは必要な時にだけ, それらを使えるようにします.

https://github.com/user-attachments/assets/b29263d7-dcc4-4282-99cc-04526b3c1c97

## 導入方法

1. アドレスバーから `about:config` を開き, `toolkit.legacyUserProfileCustomizations.stylesheets` を `true` にする
2. アドレスバーから `about:profiles` を開き, 使用中のプロファイルに設定されているディレクトリを確認する
3. 確認したディレクトリに `chrome` というディレクトリを作る
4. そこにこのリポジトリの `userChrome.css` を配置する
5. Firefox を再起動する

## 機能

- タブバーとツールバーを隠す
- 上部にホバーまたはアドレスバーなどにフォーカスした際に表示させる

- 他の似た設定と異なるところ
    - ツールバーがコンテンツ全体の上に重ねて表示される
    - ホバー後, 少し待ってから表示することで誤作動を防ぐ

### 似たことができる設定一覧

- 全画面表示（F11キー）
- アドオン [New window without toolbar](https://addons.mozilla.org/en-US/firefox/addon/new-window-without-toolbar/)
- [UserChrome-Tweaks/navbar@Timvde](https://github.com/Timvde/UserChrome-Tweaks/tree/master/navbar)
- [firefox-autohide-navbar@3ae3ae](https://github.com/3ae3ae/firefox-autohide-navbar/tree/main)

## カスタマイズ

`userChrome.css` の冒頭にかいてある, 以下の変数の値を編集することで挙動を変更できる:

```css
:root {
    --navbar-hover-area-height: 25px; 
        /* Height of the hover area that triggers the navbar to appear */
        /* バーの表示のきっかけとなるエリアの高さ */
    --navbar-show-delay: 0.35s;
        /* Delay before navbar appears on hover */
        /* ホバーしてから現れるまでの遅れ */
    --navbar-transition-duration: 0.3s;
        /* Duration of transition ease-in-out */
        /* バーが現れるのにかかる時間 */
}
```

<!-- 
## TODO 
- [x] 各種方法との比較
- [x] 変数を用意し, カスタマイズ性を上げる
- [x] 全画面にした時, ホバーエリアを消す
- [ ] 設定用スクリプト
- [ ] navbar から出たペインにホバー時

-->
