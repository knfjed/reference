# CSS について

## flexbox

- `flex-direction`
  主軸の方向を指定するもの。
  <https://developer.mozilla.org/ja/docs/Web/CSS/flex-direction>
  1. row（デフォルト）
  2. row-reverse
  3. column
  4. column-reverse

* `justify-content`
  アイテムを主軸に沿って配置する
  <https://developer.mozilla.org/ja/docs/Web/CSS/justify-content>

  1. flex-start（デフォルト）
  2. flex-end
  3. center
  4. space-between
  5. space-around

- `align-items`
  アイテムを交差軸に沿って配置する
  <https://developer.mozilla.org/ja/docs/Web/CSS/align-content>
  1. flex-start
  2. flex-end
  3. center
  4. base-line
  5. stretch（デフォルト）

* `order`
  flex アイテムのデフォルトの order は 0 です。
  したがって 0 より大きい order をもつアイテムは、
  明示的に order を指定されていないアイテムの後ろに表示されます。

  order には負の値を指定することもでき、
  ほかのアイテムはそのままの順序を保ちながら一つのアイテムだけを先頭に表示したい場合になどに有用です。
  先頭に表示したいアイテムに order: -1 を設定することで、
  0 より小さい order のこのアイテムが常に先頭に表示されるようになります。

  以下の例では flexbox を使ってレイアウトをしています。
  HTML の中で指定されている active クラスを別のアイテムに付け替えることで、
  レイアウトの先頭に幅すべてを使って表示されるアイテムを変更することができ、
  残りのアイテムは次の行に表示されるようになります。
  <https://developer.mozilla.org/ja/docs/Web/CSS/CSS_Flexible_Box_Layout/Ordering_Flex_Items>

* `align-self`
  個別のアイテムに設定できるプロパティ。
  align-items と同じ値を受け付ける。（flex-end,center など）

* `flex-wrap`

  1. nowrap: 全てのアイテムは、ひとつの行にフィットします。
  2. wrap: アイテムは他の行へ折り返します。
  3. wrap-reverse: アイテムは逆順になって他の行へ折り返します。

* `flex-flow`
  flex-direction と flex-wrap の二つのプロパティーはよく一緒に使われます。
  そこで、これらを統合するショートハンドプロパティー flex-flow が作られました。
  例：`flex-flow: column wrap;`

* `align-content`
  複数の行が他の行とどう距離を取り広がるのかを指定するのに、
  align-content を使うことができます。

  1. flex-start: 行はコンテナーの上側に詰められます。
  2. flex-end: 行はコンテナーの下側に詰められます。
  3. center: 行はコンテナーの中央に詰められます。
  4. space-between: 行はその間に等しい間隔を空けて表示されます。
  5. space-around: 行はその周囲に等しい間隔を空けて表示されます。
  6. stretch: 行はコンテナーに合うよう引き延ばされます。

  混乱したかもしれませんが、align-content は行間の余白を決めるもので、
  align-items はコンテナーに含まれるアイテム全体としての配置を決めるものです。
  一行だけの場合は align-content は何も効果がありません。
