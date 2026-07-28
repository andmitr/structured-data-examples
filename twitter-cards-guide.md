# Twitter Cards Guide

This guide provides a detailed explanation of all Twitter Card fields and tags used in the `structured-data-examples` repository. Twitter Cards enhance the presentation of shared content on Twitter, such as displaying images or summaries. All descriptions are based on the official [Twitter Cards documentation](https://developer.twitter.com/en/docs/twitter-for-websites/cards) (last updated April 2025) and are crafted to be clear, detailed, and useful for beginners, adhering to modern web standards.

## Tags for `summary`

The `summary` card type displays a small image alongside a title and description. It is used in `author-profile.html` for profile pages.

- **`twitter:card`**  
  This tag specifies the type of Twitter Card, set to "summary". It displays a smaller image thumbnail alongside the title and description, suitable for profile pages and shorter content.

- **`twitter:site`**  
  This tag provides the Twitter handle of the website, prefixed with "@" (e.g., "@blogTwitter"). It identifies the account associated with the content.

- **`twitter:title`**  
  This tag contains the title displayed on Twitter. It should be kept to approximately 70 characters to avoid truncation.

- **`twitter:description`**  
  This tag provides a summary of the content, displayed on Twitter. It should be between 100 and 200 characters to fit well within the platform's display limits.

- **`twitter:image`**  
  This tag contains the URL of the image to be displayed on the Twitter Card. For the `summary` card, the image is displayed as a small thumbnail.

- **`twitter:image:alt`**  
  This tag provides a textual description of the image, such as "Photo of John Doe". It is essential for accessibility.

## Tags for `summary_large_image`

- **`twitter:card`**  
  This tag specifies the type of Twitter Card, set to "summary_large_image". It indicates that the card will feature a large image along with a title and description when shared on Twitter.

- **`twitter:site`**  
  This tag provides the Twitter handle of the website, prefixed with "@" (e.g., "@amazingbrand"). It identifies the account associated with the content.

- **`twitter:title`**  
  This tag contains the title displayed on Twitter. It should be kept to approximately 70 characters to avoid truncation and ensure full visibility.

- **`twitter:description`**  
  This tag provides a summary of the content, displayed on Twitter. It should be between 100 and 200 characters to fit well within the platform’s display limits.

- **`twitter:image`**  
  This tag contains the URL of the image to be displayed on the Twitter Card. It must be in JPEG, PNG, or WebP format, with a minimum resolution of 280 pixels in width and 150 pixels in height, though 1200 pixels in width and 628 pixels in height is recommended for optimal quality. The file size should not exceed 5MB to ensure efficient loading.

- **`twitter:image:alt`**  
  This tag provides a textual description of the image, such as "Photo of a product". It is essential for accessibility, helping users who cannot see the image understand its content.

- **`twitter:creator`**  
  This tag provides the Twitter handle of the content’s author, prefixed with "@" (e.g., "@authorTwitter"). It credits the individual who created the content, helping users identify the author on Twitter.

- **`twitter:player`**  
  This tag specifies the URL of an iframe-based video player, such as "https://example.com/embed/video". It’s required for the "player" card type in `online-cinema.html`, enabling users to play the movie directly within the Twitter feed. The player must use HTTPS, support a 16:9 aspect ratio, and be publicly accessible, per Twitter’s guidelines.

- **`twitter:player:width`**  
  This tag defines the width of the video player in pixels, set to "640" in `online-cinema.html`. It’s required for "player" cards, ensuring the embedded player fits Twitter’s display correctly. The value should match the actual player width, with a minimum of 320 pixels recommended for clarity.

- **`twitter:player:height`**  
  This tag sets the height of the video player in pixels, set to "360" in `online-cinema.html`. It’s required alongside `twitter:player:width` for "player" cards, maintaining the aspect ratio (e.g., 16:9 for 640x360). It ensures the video displays properly within the card on Twitter.