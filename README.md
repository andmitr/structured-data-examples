# Structured Data Examples

This repository provides practical examples of structured data markup using [Schema.org](https://schema.org) and [Open 
Graph](https://ogp.me/) protocols, helping developers improve SEO, enable rich snippets in search results, and enhance social media sharing. 

[![License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square&logo=opensource)](LICENSE)

## Table of Contents

- [Introduction](#introduction)
- [Included Files](#included-files)
  - [Product Landing Page](#product-landing-page)
  - [Service Landing Page](#service-landing-page)
  - [Blog Article Page](#blog-article-page)
  - [Tech Blog Article Page](#tech-blog-article-page)
  - [Online Cinema Page](#online-cinema-page)
  - [Author Profile Page](#author-profile-page)
  - [Software Review Page](#software-review-page)
- [Usage](#usage)
- [Validation](#validation)
- [Resources](#resources)
- [License](#license)

## Introduction

Structured data markup helps search engines and social platforms understand the content of web pages more effectively. By implementing Schema.org and Open Graph protocols, developers can:
- Boost SEO with rich snippets (e.g., product prices, ratings, or business details in search results).
- Ensure proper rendering of shared links on platforms like Facebook, X (Twitter), and LinkedIn.

This repository contains seven example files demonstrating structured data for common use cases: a product landing page, a service landing page, a blog article page, a tech blog article page, an online cinema page, an author profile page, and a software review page.

## Included Files

Each file is a self-contained HTML example with Schema.org and Open Graph markup in the `<head>` section.

### [Product Landing Page](product-landing.html)

An e-commerce product page with full offer markup: pricing, shipping, return policy, seller details, and customer reviews. Helps online stores display rich product snippets in search results and optimize social sharing.

### [Service Landing Page](service-landing.html)

A local service business page with location, opening hours, service offerings, pricing, area served, and reviews. Designed for local businesses looking to enhance search visibility and social media presence.

### [Blog Article Page](blog.html)

A standard blog article with author info, publication dates, keywords, and breadcrumb navigation. A baseline example for content-heavy websites aiming to display rich article snippets.

### [Tech Blog Article Page](tech-blog.html)

A technical article or tutorial that extends the blog example with proficiency level, dependencies, and target audience. Aimed at educational and developer-focused content.

### [Online Cinema Page](online-cinema.html)

A movie page combining `Movie` and `VideoObject` markup: cast, ratings, reviews, video playback metadata, and interaction statistics. Built for streaming platforms and video-centric websites.

### [Author Profile Page](author-profile.html)

An author's profile or about page using `ProfilePage` markup. Links to published articles, enabling Google's Profile Page appearance. Useful for blog networks and personal branding.

### [Software Review Page](software-review.html)

An editorial software review with ratings, pros and cons lists, FAQ section, and breadcrumb navigation. Designed for independent review articles and affiliate content aiming for Google's review rich result.

## Usage

To use these examples:
1. Clone or download this repository: 
```zsh
git clone https://github.com/andmitr/structured-data-examples.git
```
2. Open the HTML files in a text editor or browser to review the markup.
3. Customize the structured data by replacing placeholder values (e.g., URLs, names, prices) with your own content.
4. Embed the modified markup into the `<head>` section of your web page.

## Validation

After implementing the structured data, validate it using these tools:
- **[Google Rich Results Test](https://search.google.com/test/rich-results)**: Checks Schema.org markup for errors and eligibility for rich snippets.
- **[Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)**: Verifies Open Graph metadata for social media sharing.
- **Twitter Card validation**: X (Twitter) no longer provides a public Card Validator. To verify Twitter Card markup, post a tweet containing your URL and check the card preview.

## Resources

Additionally, refer to the following guides for detailed explanations of the fields and tags used in this repository:
- **[Schema.org Guide](schema-guide.md)** - Details on Schema.org fields.
- **[Open Graph Guide](opengraph-guide.md)** - Details on Open Graph tags.
- **[Twitter Cards Guide](twitter-cards-guide.md)** - Details on Twitter Card tags.

For more details on the structured data protocols used in these examples, explore the official documentation:
- **[Schema.org](https://schema.org)** - Comprehensive vocabulary for structured data markup.
- **[Open Graph](https://ogp.me/)** - Protocol for enhancing social media sharing.


## License

MIT Licensed. See [LICENSE](LICENSE) for details.
