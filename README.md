## Design: Produce a document that shows how to the structure for our site in Hugo. Elements to address in the design
 Folders:

— config
  	— config.toml [contains site url and Hugo related setting]
  	—menus.toml [contains menus]
  	—params.toml [logs etc]

 — content
	— contains markdown files of content pages/blogs etc

— themes 
  — mergebase
	— static 
		css
		js
		images [logs and other images]

## Which pages will to be broken up into sub pages and what mechanism is used to achieve that
		
Can be achieved using 
— Shortcodes [complex  shortcodes not recommend]
—Param (done for homepage) [I’ll recommend this approach already implemented on many sites and works well]
—creating separate markdown file and including in main markdown file  [complex  because of theme layout nested emergents and tabs]


## What will be structure of the content folder be? [high level]
 — content
	—blog
	—pages
	—feared-news
       —products
    

## What does the structure for our blog pages look like?
	— content
		—blog
			—-post-slug
				—index.md
				images
					image.webp
	

## What does the “front matter” look like for pages and blogs? What will the variables be?

For post:
Sample:
content/blog/sca-runtime-protection/index.md
`
title: "Patching takes time, sometimes forever. <br>What can you do now?"
description: This is where MergeBase's SCA Runtime Protection comes in. Java Runtime Protection allows you to block a Java library or a function within it so that it can't
date: 2023-02-20T23:02:46+00:00
author: "shannon-smith"
summary: The majority of software supply chain attacks involve Java-based systems. However, the complexity of third-party libraries, which often make up 80-90% of applications, makes them hard to scan, review and analyze. This is where MergeBase’s Java Runtime Protection comes in as a unique capability in the industry. MergeBase’s SCA Runtime Protection provides visibility into the 
aliases: 
  - /sca-runtime-protection/ # old url for prevent 404
categories: ['Cyber Security']
image: "images/SCA-Runtime-Protection.webp"
`
===========
For pages:
Sample: 
Content/_index.md
 — title
— description

 — and params for page section [added to homepage can check there]

 

## What Is the solution for searching blogs?
To enable searching on a static site, 
We need to first create a JSON search index which acts as a database for your search results. 
From there, we update this JSON search index each time you update/create new pages. 
Then, you access/query the data by Client-Side Search Tool FuseJS or lunr.js
Finally, you display the results on your page.

## What is the solution for SEO? 
 Did some research current available  SEO optimization plug-in for Hugo is “Victor Hugo”
Added to blog page. Victor Hugo will never, ever get built into the public directory of your project.
gets executed only when you are in Hugo's local built-in server
