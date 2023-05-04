[English](README.md) | [中文](README_zh.md)

# Project Introduction
This is my personal blog website, built on Github Pages using the Jekyll Minimal Mistakes theme.

## Implementation Steps
- Create a '<Your-UserName>.github.io' repository.
- Place articles in the _posts/ directory and images in the assets/images/ directory, and upload them all to Github.
- Create a _config.yml file in the root directory, pointing the theme to the Jekyll Minimal Mistakes theme on Github, and correctly configuring the reference path for articles and images.
- Create a Gemfile file in the root directory to install the Ruby environment and plugins required by Jekyll.
- Install necessary tools on the Mac M1 machine and start and access the website locally from the root directory to ensure everything is working properly.
- Push the code to the Github repository after adding new articles to enable the website to be accessed via a remote URL.

## Necessary Tools
I am using a Mac and have installed the following tools:
```
# Install Ruby
brew install ruby

# Install Jekyll
gem install bundler jekyll
```

## How to debug locally
```
# Install dependencies
bundle install

# Start the website
bundle exec jekyll serve

# Access the website
http://127.0.0.1:4000/
```

## Project Structure
```
.
├── Gemfile         # Project dependencies
├── README.md
├── _config.yml     # Theme configuration
├── _data
├── _pages          # Category pages such as TAG & directories
├── _posts          # Personal blog articles
├── _includes       # Store common HTML fragments, this project is used to ensure that your website page title and meta description tags are valid and contain relevant keywords to improve search engine rankings
├── robots.txt      # Tell the search engine which pages can be indexed, and all configurations in this project can be indexed
├── assets          # Static files, including images, etc.
└── index.html
```

## Contact the Author
The theme used in this project:
- https://github.com/mmistakes/minimal-mistakes
- Template reference: https://github.com/mmistakes/mm-github-pages-starter
- https://github.com/mmistakes/so-simple-theme/blob/master/example/_config.yml

Feel free to contact me on Github, Have A Nice Day!