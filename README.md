# Minimal Mistakes remote theme starter

Click [**Use this template**](https://github.com/mmistakes/mm-github-pages-starter/generate) button above for the quickest method of getting started with the [Minimal Mistakes Jekyll theme](https://github.com/mmistakes/minimal-mistakes).

Contains basic configuration to get you a site with:

- Sample posts.
- Sample top navigation.
- Sample author sidebar with social links.
- Sample footer links.
- Paginated home page.
- Archive pages for posts grouped by year, category, and tag.
- Sample about page.
- Sample 404 page.
- Site wide search.

Replace sample content with your own and [configure as necessary](https://mmistakes.github.io/minimal-mistakes/docs/configuration/).

---

## Troubleshooting

If you have a question about using Jekyll, start a discussion on the [Jekyll Forum](https://talk.jekyllrb.com/) or [StackOverflow](https://stackoverflow.com/questions/tagged/jekyll). Other resources:

- [Ruby 101](https://jekyllrb.com/docs/ruby-101/)
- [Setting up a Jekyll site with GitHub Pages](https://jekyllrb.com/docs/github-pages/)
- [Configuring GitHub Metadata](https://github.com/jekyll/github-metadata/blob/master/docs/configuration.md#configuration) to work properly when developing locally and avoid `No GitHub API authentication could be found. Some fields may be missing or have incorrect data.` warnings.





Some info that'll be useful later:

Steps:

1. Install Ruby:
   
   1. Follow steps given here [Installation | Jekyll • Simple, blog-aware, static sites](https://jekyllrb.com/docs/installation/)
   
   2. Check if Ruby is installed by typing ruby -v

2. Install jekyll:
   
   1. In a new command window, type
      
      `gem install jekyll bundler`

Initializing:

1. Create a folder for website, say 'website1'. Navigate to that website

2. To create a gemfile, type bundle init. Within the newly greated gemfile, add `gem "jekyll"`

3. Run the following:
   
   1. `bundle`
   
   2. `bundle add webrick`

4. Create an html file, say `index.html` and save it in the 'website1' folder.

5. Build the site:
   
   1. `jekyll build`
   
   2. `jekyll serve` (or `jekyll serve --livereload` ). Go to `localhost:4000` to see what the website will look like.
