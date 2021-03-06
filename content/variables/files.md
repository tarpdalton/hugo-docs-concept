---
title: File Variables
linktitle:
description: Hugo provides the ability to traverse your website's files on your server, including the local Hugo server.
date: 2017-02-01
publishdate: 2017-02-01
lastmod: 2017-02-01
categories: [variables and params]
tags: [files]
draft: false
menu:
  main:
    parent: "Variables"
    weight: 40
weight: 40
sections_weight: 40
aliases: [/variables/file-variables/]
toc: false
---

Hugo provides the ability to traverse your website's files on your server, including the local `Hugo server`. You can access file-system-related data for a piece of content via the `.File` variable.

{{% note "Rendering Local Files" %}}
For information on creating shortcodes and templates that tap into Hugo's file-related feature set, see [Local File Templates](/templates/files/).
{{% /note %}}

The `.File` object contains the following fields:

`.File.Path`
: the original relative path of the page (e.g., `content/posts/foo.en.md`)

`.File.LogicalName`
: the name of the content file that represents a page (e.g., `foo.en.md`)

`.File.TranslationBaseName`
: the filename without extension or optional language identifier (e.g., `foo`)

`.File.BaseFileName`
: the filename without extension (e.g., `foo.en`)

`.File.Ext`
: the file extension of the content file (e.g., `md`); this can also be called using `.File.Extension` as well. Note that it is *only* the extension without `.`.

`.File.Lang`
: the language associated with the given file if Hugo's [Multilingual features][multilingual] are enabled (e.g., `en`)

`.File.Dir`
: given the path `content/posts/dir1/dir2/`, the relative directory path of the content file will be returned (e.g., `posts/dir1/dir2/`)

[Multilingual]: /content-management/multilingual/