---
title:          "What's Kikofri?"
description:    "Short description of Kikofri"
layout: post
permalink:      /ofri
tag: Kikofri
---

<style>
img {
    width: 120px;
    margin: 3rem auto 0 auto;
}
p.pic {
    margin: auto;
    margin-bottom: 2rem;
    text-align: center;
    font-size: 0.75rem;
}
</style>

![Kikofrieye. Used as default favicon. CC0.](/assets/images/kikofrieye.png)
<p class="pic">Pictured: <em>'Ofri Eyeparchment'</em>. Default
favicon/spokesperson.  (CC0/Public Domain).</p> 


**Kikofri** is a theme for Jekyll that's a fork of the [Kiko theme][1]. Today I'd
say Kikofri is Kiko mangled beyond recognition. It came about because I like my
themes like I like my music: ugly, old and barren. It's an assortment of hacks
filtered through web-design choices from the turn of the millennium.

The theme doesn't use any Google Analytics spyware by default, and it doesn't rely on
Google Fonts API for font rendering and the like. Since I never particularly
liked '[jekyll-seo-tag][2]' there's second-rate implementation of it under
`\_includes/head.html`. Pure `liquid`. Configure it to your liking.

[1]: https://github.com/gfjaru/Kiko
[2]: https://github.com/jekyll/jekyll-seo-tag


### Quirks Mode: [](){:id="micros"}

Kikofri comes with a few _quirks_. Since I'm an old person in a young body my
sense of humor is dry. Therefore I decided to call the quirky [macro][4]-like
thingies 'micros', and thus we use to **`µ`** symbols to use them. (Honestly
they're just liquid filters). They can be found at '[\_layouts/post.html][5]'.

These are:

* **micro-hash**:  
    Produces "Wikipedia-style" reference links:
    - "micro-hash" equals 'left backet' ( **`µ#`** = '**`<sup>[`**' ),
    - "hash-micro" equals 'right bracket' ( **`#µ`** = '**`]</sup>`**' )
            
* **micro-semis**:  
    Produces "Bring Attention To element" tag:
    - "micro-semis" ('**`µ;;`**)' equals '**`<b>`**'
    - "semis-micro" ('**`;;µ`**') equals '**`</b>`**'
            
* **micro-micro** (What a stupid name):  
    Indentation:
    - "micro-micro" ("**`µµ`**") "**`&emsp;`**"

[4]: https://en.wikipedia.org/wiki/Macro_(computer_science)
[5]: https://github.com/kxxvii/Kikofri/blob/master/_layouts/post.html

{% capture motherdemon %}
**Example:** Here comes the stepmother of all demo(n)sµ#[a][reflink]#µ. I
really need to put µ;;emphasis;;µ on the next paragraph.

µµ A paragraph like all others, but this one is mine and it is too long because I
need to put enough letters in here to make sense of indenting it.
{% endcapture %}

{{ motherdemon | replace: 'µ#', '<sup>[' | replace: '#µ', ']</sup>'
| replace: 'µ;;', '<b>' | replace: ';;µ', '</b>'
| replace: "µµ", "&emsp;" }}


Here's how it looks in a source file:

```
Here comes the stepmother of all demo(n)sµ#[a][reflink]#µ. I really
need to put µ;;emphasis;;µ on the next paragraph.

µµ A paragraph like all others... /* And so on */
```

[reflink]: https://en.wikipedia.org/wiki/The_Mother_of_All_Demos

Why use 'micros'? Well, you don't need to. Rip 'em out if you want to. Since
I'm used to ugly stuff I just prefer not to use too many fancy plugins. Take a
look at the reference link especially; '`µ#[a][reflink]#µ`' Ain't it ugly?
***Yes it is***, _and it's awesome_.

Markdown can be pretty awkward too though. Ever tried to wrap all lines at a
specific column no matter the cost because you dislike long lines? Ever done it
while trying to produce a clickable image link _with a caption_? Don't try it.
That's what killed Superman.<style>a.d{color: #fff;font-weight:bold;}a.d:hover
{color:#000;}</style><a class="d"> TWICE!!!</a>?

### Other notes: ###

I've at least _tried_ to take a modular approach. That is to break up the theme
is smaller, more or less  self-contained parts, in the form of 'includes' where
applicable.

There are also a configurable front matter value '`pagin`' which serve as a
switch for this theme's "pagination"/archive feature. The variable '`pagnum`'
can be found under `_default.html`. It decides the number of entries at
`index.html` and the offset in the archive. (Default: 10).

The [archive](/archive) is just a neat list of posts. Since few will write
3048+, it'll do. It's plain HTML/CSS, won't spend a lot of bandwidth.

### Some Poetry: ###

**On a more idealistic note**: I always _hated_ the word "blog". I recognize
one blog and it's [this one][8]. I always prefered the concept of a site,
because it can be anything. A newspaper, an encyclopedia, a collections of
essays or a book. The 'micros' are small and simple hacks to turn a "blog" into
something more than just a "blog".

They are stupid unlikely sequences of symbols to create some neat stuff. While
still sticking to the goal of being ugly and a _"dirty and malnourished jekyll
theme"_ of course.

[8]: https://metroid.fandom.com/wiki/Alpha_Blogg

### What It All Boils Down To: ###

There's no reason to use Javascript or something when you can accomplish the
same things with HTML/CSS.

The thing is: a lot of the things people might want to say, write or show don't
really require all that much. Even if it does it's rarely as much as the first
5 search engine results makes you think.

Kikofri tries to keep it simple, being partly flawed by design, partly flawed
because "we're all human". Looking the way it wants instead of following trends
and it strives to be reasonably easy to modify. Tweaking is learning.

Well, of course you can't turn the world upside down with a theme, but worrying
about your "content", "workflow" and striving to be a automaton spewing out
what amounts to mere fluff, i.e. "content", is useless.

[_Don't call it "content"_][works]. It diminishes your work. It makes you a
commodity and what you create some kind of placeholder waiting to be replaced.

[works]: https://www.gnu.org/philosophy/words-to-avoid.html#Content

Or to quote [Proudhon][prod] who put it so eloquently (replace 'man' with your
proper noun if you want to):

> No extended argument would be required to show that the power to take from a
> man his thought, his will, his personality, is a power of life and death; and
> that to enslave a man is to kill him. Why, then, to this other question: WHAT
> IS PROPERTY! may I not likewise answer, IT IS THEFT...

[prod]: /2016/07/16/example-post.html#theft


### Other Important information...

...usually resides [**HERE**](https://github.com/kxxvii/Kikofri/tree/master).
