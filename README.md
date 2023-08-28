# academic

This is a fork from the Jekyll theme Github repository that I use for my website. While I edit some things, most of the overall structure is the same, so I am going to keep the README the same with some tweaks in the usage section.

Here's a brief way that I choose to understood all of these filed. The `md` files in the root of the repo are each pages/sections of the website: About, Contact, CV, Posts, Research, and Resources. Each of these pages need to import an html layout to use, which all live under `_layouts/`. Each page/section has its own `html` layout that I populate. Each blog post (which live in `_posts/`) uses `post.html` as the template to use. Each research project explanation (which live in `research`) uses `project.html` as the template to use. Each resource will have all of their related filed under their own file/directory in `resources`. In `data/` are configuration files that make it easy to change to somebody else's. Some of the sites that aren't duplicated and can be done once can be done in markdown and pasted onto an `html` file using `{{ content }}`, but I found more flexibility in using `html` sometimes.

### A Jekyll theme for academia

![Academic Screenshot](https://raw.githubusercontent.com/LeNPaul/academic/gh-pages/screenshot.png)

A Jekyll theme designed for academia, although you can use it for almost any other purpose as well:

* Showcase your research interests, publications, your curriculum vitae, the people in your research group, and your contact information.

* Manage courses that you are teaching.

* Provide updates to your students and faulty.

For a guide on how to deploy a Jekyll site using GitHub Pages, please check out [this article](https://paulle.ca/jekyll-tutorials/deploy-jekyll-site-github-pages).

If you like my work then please consider supporting me with [Ko-fi](https://ko-fi.com/paulle).

## Installation

### Ruby Gem Method

Add this line to your Jekyll site's `Gemfile`:

```ruby
gem "academic-jekyll-theme"
```

And add this line to your Jekyll site's `_config.yml`:

```yaml
theme: academic-jekyll-theme
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install academic-jekyll-theme

## Usage

### Layouts

The following sections describe usage instructions for this Jekyll theme,including available layouts, includes, sass and/or assets.

#### Home

The `_layouts/home.html` layout defines the home page for this theme. An introduction to your research group or to yourself can be provided, along with a list of featured publications. There is also a section for providing any updates through posts placed in the `_posts` directory.

#### About

The `_layouts/about.html` layout can be used to showcase and describe people in your research group. People are defined in the `_data/settings.yml` file, and markdown pages for each person with the `_layouts/page.html` layout can be placed in the `people` directory. 

Since I'm only one person, I change the `people` layout to a simple about section/bio.

#### Research

The `_layouts/research.html` layout can be used to showcase selected publications, or the entire catalogue of publications. Direct links to the paper can be used, or a PDF copy of the paper can be served. Publications are defined in the `_data/research_projects.yml` file, and any PDF files that are served can be placed in the `research` directory. 

I expand this section to let me make research posts about each project.

#### Resources

The `_layouts/resources.html` layout can be used to showcase courses that were taught in the past or are currently being taught. Courses are defined in the `_data/settings.yml` file, and markdown pages for each course with the `_layouts/page.html` layout can be placed in the `resources` directory. Related course material, such as PDF files, can also be placed in the `resources` directory in a subdirectory with the same name as the corresponding course. 

I expanded this section by generalizing `courses` to `resources` so I can place non-class related resources here.

#### CV

The `_layouts/cv.html` layout can be used to showcase a curriculum vitae. The sections of the cv are defined in the `_data/cv` directory, where each section has its own `<section>.yml` file.

#### Contact

The `_layouts/contact.html` layout can be used to provide contact information for the research group or the people that lead the research group. Contact information is defined in the `_data/settings.yml` file.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/LeNPaul/academic. This project is intended to be a safe, welcoming space for collaboration, and contributors are expected to adhere to the [Contributor Covenant](http://contributor-covenant.org) code of conduct.

## Development

To set up your environment to develop this theme, run `bundle install`, then run `bundle exec jekyll serve`, and open your browser at `http://localhost:4000`. This starts a Jekyll server using this theme. Make changes to the pages, documents, data, etc. like normal to test this theme's contents. As you make modifications to this theme the site will regenerate and you should see the changes in the browser after a refresh.

## License

The theme is available as open source under the terms of the [MIT License](https://opensource.org/licenses/MIT).
