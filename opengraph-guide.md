# Open Graph Guide

This guide provides a detailed explanation of all Open Graph protocol fields and tags used in the `structured-data-examples` repository, specifically within `product-landing.html`, `service-landing.html`, `blog.html`, `tech-blog.html`, and `online-cinema.html`. Open Graph enhances how content is displayed on social media platforms like Facebook and LinkedIn when shared. All descriptions are based on the official [Open Graph documentation](https://ogp.me) (last updated April 2025) and incorporate practical recommendations from platforms like Facebook where applicable. They are designed to be clear, detailed, and useful for beginners, adhering to modern web standards. For `product` type in `product-landing.html`, the `product` namespace (`prefix="og: http://ogp.me/ns# product: http://ogp.me/ns/product#"`) is required in the `<html>` tag. For `video.movie` type in `online-cinema.html`, the `video` namespace (`prefix="og: http://ogp.me/ns# video: http://ogp.me/ns/video#"`) is required in the `<html>` tag.

## Open Graph Tags

- **`og:title`**  
  This tag specifies the title displayed when the content is shared on social media. It should be concise and descriptive, with a recommended length of 60 to 70 characters to avoid truncation. (Used in `product-landing.html`, `service-landing.html`, `blog.html`, `tech-blog.html`)

- **`og:description`**  
  This tag provides a summary of the content for social media sharing. It should be concise, with length varying by platform (e.g., up to 300 characters for optimal display). (Used in `product-landing.html`, `service-landing.html`, `blog.html`, `tech-blog.html`)

- **`og:url`**  
  This tag provides the canonical URL of the page as an absolute URL (e.g., "https://example.com"), ensuring the correct link is shared and indexed by social platforms. (Used in `product-landing.html`, `service-landing.html`, `blog.html`, `tech-blog.html`)

- **`og:type`**  
  This tag defines the content type, informing social media platforms about the nature of the content and influencing the card layout. (Used in `product-landing.html`, `service-landing.html`, `blog.html`, `tech-blog.html`)

- **`og:locale`**  
  This tag specifies the language and region using a code like "en_US" (English, United States) or "ru_RU" (Russian, Russia), based on the IETF language tag standard. It tailors the content presentation to the intended audience. (Used in `product-landing.html`, `service-landing.html`, `blog.html`, `tech-blog.html`)

- **`og:image`**  
  This tag contains the URL of the content’s image. It must be in JPEG, PNG, GIF, or WebP format, with a minimum resolution of 50x50 pixels (recommended 1200x630 with aspect ratio 1.91:1), and a maximum file size of 8MB to ensure fast loading. The image must be publicly accessible without requiring authentication. (Used in `product-landing.html`, `service-landing.html`, `blog.html`, `tech-blog.html`, `online-cinema.html`)

- **`og:image:width`** (Used in `product-landing.html`, `service-landing.html`, `online-cinema.html`)  
  This tag specifies the width of the image in pixels, such as 1200. It provides additional metadata for rendering the image on social platforms.

- **`og:image:height`** (Used in `product-landing.html`, `service-landing.html`, `online-cinema.html`)  
  This tag specifies the height of the image in pixels, such as 630. It complements `og:image:width` for proper image display.

- **`og:image:alt`** (Used in `service-landing.html`, `online-cinema.html`)  
  This tag provides a textual description of the image, such as "PC Repair Service Logo" or "Movie Thumbnail". It improves accessibility for users who cannot view the image.

- **`og:site_name`**  
  This tag identifies the name of the website (e.g., "Amazing Brand", "PC Repair Service", "Blog Name", "Tech Blog"). It helps users recognize the source of the content on social media. (Used in `product-landing.html`, `service-landing.html`, `blog.html`, `tech-blog.html`)

- **`og:price:amount`** (Used in `product-landing.html`)  
  This tag defines the product’s price as a number, such as 2999.99 or 2999. It is crucial for displaying the cost on social media platforms.

- **`og:price:currency`** (Used in `product-landing.html`)  
  This tag specifies the currency using the ISO 4217 standard, such as "RUB". It ensures the price is presented in the correct monetary unit.

- **`og:availability`** (Used in `product-landing.html`)  
  This tag indicates the product’s stock status, with values like "instock" or "outofstock". In `product-landing.html`, it uses "InStock". It informs users whether the item is currently available for purchase.

- **`og:brand`** (Used in `product-landing.html`)  
  This tag specifies the brand name of the product, such as "Amazing Brand". It links the product to its manufacturer for better recognition.

- **`og:sku`** (Used in `product-landing.html`)  
  This tag provides the stock keeping unit (SKU), a unique identifier for the product, such as "12345". It aids in product tracking.

- **`og:product:category`** (Used in `product-landing.html`)  
  This tag categorizes the product, such as "Electronics". It helps social platforms organize and present the content.

- **`og:product:condition`** (Used in `product-landing.html`)  
  This tag indicates the condition of the product, such as "New". It informs users about the state of the item.

- **`article:published_time`** (Used in `blog.html`, `tech-blog.html`)  
  This tag specifies the publication date of the blog post in ISO 8601 format with UTC (e.g., "2025-04-03T10:00:00Z"). It helps social media platforms display the original posting time.

- **`article:modified_time`** (Used in `blog.html`, `tech-blog.html`)  
  This tag indicates the last modification date of the blog post in ISO 8601 format with UTC (e.g., "2025-04-03T12:00:00Z"). It ensures the most recent update is reflected.

- **`article:author`** (Used in `blog.html`, `tech-blog.html`)  
  This tag provides a URL for the blog post’s author, such as "https://example.com/about" in these files. Per the Open Graph standard, it should link to an Open Graph profile (`og:type="profile"`), which `author-profile.html` demonstrates for that same URL. It credits the writer on social media.

- **`article:section`** (Used in `blog.html`, `tech-blog.html`)  
  This tag categorizes the article, such as "Category" or "Code Optimization Techniques". It helps organize content on social platforms.

- **`article:tag`** (Used in `blog.html`, `tech-blog.html`)  
  This tag specifies individual keywords associated with the article, such as "keyword1" or "coding". Multiple `<meta>` tags are used, one for each keyword.

- **`video:actor`** (Used in `online-cinema.html`)  
  This tag specifies an actor appearing in the video, such as "Actor One". Multiple `<meta>` tags are used, one per actor.

- **`video:director`** (Used in `online-cinema.html`)  
  This tag specifies the director of the video, such as "Director Name".

- **`video:duration`** (Used in `online-cinema.html`)  
  This tag specifies the video’s duration in whole seconds, such as 7200 (2 hours).

- **`video:release_date`** (Used in `online-cinema.html`)  
  This tag specifies the release date of the video in ISO 8601 format, such as "2025-04-03".

- **`video:tag`** (Used in `online-cinema.html`)  
  This tag specifies a keyword or genre associated with the video, such as "Action". Multiple `<meta>` tags are used, one per tag.

- **`og:video`** (Used in `online-cinema.html`)  
  This tag provides the URL of the actual video file or player, such as "https://example.com/video.mp4". It requires the `video.movie` type and the `video` namespace declared in the `<html>` tag.

- **`og:video:type`** (Used in `online-cinema.html`)  
  This tag specifies the MIME type of the video referenced by `og:video`, such as "video/mp4".