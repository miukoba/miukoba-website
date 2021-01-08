---
title: タイトル
date: "2021-01-08T00:00:00Z"
draft: true

---


# 見出し1

あいうえお

## 見出し2

あいうえお

### 見出し3

あいうえお

#### 見出し4

あいうえお

- ひとつめ
- ふたつめ
  - ネスト
- みっつめ

# コード

```ruby
# The Greeter class
class Greeter
  def initialize(name)
    @name = name.capitalize
  end

  def salute
    puts "Hello #{@name}!"
  end
end

# Create a new object
g = Greeter.new("world")

# Output "Hello World!"
g.salute
```


# Twitter埋め込み

{{< tweet 1237977473184194560 >}}


# mermaid

```mermaid
sequenceDiagram
  participant Alice
  participant Bob
  Alice->John: Hello John, how are you?
  loop Healthcheck
      John->John: Fight against hypochondria
  end
  Note right of John: Rational thoughts <br/>prevail...
  John-->Alice: Great!
  John->Bob: How about you?
  Bob-->John: Jolly good!
```

