---
title: replacere
linktitle: replaceRE
description: Replaces all occurrences of a regular expression with the replacement pattern.
godocref:
date: 2017-02-01
publishdate: 2017-02-01
lastmod: 2017-02-01
categories: [functions]
tags: [regex]
ns:
signature: ["replaceRE PATTERN REPLACEMENT INPUT"]
workson: []
hugoversion:
relatedfuncs: []
deprecated: false
aliases: []
---

Replaces all occurrences of a regular expression with the replacement pattern.

```golang
{{ replaceRE "^https?://([^/]+).*" "$1" "http://gohugo.io/docs" }}` → "gohugo.io"
{{ "http://gohugo.io/docs" | replaceRE "^https?://([^/]+).*" "$1" }}` → "gohugo.io"
```

{{% note %}}
Hugo uses Golang's [Regular Expression package](https://golang.org/pkg/regexp/), which is the same general syntax used by Perl, Python, and other languages but with a few minor differences for those coming from a background in PCRE. For a full syntax listing, see the [GitHub wiki for re2](https://github.com/google/re2/wiki/Syntax).
{{% /note %}}
