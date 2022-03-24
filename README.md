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

In order to use a specific theme, one may use the remote theme option (in which one tells the server to use the theme files stored in a GitHub repository maintaned by developers), or install a theme. I found the latter to be more suitable, since I wanted to make my own changes to the theme I was planning to use. (It is possible to make changes even in the remote theme option, but there is a risk of something breaking if the remote repository becomes incompatible with the changes you make.)

Here are the steps I followed:

1. Create my website repository (`pratiksathe.github.io`)

2. Copy all the files from the `Minimal Mistakes` repository into this repository.

3. In cmd, do `bundle`, `bundle add webrick`, `bundle update` and `bundle install`.

4. Do `bundle exec jekyll serve --livereload`. Go to `localhost:4000` in a browser. Making any changes in the folder will be reflected immediately in the browser.

5. Make the changes you want, such as editing or adding posts and pages. If you want to make changes to the theme, make appropriate edits to the sass, layout files etc.

6. If it all looks good at `localhost:4000` commit and push changes.

After doing all this, the website will be available at `username.github.io`.

In order to host the website on GitHub after buying a domain from Google domains, follow the instructions here [link](https://dev.to/trentyang/how-to-setup-google-domain-for-github-pages-1p58).
