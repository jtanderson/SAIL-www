# SAIL-www
Salisbury AI Lab Webpage

# Developing

The site uses the [Hugo](https://gohugo.io/) system to generate the content.
After cloning, make sure you download the [Manis](https://github.com/yursan9/manis-hugo-theme) theme submodule in the `themes` directory.
Then you can run the site locally to preview your content with `hugo server -D`.

# Posts

Basic flow to add a post:
- Make a folder with a shortname for your post under the `content/posts` directory
- Add an `index.md` file with the markdown for your post
- If images or other static resources are need them, add them to the same folder of your post and assume the resources will reside in the same place as the page, so use local urls in your markdown.
- See the `example` post in this repository for a concrete example
