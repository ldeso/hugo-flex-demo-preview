---
author: Hugo Authors
title: Math Typesetting
date: 2019-03-08
description: A brief guide to setup KaTeX
math: true
---

Mathematical formulas written in LaTeX notation can be rendered to HTML on the client side by bundling the [KaTeX](https://katex.org/) library with the website.<!--more-->
Rendering can take place either globally, or in specific locations using a built-in shortcode.

1. Math can be rendered globally or on a per-page basis by setting the `math` parameter to `true` in the site configuration or on specific pages, and by [enabling the passthrough extension](https://gohugo.io/content-management/mathematics/) in the site configuration.

2. If the `math` parameter is set to `false`, mathematical formulas can still by rendered by surrounding them with the `math` shortcode:

    ```
    {{%/* math */%}}
    Inline formulas such as $y=ax+b$ are supported, displayed formulas as well:

    $$e^{i\pi}+1=0$$
    {{%/* /math */%}}
    ```

As of 2024, it is [not yet possible](https://github.com/gohugoio/hugo/issues/10044) to render math on the server side with Hugo.

**Note:** Use the online reference of [Supported TeX Functions](https://katex.org/docs/supported.html)

### Examples

Inline math: $\varphi = \dfrac{1+\sqrt5}{2}= 1.6180339887…$

Block math:
$$
 \varphi = 1+\frac{1} {1+\frac{1} {1+\frac{1} {1+\cdots} } } 
$$
