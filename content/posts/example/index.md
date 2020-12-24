---
title: "Example Post"
date: 2020-12-24T10:21:56-05:00
draft: false
---

This is the homepage of the Salisuby AI Lab (SAIL)!

Let's try some \\( \LaTeX \\)! Let \\( f(x) = x^2 \\).
Can we still do nice things with Markdown getting in the way?
How about a sequence: \\( a_n = a_{n-1} + 2 \\).
Hopefully this text renders sanely from here on out... but the syntax highlighting in your editor is probably going crazy by now :)

Time for some inline:
$$ a_n =
\begin{cases}
3 \cdot a_n-2 &\text{ if } n > 2 \\\\
1 &\text{ if } n \leq 2.
\end{cases}
$$

That works fine with the caveat that _all_ backslases get escaped during the process!

Here is the source for the above text (oh yes, check out that sweet syntax highliting!):

```latex
Let's try some \\( \LaTeX \\)! Let \\( f(x) = x^2 \\).
Can we still do nice things with Markdown getting in the way?
How about a sequence: \\( a_n = a_{n-1} + 2 \\).
Hopefully this text renders sanely from here on out... but the syntax highlighting in your editor is probably going crazy by now :)

Time for some inline:
$$ a_n =
\begin{cases}
3 \cdot a_n-2 &\text{ if } n > 2 \\\\
1 &\text{ if } n \leq 2.
\end{cases}
$$
```

And using an image local to this post: ![barrel](barrel_1.jpeg)
This image is local to the `index.md` file for this post and will get compiled into a folder alongside the final html.
Note that the final structure for this post is:
```text
welcome/
  index.md        # contains the header of the post
  barrel_1.jpeg   # the local image resource
```

For reference, the preamble for this page looks like:
```text
---
title: "Example Post"
date: 2020-12-24T10:21:56-05:00
draft: false
---

[ Rest of the post here ]
```

For further reading, check the [Hugo Documentation](https://gohugo.io/content-management/).








