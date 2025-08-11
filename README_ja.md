# Firefox Quietbar

あなたのブラウザの上部には, きっとたくさんの開きっぱなしのタブや拡張機能のアイコンが並んでいることでしょう.
魅力的なアイコンは時に私たちの集中を邪魔します.

`firefox-quietbar` が提供する CSS のスニペットは必要な時にだけ, それらを使えるようにします.

## 導入方法

## 機能

- タブバーとツールバーを隠す
- 上部にホバーまたはアドレスバーなどにフォーカスした際に表示させる

## 他の似た設定と異なるところ

- ツールバーが上に重ねて表示される
- ホバー後, 0.35s 待ってから表示することで誤作動を防ぐ

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
        /* バーが現れる時間 */
}
```

<!-- 
## TODO 
- [x] 各種方法との比較
- [x] 変数を用意し, カスタマイズ性を上げる
- [ ] 設定用スクリプト
- [ ] navbar から出たペインにホバー時

-->
