---
title: urls.Anchorize
description: Returns the given string, sanitized for usage in an HTML id attribute.
categories: []
keywords: []
params:
  functions_and_methods:
    aliases: [anchorize]
    returnType: string
    signatures: [urls.Anchorize INPUT]
aliases: [/functions/anchorize]
---

{{% include "/_common/functions/urls/anchorize-vs-urlize.md" %}}

## Sanitizing logic

With the default Markdown renderer, Goldmark, the sanitizing logic is controlled by your site configuration:

{{< code-toggle file=hugo >}}
[markup.goldmark.parser]
autoHeadingIDType = 'github'
{{< /code-toggle >}}

This controls the behavior of the `anchorize` function and the generation of heading IDs when rendering Markdown to HTML.

Set `autoHeadingIDType` to one of:

github
: Compatible with GitHub. This is the default.

github-ascii
: Similar to the `github` setting, but removes non-ASCII characters.

blackfriday
: Provided for backwards compatibility with Hugo v0.59.1 and earlier. This option will be removed in a future release.
