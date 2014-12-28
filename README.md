woodpecker
==========

![](https://camo.githubusercontent.com/4eebfbf006d6deffc7b0b373314f1feee374cb01/687474703a2f2f75706c6f61642e77696b696d656469612e6f72672f77696b6970656469612f636f6d6d6f6e732f7468756d622f622f62662f446f776e795f576f6f647065636b65722d46656d616c652e6a70672f33353870782d446f776e795f576f6f647065636b65722d46656d616c652e6a7067)

Interactive scraping interface in CLI

```sh
woodpecker> https://github.com/kaiinui/woodpecker
Fetched https://github.com/kaiinui/woodpecker
woodpecker> .pagehead
[1] kaiinui (.author > a > span)
[2] woodpecker (strong.js-current-repository)
woodpecker> 1
.pagehead .author > a > span
```

Features
---

### Drill Down

```
woodpecker> .pagehead
[1] kaiinui (.author > a > span)
[2] woodpecker (strong.js-current-repository)
woodpecker> 1
.pagehead .author > a > span
```

### Search

```
woodpecker> search kaiinui
[1] kaiinui (.pagehead .author > a > span)
woodpecker> 1
.pagehead .author > a > span
```

### List

```
woodpecker> list
[1] kaiinui / woodpecker (.entry-title.public)
[2] Unwatch / Star / Fork (.pagehead-actions)
```

Advanced Features
---

### Extract the body

Infer body location by heuristics rule.

```
woodpecker> body
Interactive Scraping tool .... terface in CLI

article.markdown-body.entry-content > p
```

### Statistic based sort

Sort `list` result with word statistic. Frequently used words have low priority.
