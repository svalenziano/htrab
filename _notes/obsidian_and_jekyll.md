---
title: Jekyll-Obsidian Workflows
---

> #### About
> This is a meta-note about how to build and test this site.

## links
Here's a wikilink:  [[your-first-note]]
<br>Markdown links don't work: `[your-first-note](your-first-note.md)`

## Testing jekyll site locally
  - `bundle exec jekyll serve -w --force_polling`
  - These might also work:
	  - `bundle exec jekyll serve`
	  - `bundle exec jekyll serve --livereload`
  - Troubleshooting
	- `gem update --system 3.5.13`, make sure gem is up to date
	- `gem update` update the gem local database
	- `gem install wdm`
  - More info: ([SO](https://stackoverflow.com/questions/15723412/jekyll-auto-reloading))

## Obsidian setup
- The Obsidian vault should be setup in the root directory of the Jekyll site
- Settings > Files and Links > Excluded files > ignore Jekyll specific folders like `_includes`.  Keep in mind that these folders will still appear in the Obsidian 'Files' browser.
- Want to setup the vault within the `_notes` folder, and keep images within that notes folder?  I haven't figured out how to successfully link images in a way that works with Jekyll.  From what I can tell, the ruby scripts aren't copying the images into the final static site, though this could probably be reconfigured.

## images
Here's an image:
You must prepend the `/assets/` folder name in order for Jekyll to find it!
`![Some alt text](/assets/pasted_image_test.png)`
![Some alt text](/assets/pasted_image_test.png)

You can't use resizing syntax:
`![Some alt text](/assets/pasted_image_test.png|50)`


