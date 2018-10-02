---
title: How to get your blog started!
tags: blog start github
layout: post
---
## Step 1: Create a Repository

Create Github repository and title it "username.github.io"

Create an `_config.yml` file and give it this content:

```yaml
remote_theme: simple-themes/blank-theme

title: Your Blog's Name
author: username
description: Describe your site
# Link to a profile picture - required
avatar: Put the url of your avatar here
# path to your repository - required
repo: username/username.github.io
# social links - optional
mail:  
twitter_username: 
github_username: username
# theme - fill out if you want to change colors

theme_nav: "#dddddd" # color of the navbar
theme_accent: "#1199ff" # color of links and some other things
theme_tags: "#ee7700" # color of tags on post pages
theme_footer: "#999999" # color of the footer

# Optional config - just for more customization or troubleshooting
# how many posts to show per page
paginate: 15

# change this if you are on a project repo, not a username.github.io repo
# for example, if your repo is hello-world, set this to hello-world
path: 

# Ignore the rest of this file unless you want to change more settings
rss: rss
permalink: /blog/:title/

paginate_path: "/blog/:num/"

sass:
    style: compact

plugins:
 - jekyll-feed
```

> **Protip:** To change the amount of posts that appear per page, change the number on the `paginate: 15` line

> **Troubleshooting:** If some features, like links and comments don't work, try setting the `path: ` field to your repo name (such as `path: hello-world`) and the `repo` field to anything in the repo URL after `https://github.com/` (if your repo url is `https://github.com/simple-themes/blank-theme`, set this to `simple-themes/blank-theme`)

## 2. Set Configuration File

In the file, set the `title`, `description` and `avatar`. Also, replace any instance of `username` with your Github username. If you want to, fill in your usernames for other places, like twitter and email, and fill in the theme colors.

## 3. Add other files

Copy the `index.html`, `style.css` and `404.md` files from [this repo](https://github.com/simple-themes/blank-theme/tree/gh-pages)

## 4. Create a post

Create file called `_posts/YEAR-MONTH-DAY-post-title.md`. Replace the date pieces with the right numbers, and the post title with your title, for example `2018-9-29-hello.md`. At the top of the file, add this:
```yaml
---
title: Post Title (Can have spaces)
tags: tags separated by spaces
layout: post
---
```

Then write the rest of your file in markdown, and commit the file!

## 5. Add pages

If you want an about page, create a file called `about.md`. At the top, put:
```yaml
---
title: About Me
permalink: /about/
layout: default
---
```

You can change either of those fields to make pages other than an about page.

> **Protip:** Set `permalink` to `404.html` to create a custom 404 error page

Then, write the rest of your file in markdown and commit your file.

> **Protip:** Put a new line, `hidefromnav: true` between `layout: default` and `---` to get a page that doesn't appear in the navbar.
