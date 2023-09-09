# Nick's Fork of Hugo Winston Theme

Hugo Winston is a bold minimal blogging theme.

Credit to Robert Austin for original theme.

## Theme features

- Posts (Markdown)
- Basic Page (Markdown)
- SCSS (Hugo Pipelines)
- Responsive design
- 100/100 Google Lighthouse speed score
- 100/100 Google Lighthouse SEO score
- 100/100 Google Lighthouse accessibility score
- Google analytics configured in `config.toml`
- Configure GID using env variable HUGO_GOOGLE_ANALYTICS_ID, compatible with Netlify.
- Title, meta description and meta tags automatically generated for every page
- OG Meta data for Facebook and Twitter
- Semantic HTML document structure

## Installation

**1. Install Hugo**

To use this theme you will first need to have Hugo installed. Please follow the official [installation guide](https://gohugo.io/getting-started/installing/)

> ⚠️ **Note:** Check your Hugo version - **Hugo Extended** is required!

This theme uses [Hugo Pipes](https://gohugo.io/hugo-pipes/scss-sass/) to compile SCSS and minify assets which means if you are not using the Hugo extended version this theme will not work. To check your version of Hugo, run `hugo version`. Make sure you see **/extended** after the version number, for example _Hugo Static Site Generator v0.51/extended darwin/amd64 BuildDate: unknown_ You do not need to use version v0.51 specifically, it just needs to have the _/extended_ part.

**2. Create a new Hugo site**

This will create a fresh Hugo site in the folder `mynewsite`.

```
hugo new site mynewsite
```

**3. Install the theme**

Download or git clone this theme into the sites themes folder `mynewsite/themes`. You should end up with the following folder structure `mynewsite/themes/hugo-winston-theme`

```
cd mynewsite
git clone https://github.com/zerostaticthemes/hugo-winston-theme.git themes/hugo-winston-theme
```

**4. Copy the example content**

Copy the entire contents of the `mynewsite/themes/hugo-winston-theme/exampleSite/` folder to root folder of your Hugo site, ie `mynewsite/`. To copy the files using terminal, make sure you are still in the projects root, ie the `mynewsite` folder.

```
cp -a themes/hugo-winston-theme/exampleSite/. .
```

**6. Run Hugo**

After installing the theme for the first time, generate the Hugo site.

You run this command from the root folder of your Hugo site ie `mynewsite`

```
hugo
```

For local development run Hugo's built-in local server.

```
hugo server
```

Now enter [`localhost:1313`](http://localhost:1313) in the address bar of your browser.

# Configuration

### Config options

```toml
# config.toml
[params]
  google_analytics_id = ""
  twitter_handle = "@zerostaticio"
  showAuthorOnHomepage = true
  showAuthorOnPosts = false
  showIntroContentOnHomepage = true
  showPostsOnHomepage = true
  usePaginationOnHomepage = false
  limitPostsOnHomepage = 3 # only used if usePaginationOnHomepage is false
  sortPostsByDateOldestFirst = false
  addDot = true
  addFrame = true
  highlightColor = '#7b16ff'
  baseColor = "#ffffff"
  baseOffsetColor = "#eaeaea"
  headingColor = "#1c1b1d"
  textColor = "#4e5157"
  dotColor = "#7b16ff"
  enableGoogleFonts = true 
  googleFontsUrl = "https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap"
  fontFamilyHeading = "Poppins"
  fontFamilyParagraph = "Helvetica"
  fontFamilyMonospace = "monospace"
```

### Google Analytics

Add your google analytics ID to the `config.toml`

```toml
# config.toml
[params]
  google_analytics_id="UA-132398315-1"
```

### Plausible Analytics

Add your plausible analytics domain to the `config.toml`.
This is `data-domain` in your [tracking script code](https://plausible.io/docs/plausible-script).

```toml
# config.toml
[params]
  plausible_analytics_domain = "example.com"
```
