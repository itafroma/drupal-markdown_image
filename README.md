# Markdown Image

Provides shorthand to allow easy use of image fields in Markdown.

## Motivation

The Markdown syntax for images is the following:

```markdown
![image title](image url)
```

In Drupal, knowing the image URL is a difficult prospect because many different
things can act on the image before it's displayed. One example is image styles:
while you might know the original URL, finding out what the image style URL is
can be difficult. Moreover, hard-linking to an image can cause problems if the
image style changes.

## Requirements

* [Drupal 7][1]
* The [Markdown][2] module
* An entity that has an image field and a text field with the Markdown text
  format enabled

## Downloading and installation

### Using [Composer][3] via [Packagist][4]

Add `itafroma/drupal-markdown_image` to your `composer.json`:

```json
{
    "require": {
        "itafroma/drupal-markdown_image": "dev-7.x-1.x"
    }
}
```

Composer's Drupal installer assumes `composer.json` is in your `modules` folder.
If it isn't and you want to install the module somewhere else, use a custom
install path in your `composer.json`:

```json
{
    "extra": {
        "installer-paths": {
            "sites/all/modules/{$name}/": ["type:drupal-module"]
        }
    }
}
```

More information can be found in the
[README for Composer's installers package][5].

### Using Git

Clone the repository into one of your `modules` folders:

```sh
git clone -b 7.x-1.x git@github.com:itafroma/drupal-markdown_image.git markdown_image
```

Once downloaded, install Markdown Image as you would [any other module][6].

## Usage

Use the standard [Markdown syntax for images][7], replacing the URL with the name of
the image field followed by the index of the image:

```markdown
![Image tite](field_image:1)
```

## Copyright and license

Contributors to **Markdown Image** hold copyright to their
[respective contributions][8]. It is licensed via the [GPLv2 only][9]: if you
contribute code, you agree to license your contributions via the same license.

GPLv2-compatible cross-licensing will be considered: please
[create an issue][10]! Due to its reliance on the Drupal API (which is
[GPLv2+][11]), it cannot be cross-licensed with a less restrictive,
non-GPL-compatible license.

The full license can be found in the [LICENSE file][12].

[1]: http://drupal.org/project/drupal "Drupal download page"
[2]: http://drupal.org/project/markdown "Markdown module project page"
[3]: http://getcomposer.org "Composer Dependency Manager for PHP"
[4]: http://packagist.org "Packagist Composer repository"
[5]: https://github.com/composer/installers/blob/master/README.md "composer/installers README"
[6]: https://drupal.org/documentation/install/modules-themes/modules-7 "Installing contributed modules (Drupal 7)"
[7]: http://daringfireball.net/projects/markdown/syntax#img "Markdown Syntax Documentation: Images"
[8]: https://github.com/itafroma/drupal/contributors "Markdown Image contributors"
[9]: http://www.gnu.org/licenses/old-licenses/gpl-2.0.html "GPLv2 license"
[10]: https://github.com/itafroma/drupal-markdown_image/issues "Markdown Image issue queue"
[11]: https://drupal.org/licensing/faq/ "Drupal Licensing FAQ"
[12]: https://github.com/itafroma/drupal-markdown_image/blob/7.x-1.x/LICENSE "LICENSE file"
