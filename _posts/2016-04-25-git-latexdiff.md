---
layout: post
title: "LaTeX 'track changes' and Git"
date: 2016-04-25 14:07
category: Software
---

When submitting revisions, many journals ask for a version of your manuscript
showing the 'track changes' since the originally submitted version.  The
excellent [`git-latexdiff`](https://gitlab.com/git-latexdiff/git-latexdiff)
provides a wrapper around Git and the
[latexdiff](https://www.ctan.org/pkg/latexdiff?lang=en) Perl script. So, if I
know the commit hash of the submitted version I can easily produce a pdf showing
the changes.

There are lots of options for how to format the output; my preferred setup is
something like the command below (to include in the project Makefile):

```Makefile
diff.pdf : paper.tex
  git-latexdiff --bibtex --quiet -t CFONT --main $^ #git_hash_of_submitted_version# HEAD -o $@
```

This produces output looking something like this:

![Example of `git-latexdiff` output](/images/git-latexdiff.png)
