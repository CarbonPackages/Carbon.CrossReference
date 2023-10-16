# CrossReference for the Neos CMS

Helper package to manage Node cross references (bidirectional references) in your Neos CMS project

## Installation

```bash
composer require carbon/crossreference
```

## Usage

Configure in your `Settings.yaml` which files should be cross-referenced.

```yaml
Carbon:
  CrossReference:
    presets:
      Vendor.Articles:Category:
        enabled: true
        mapping:
          - Vendor.Articles:Document.Item: category
          - Vendor.Articles:Document.Category: articles
      Vendor.Articles:Author:
        enabled: true
        mapping:
          - Vendor.Articles:Document.Item: authors
          - Vendor.Articles:Document.Author: articles
```

## Acknowledgments

This package is mainly a for of [ttreeagency/CrossReference], as this packages gets no updates since a long time.
[Dominique], thank you for all your work! :heart:
This package include the work from [David Spiola], to make this run under Neos 7 - 8.

Development sponsored by [ttree ltd - neos solution provider].

## License

Licensed under MIT, see [LICENSE](LICENSE)

[ttreeagency/CrossReference]: https://github.com/ttreeagency/CrossReference
[Dominique]: https://github.com/dfeyer
[ttree ltd - neos solution provider]: http://ttree.ch
[David Spiola]: https://github.com/davidspiola
