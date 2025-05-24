[![MIT license](https://img.shields.io/static/v1?label=license&message=MIT&color=blue)](https://github.com/jakob-bagterp/index-now-submit-sitemap-action/blob/master/LICENSE.md)
[![Codecov](https://codecov.io/gh/jakob-bagterp/index-now-submit-sitemap-action/branch/master/graph/badge.svg?token=PEGUV7IL8T)](https://codecov.io/gh/jakob-bagterp/index-now-submit-sitemap-action)
[![CodeQL](https://github.com/jakob-bagterp/index-now-submit-sitemap-action/actions/workflows/codeql.yml/badge.svg)](https://github.com/jakob-bagterp/index-now-submit-sitemap-action/actions/workflows/codeql.yml)
[![Test](https://github.com/jakob-bagterp/index-now-submit-sitemap-action/actions/workflows/test.yml/badge.svg)](https://github.com/jakob-bagterp/index-now-submit-sitemap-action/actions/workflows/test.yml)

# 🔍 Automatically Submit Sitemap URLs to IndexNow 🔎
Are you concerned about search engine optimization (SEO)? Do you want to make sure your website is indexed frequently by [Bing](https://www.bing.com/indexnow), [Yandex](https://yandex.com/indexnow), [DuckDuckGo](https://duckduckgo.com/), and other search engines?

This workflow for GitHub Actions will automatically submit your sitemap to IndexNow for faster indexing by Bing, Yandex, DuckDuckGo and other search engines.

Ready to try? Find more information on [GitHub's Marketplace](https://github.com/marketplace/actions/index-now-submit-sitemap-action).

> [!TIP]
> IndexNow requires an API key stored on your website, but how do you keep it secret and secure?
>
> For public repositories, you normally can't hide your IndexNow API key and its location – the file is visible in the repository code and the API key is exposed.
>
> However, with this action, the API key is generated on the fly and cached until the sitemap is successfully submitted and accepted by IndexNow. After that, the file will be removed from the repository.

## How to Use
Example workflow:

```yaml
name: Submit Sitemap URLs to IndexNow

on:
  push:
    branches:
      - master

jobs:
  submit-sitemap:
    runs-on: ubuntu-latest
    steps:
      - name: Submit sitemap URLs to IndexNow
        uses: jakob-bagterp/index-now-submit-sitemap-action@v1
        with:
          host: "example.com"  # Replace with your website's host
          api_key: ${{ secrets.INDEX_NOW_API_KEY }}  # Replace with your IndexNow API key
          api_key_location: "https://jakob-bagterp.github.io/${{ secrets.INDEX_NOW_API_KEY }}.txt"  # Replace with your IndexNow API key location
          sitemap_location: "https://example.com/sitemap.xml"  # Replace with your sitemap location
          endpoint: yandex
```

## Become a Sponsor 🏅
If you find this project helpful, please consider supporting its development. Your donations will help keep it alive and growing. Every contribution, no matter the size, makes a difference.

[Donate on GitHub Sponsors](https://github.com/sponsors/jakob-bagterp)

Thank you for your support! 🙌

## Contribute
If you have suggestions or changes to the module, feel free to add to the code and create a [pull request](https://github.com/jakob-bagterp/index-now-submit-sitemap-action/pulls).

## Report Bugs
Report bugs and issues [here](https://github.com/jakob-bagterp/index-now-submit-sitemap-action/issues).
