This is the website for my mother's rental in Martinique.
Powered by [jekyll](http://jekyllrb.com/)

Install
-------
Install [git](http://git-scm.org)

[Install jekyll](https://github.com/mojombo/jekyll/wiki/Install)

[Fork](https://help.github.com/articles/fork-a-repo) the repository

Copy `_config.yml.sample` to `_config.yml`. If you want you can specify your google analytics key

Edit pages under `src/`

To test your changes cd to `villa-martinique/`, run `jekyll --server` and go to http://localhost:4000/

Deploy to Amazon S3
---------
Install [s3cmd](http://s3tools.org/download)

Create a bucket and [use it as a website](http://docs.amazonwebservices.com/AmazonS3/latest/dev/WebsiteHosting.html)

To deploy :

`s3cmd del --recursive --force s3://[bucket name]`

`s3cmd put --recursive _site/ s3://[bucket_name]`

Required Front Matter Properties
--------------------------------
Front matters must contain properties `lang`, `tabs_priority` and `title`

Homepage Snippets
-----------------
Pages whose [front matter](https://github.com/mojombo/jekyll/wiki/YAML-Front-Matter) contains a `homepage_summary` will be added to its language homepage snippets. Snippets are displayed 3 in a row.

Localization
------------
Languages are listed in `_config.yaml`. If you add one, be sure to add its localized name in all other languages.

