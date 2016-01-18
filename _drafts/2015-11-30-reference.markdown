---
layout:   post
title:    "Cheatsheet"
date:     2015-11-30
author:   "Dave Anderson"
subtitle: "A markdown reference page"
---

Whoa yeah, blogging. How very 2000's!

I hadn't much considered writing a blog - technical or otherwise - until it was suggested by some colleagues at Recurse Center. Going through [some][rc1] of their [awesome work][rc2] really [inspired me][rc3] and reminded me that I love blogs and that feeling that comes burning through a pile of articles in a finely curated [RSS feed reader][feedly]. I'm reminded specifically that I love blogs that:

* are informative [technically][tech] or [otherwise][non-tech].
* provide you with a [new perspective or appreciation][perspective] for the world around you.
* [amuse][haha], [entertain][entertainment] or fill you with [a sense of wonder][wonder].
* connect you with the [cultural movements][cultural], [trends][trend] or other [happenings][haps] in the internet or community around you.

Hopefully this pile of words will do something along those lines while also helping to cement the knowledge that I'm working to gather and give back to the broader community.

If you have any thoughts or suggestions, don't hesitate at all to [contact me on email][contact-form], [twitter][twitter-url], or any of the various social media buttons below.

[rc1]: http://julia-evans
[rc2]: http://rose-aimes
[rc3]: http://anjana
[feedly]: http://www.feedly.com/
[tech]: http://
[non-tech]: http://
[perspective]: http://
[haha]: http://
[entertainment]: http://
[wonder]: http://
[cultural]: http://
[trend]: http://
[haps]: http://
[contact-form]: /contact.html
[twitter-url]: http://www.twitter.com/dvndrsn/




Blogs to book deals. Blogs immortalized in Hollywood. The Martian, from blog to Hollywood. The romantsized image of the struggling blogger typing away a la [Julia and Julia](http://www.lmgtfy.com/juilia+and+julia). Who knew that it would be me to do this and post things after writing them? But.. there are some really useful things about writing. You can cement your knowledge. You can give back to your community. And also, RSS feeds are still really fun, even after the demise of Google Reader (thanks Feedly for keeping the dream alive).

Who, why - you! to get experience writing, document your knowledge and findings and get exposure.

what when - content & frequency

where how - hosting method and content management

In this post, I'll provide an overview of both hosting methods and ways to manage content for a blog.

The first question to ask yourself is how you want to manage your content. This will drive how you can host your blog.

The traditional way of maintaining blog content is using a Content Management System (CMS) such as WordPress for adding and updating posts and pages. CMS typically provide WYSIWYG admin tools for updating and formatting site content and styling on the font end of the application. This can be really helpful for non-technical people to get involved in maintaining the site.

A increasingly popular method of managing your content is using a static site generator such as Jekyll. A static site generator takes plain text files with minimal markup and converts them into formatted html using templates. For a

* Learn how to use git and github. Git is largely the default version control software to use for software development.
* Learn how to use markdown. Markdown is increasingly popular

However, there are other real reasons to use

# Choosing a blog hosting method.

Hosted, Self-hosted,


## Hosted blog service.

([Blogger](http://www.blogger.com), [WordPress.com](https://wordpress.com/), [Tumblr](http://www.tumblr.com), [Medium](http://www.medium.com))

Twitter, linkedin, google+

## Self-hosted (free).

* [Github Pages](https://pages.github.com/) allows for static content (HTML, CSS) only. Easy to update using Git remote.
* [Heroku](http://www.jamesward.com/2014/09/24/jekyll-on-heroku). More flexible, but also more complicated hosting which allows for static site hosting as well as more complicated server side applications. Updates can also be made using Git remote.
* [OpenShift](https://www.openshift.com/pricing/plan-comparison.html) similar to heroku,
* [CloudCannon](http://cloudcannon.com/) adds 'user friendly' CMS-like features for updating content.

## Self-hosted (paid).

A paid host will get you more flexibility in what kind of features are available for you to use.

Some hosts such as Hostgator You can use CMS and limited

Heroku, AWS and Digital Ocean.

# Content Method

## Blog service

## Content Management System (CMS)

CMS. [WordPress]() [Drupal]()

## Static Site Generator.

More secure, better performance than CMS. Strong separation of content and presentation through use of Markdown. Easy to maintain and edit markdown from offline text editors and tools (plain text!). Flexible styling with free hosting options available.

* Jekyll or Octopress (Ruby).
* Pelican (Python).
* Hexo (JavaScript).
* Hugo (Go).


Hacker friendly [static site generator](https://www.staticgen.com/) for hosting on Github.io (or for self-hosting) [Why static site generators](http://www.smashingmagazine.com/2015/11/modern-static-website-generators-next-big-thing/)


. Do initial setup.
    * [Pre-requisite requirements](http://jekyllrb.com/docs/installation/). Easy to tool such as [RVM](https://rvm.io/rvm/install).
. Choose a theme. A helpful resource is [Jekyll themes](http://jekyllthemes.org/)
. Front matter.
. Write an article.
. Familiarize yourself with markdown. Markdown was created by [John Gruber](http://daringfireball.net/projects/markdown/syntax) in 2004 ([Wiki](https://en.wikipedia.org/wiki/Markdown)). Further revisions of this standard have been implemented since then such as [Kramdown](http://kramdown.gettalong.org/syntax.html) which is used by default in [Jekyll](http://jekyllrb.com/docs/home/).

Markdown vs kramdown
[Kramedown Cheatsheet](http://ricostacruz.com/cheatsheets/kramdown.html)
[Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)


# TODO
Take some the fixed top scroll from here.
[MADness](http://madforjekyll.github.io/)
[Personal](https://github.com/PanosSakkos/personal-jekyll-theme)
Finagle with [CSS syntax](http://www.w3schools.com/css/css_syntax.asp)

# Kramdown

[Cheatsheet](http://ricostacruz.com/cheatsheets/kramdown.html)

## Footnotes

This is some text.[^1]. Other text.[^footnote].

[^1]: Some *crazy* footnote definition.
[^footnote]: Some other footnote definition.

## Abbreviations
This is some text not written in HTML but in another language!

*[another language]: It's called Markdown
*[HTML]: HyperTextMarkupLanguage


## Classes and IDs

A simple paragraph with an ID attribute.
{: #para-one}

> A blockquote with a title
{:title="The blockquote title"}
{: #myid}

* {:.cls} This item has the class "cls"

{:.ruby}
    Some code here

# Markdown

[Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

## Sections

# Header 1 (reserved per Jekyll for 'Title')

## Header 2

### Header 3

#### Header 4

##### Header 5

###### Header 6

Header 1
========

Header 2
--------

## Emphasis

_Italics_ and *also italics*
__bold__ and **also bold**

1. First ordered list item
2. Another item
    * Unordered sub-list.
3. Actual numbers don't matter, just that it's a number
    1. Ordered sub-list
4. And another item.

   You can have properly indented paragraphs within list items. Notice the blank line above, and the leading spaces (at least one, but we'll use three here to also align the raw Markdown).

   To have a line break without a paragraph, you will need to use two trailing spaces.
   Note that this line is separate, but within the same paragraph.
   (This is contrary to the typical GFM line break behaviour, where trailing spaces are not required.)

* Unordered list can use asterisks
- Or minuses
+ Or pluses

## Links

[I'm an inline-style link](https://www.google.com)

[I'm an inline-style link with title](https://www.google.com "Google's Homepage")

[I'm a reference-style link][Arbitrary case-insensitive reference text]

[I'm a relative reference to a repository file](../blob/master/LICENSE)

[You can use numbers for reference-style link definitions][1]

Or leave it empty and use the [link text itself].

URLs and URLs in angle brackets will automatically get turned into links.
http://www.example.com or <http://www.example.com> and sometimes
example.com (but not on Github, for example).

Some text to show that the reference links can follow later.

[arbitrary case-insensitive reference text]: https://www.mozilla.org
[1]: http://slashdot.org
[link text itself]: http://www.reddit.com

Images

Here's our logo (hover to see the title text):

Inline-style:
![alt text](https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 1")

Reference-style:
![alt text][logo]

[logo]: https://github.com/adam-p/markdown-here/raw/master/src/common/images/icon48.png "Logo Title Text 2"

Emphasis
Emphasis, aka italics, with *asterisks* or _underscores_.

Strong emphasis, aka bold, with **asterisks** or __underscores__.

Combined emphasis with **asterisks and _underscores_**.

Strikethrough uses two tildes. ~~Scratch this.~~

Code/syntax
Inline `code` has `back-ticks around` it.


```javascript
var s = "JavaScript syntax highlighting";
alert(s);
```

{% highlight javascript %}
var s = "JavaScript syntax highlighting";
alert(s);
{% endhighlight %}

```python
s = "Python syntax highlighting"
print s
```

{% highlight python %}
s = "Python syntax highlighting"
print s
{% endhighlight %}

```
No language indicated, so no syntax highlighting.
But let's throw in a <b>tag</b>.
```

Colons can be used to align columns.

| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |

There must be at least 3 dashes separating each header cell.
The outer pipes (|) are optional, and you don't need to make the
raw Markdown line up prettily. You can also use inline Markdown.

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

> Blockquotes are very handy in email to emulate reply text.
> This line is part of the same quote.

Quote break.

> This is a very long line that will still be quoted properly when it wraps. Oh boy let's keep writing to make sure this is long enough to actually wrap for everyone. Oh, you can *put* **Markdown** into a blockquote.

Inline HTML
<dl>
  <dt>Definition list</dt>
  <dd>Is something people use sometimes.</dd>

  <dt>Markdown in HTML</dt>
  <dd>Does *not* work **very** well. Use HTML <em>tags</em>.</dd>
  </dl>

Horzontal rule
Three or more...

---

Hyphens

***

Asterisks

___

Underscores

Line breaks
Here's a line for us to start with.

This line is separated from the one above by two newlines, so it will be a *separate paragraph*.

This line is also a separate paragraph, but...
This line is only separated by a single newline, so it's a separate line in the *same paragraph*.
