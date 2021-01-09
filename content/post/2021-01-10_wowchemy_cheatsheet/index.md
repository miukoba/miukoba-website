---
title: Wowchemy/Hugo/Markdown cheatsheet  
date: "2021-01-10 00:00:00 +0900"
draft: false

---

## はじめに

- 網羅はしておらず、よく使うものだけ。
- 自分用なのもあって、下記が全部混ざっているので、部分的に参考にする方は注意してください（この記事を書いてる現在、ブログはWowchemyで運用しています）
  - markdown
    - [https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
  - Hugo Shortcodes
    - [https://gohugo.io/content-management/shortcodes/](https://gohugo.io/content-management/shortcodes/)
  - Wowchemy Shortcodes
    - [https://wowchemy.com/docs/writing-markdown-latex/](https://wowchemy.com/docs/writing-markdown-latex/)

{{% toc %}}

## 基本

```
※ H1は記事タイトルで使われるので使わない
## Heading 2
### Heading 3
#### Heading 4

Italics with _underscores_.
Bold with **asterisks**.
Combined emphasis with **asterisks and _underscores_**.
Strikethrough with ~~two tildes~~.

Inline `code` has `back-ticks around` it.

> This is a blockquote.
```

## リスト

```
1. First item
2. Another item

- First item
- Another item

- [x] Write math example
- [x] Write diagram example
- [ ] Do something else
```

1. First item
2. Another item

- First item
- Another item

- [x] Write math example
- [x] Write diagram example
- [ ] Do something else

## Footnotes

```
I have more [^1] to say.
[^1]: Footnote example.
```

I have more [^1] to say.
[^1]: Footnote example.

## テーブル

```
Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3
```

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

## 水平線

ここと

***

ここの間に水平線

## リンク

[リンク](https://www.example.com)

```
[リンク](https://www.example.com)
```

[他コンテンツへのリンク]({{< ref "/post/2021-01-10_wowchemy_cheatsheet/index.md" >}})

```
[他コンテンツへのリンク]({{</* ref "/post/2021-01-10_wowchemy_cheatsheet/index.md" */>}})
```

{{% staticref "/post/2021-01-10_wowchemy_cheatsheet/dummy.png" "newtab" %}}Download file{{% /staticref %}}

```
{{%/* staticref "/post/2021-01-10_wowchemy_cheatsheet/dummy.png" "newtab" */%}}Download file{{%/* /staticref */%}}
```

## コードブロック

```ruby
def hi
  puts "Hello World!"
end
```

## 画像(figure)

```
{{</* figure src="./dummy.png" title="Steve Francia" */>}}
```

{{< figure src="./dummy.png" title="画像のタイトル" >}}

```
{{</* figure src="./dummy.png" width="50%" */>}}
```

{{< figure src="./dummy.png" width="50%" >}}

## gist埋め込み

```
{{</* gist miukoba fc3c10a25c1c675c1e97 */>}}
```

{{< gist miukoba fc3c10a25c1c675c1e97 >}}

## Twitter埋め込み

```
{{</* tweet 877500564405444608 */>}}
```

{{< tweet 877500564405444608 >}}

## YouTube埋め込み

```
{{</* youtube w7Ft2ymGmfc */>}}
```

{{< youtube id="w7Ft2ymGmfc" >}}

## 目次

```
{% toc %}
```

## callout

```
{{%/* callout note */%}}
A Markdown callout is useful for displaying notices, hints, or definitions to your readers.
{{%/* /callout */%}}
```

{{% callout note %}} A Markdown callout is useful for displaying notices, hints, or definitions to your readers. {{%/
callout %}}

```
{{%/* callout warning */%}}
Here's some important information...
{{%/* /callout */%}}
```

{{% callout warning %}} Here's some important information... {{% /callout %}}

## 絵文字

https://www.webfx.com/tools/emoji-cheat-sheet/

```
I : heart : Wowchemy : smile :
```

I :heart: Wowchemy :smile:

## diagrams(mermaid.js)

https://mermaid-js.github.io/mermaid/

```mermaid
classDiagram
Class01 <|-- AveryLongClass : Cool
Class03 *-- Class04
Class05 o-- Class06
Class07 .. Class08
Class09 --> C2 : Where am i?
Class09 --* C3
Class09 --|> Class07
Class07 : equals()
Class07 : Object[] elementData
Class01 : size()
Class01 : int chimp
Class01 : int gorilla
Class08 <--> C2: Cool label
```

```mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>John: Hello John, how are you?
    loop Healthcheck
        John->>John: Fight against hypochondria
    end
    Note right of John: Rational thoughts <br/>prevail!
    John-->>Alice: Great!
    John->>Bob: How about you?
    Bob-->>John: Jolly good!
```

## その他

- 開いているページのタイトルとURLをMarkdown形式でコピーするChrome Extension
  - https://chrome.google.com/webstore/detail/copy-title-and-url-as-mar/fpmbiocnfbjpajgeaicmnjnnokmkehil

- ローカルで確認
  - `hugo server -D -F`
    - `-F` 未来時刻の記事を含める
    - `-D` draftを含める
