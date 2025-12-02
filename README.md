# README.md

# Structured Data Examples

This repository provides practical examples of structured data markup using [Schema.org](https://schema.org) and [Open Graph](https://ogp.me/) protocols. These examples are designed to help developers implement structured data on their websites to improve search engine optimization (SEO), enable rich snippets in search results, and enhance social media sharing.

## Table of Contents

- [Introduction](#introduction)
- [Included Files](#included-files)
  - [Product Landing Page](#product-landing-page)
  - [Service Landing Page](#service-landing-page)
  - [Blog Article Page](#blog-article-page)
  - [Tech Blog Article Page](#tech-blog-article-page)
  - [Online Cinema Page](#online-cinema-page)
- [Usage](#usage)
- [Validation](#validation)
- [Resources](#resources)

## Introduction

Structured data markup helps search engines and social platforms understand the content of web pages more effectively. By implementing Schema.org and Open Graph protocols, developers can:
- Boost SEO with rich snippets (e.g., product prices, ratings, or business details in search results).
- Ensure proper rendering of shared links on platforms like Facebook, Twitter, and LinkedIn.

This repository contains three example files demonstrating structured data for common use cases: a product landing page, a service landing page, and a blog article page.

## Included Files

### Product Landing Page

- **File**: `product-landing-page.html`
- **Description**: This example showcases structured data for an e-commerce product page using Schema.org `Product` type and Open Graph's `product` type.
- **Key Features**:
  - **Schema.org**: Includes product details such as name, image, description, brand, SKU, offers (with pricing and availability), shipping details, return policy, and reviews.
  - **Open Graph**: Uses `og:type="product"` with properties like `og:price:amount`, `og:price:currency`, and `og:brand`.
- **Use Case**: Perfect for online stores or product-focused landing pages aiming to display rich snippets and improve social sharing.

### Service Landing Page

- **File**: `service-landing-page.html`
- **Description**: This example demonstrates structured data for a local service provider (e.g., computer repair) using Schema.org `LocalBusiness` type and Open Graph's `website` type.
- **Key Features**:
  - **Schema.org**: Provides business details like name, address, phone, email, opening hours, services offered, pricing range, and customer reviews.
  - **Open Graph**: Uses `og:type="website"` with general metadata such as title, description, and image.
- **Use Case**: Ideal for local businesses or service providers looking to enhance local SEO and social media visibility.

### Blog Article Page

- **File**: `blog.html`
- **Description**: This example demonstrates structured data for a blog article using Schema.org `BlogPosting` type and Open Graph's `article` type.
- **Key Features**:
  - **Schema.org**: Includes article details such as headline, description, publication and modification dates, author information, main image, and keywords. Additionally, it features a `BreadcrumbList` for navigation.
  - **Open Graph**: Uses `og:type="article"` with properties like `og:title`, `og:description`, `og:image`, and article-specific tags such as `article:published_time` and `article:author`.
- **Use Case**: Ideal for blogs or content-heavy websites aiming to improve SEO, display rich snippets (e.g., publication date, author), and ensure proper social media sharing.

### Tech Blog Article Page

- **File**: `tech-blog.html`
- **Description**: This example demonstrates structured data for a technical blog article using Schema.org `TechArticle` type and Open Graph's `article` type.
- **Key Features**:
  - **Schema.org**: Includes technical article details such as headline, description, publication and modification dates, author information, main image, keywords, proficiency level, dependencies, and audience. Additionally, it features a `BreadcrumbList` for navigation.
  - **Open Graph**: Uses `og:type="article"` with properties like `og:title`, `og:description`, `og:image`, and article-specific tags such as `article:published_time` and `article:author`.
- **Use Case**: Ideal for technical blogs or educational websites targeting developers, aiming to improve SEO, display rich snippets (e.g., publication date, author), and enhance social media sharing.

### Online Cinema Page

- **File**: `online-cinema.html`
- **Description**: This example demonstrates structured data for an online cinema page featuring a movie, using Schema.org `Movie` and `VideoObject` types, along with Open Graph's `video.movie` type.
- **Key Features**:
  - **Schema.org**: Includes movie details such as name, description, actors, director, duration, ratings, reviews, and a nested `VideoObject` with video-specific properties like thumbnail, upload date, and interaction statistics. It also features a `BreadcrumbList` for navigation.
  - **Open Graph**: Uses `og:type="video.movie"` with properties like `og:title`, `og:description`, `og:image`, and video-specific tags such as `video:actor`, `video:director`, and `video:duration`.
- **Use Case**: Ideal for online cinema or streaming websites aiming to enhance SEO with rich video snippets, improve discoverability, and optimize social media sharing.

## Usage

To use these examples:
1. Clone or download this repository: 
```zsh
   git clone https://github.com/theEvilGrinch/structured-data-examples.git  
```
2. Open the HTML files in a text editor or browser to review the markup.
3. Customize the structured data by replacing placeholder values (e.g., URLs, names, prices) with your own content.
4. Embed the modified markup into the `<head>` section of your web page.

## Validation

After implementing the structured data, validate it using these tools:
- **[Google Rich Results Test](https://search.google.com/test/rich-results)**: Checks Schema.org markup for errors and eligibility for rich snippets.
- **[Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)**: Verifies Open Graph metadata for social media sharing.
- **[Twitter Card Validator](https://cards-dev.twitter.com/validator)**: Ensures Twitter Card markup works correctly.

Test your pages to resolve any warnings or errors before deployment.

## Resources

Additionally, refer to the following guides for detailed explanations of the fields and tags used in this repository:
- **[Schema.org Guide](schema-guide.md)** - Details on Schema.org fields.
- **[Open Graph Guide](opengraph-guide.md)** - Details on Open Graph tags.
- **[Twitter Cards Guide](twitter-cards-guide.md)** - Details on Twitter Card tags.

For more details on the structured data protocols used in these examples, explore the official documentation:
- **[Schema.org](https://schema.org)** - Comprehensive vocabulary for structured data markup.
- **[Open Graph](https://ogp.me/)** - Protocol for enhancing social media sharing.
- **[Twitter Cards](https://developer.twitter.com/en/docs/twitter-for-websites/cards)** - Twitter-specific markup for rich media previews.

## ⚖️ License

MIT Licensed - See [LICENSE](LICENSE) for details.
