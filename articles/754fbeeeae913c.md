---
title: "連続した文字列を取得したい時"
emoji: "🉑"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["ruby"]
published: true
---

正規表現とかのテストで連続した文字列が欲しい

ので、rubyでコピペ用

unicode表

https://www.unicode.org/charts/

## アルファベット

```ruby
("a".."z").inject {|r, i| r + i}
```

## アルファベット大文字

```ruby
("A".."Z").inject {|r, i| r + i}
```

## 全角アルファベット

```ruby
("ａ".."ｚ").inject {|r, i| r + i}
```

## 全角アルファベット大文字

```ruby
("Ａ".."Ｚ").inject {|r, i| r + i}
```

## 数字
```ruby
("0".."9").inject {|r, i| r + i}
```

## 全角数字

```ruby
 ("０".."９").inject {|r, i| r + i}
```

## ひらがな

```ruby
("\u3041".."\u3096").inject {|r, i| r + i}
```

## カタカナ

```ruby
("\u30A1".."\u30FA").inject {|r, i| r + i}
```

## 半角カタカナ

半角長音含む

```ruby
("ｦ".."ﾝ").inject {|r, i| r + i}
```
