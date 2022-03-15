# How to Use

1. Place `seo.liquid` in `_includes`.
2. Place `include seo.liquid` in your HTML head. (Note that the title and meta charset tag are already included in here.)
3. Place `metadata.yml` in `_data`
4. Reference variables in `metadata.yml` as site.data.metadata.{prop} 

## Front Matter
To handle SEO on a per-page basis, use front-matter formatted in the following way:

```yml
author: Daniel Hernandez
seo:
  meta:
    robots: "index, dofollow" #you don't have to set *every* variable
                              #for example, you can just rely on your global fall back if 
                              #every page is gonna be indexable.
  og:
    title: Building a Jekyll site in the 20s
    description: How hard is it to build and deploy a Jekyll website nowadays? Read to learn more about an exploration of the static site generator.
    type: article #on articles or different content types. check https://ogp.me// for specific documentation
    image: https://imagedelivery.net/fDayHQi5y0lm6y93ekDYPw/895849c8-9d8c-4279-ee9a-3a4a2814c000/public
tags:
  - jekyll
  - jamstack
  - static sites
```
Not every tag is implemented but it includes most use cases:

```yml
image: #this can be used as an alternative to the og.image. you don't need both.
seo:
  meta:
    robots: #check mdn for values: https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta/name 
    revisit:
    author:
    keywords: #not really used by search engines anymore, but included if you still want 
    #to fill it out. If it's' null in the data file and on the page, the tag won't be rendered.
  og: #https://ogp.me// for values
    title:
    description:
    type:
    image: 
    locale:
    site_name:
```