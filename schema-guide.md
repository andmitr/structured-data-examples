# Schema.org Guide

This guide provides a detailed explanation of all Schema.org properties used in the `structured-data-examples` repository, specifically within `product-landing.html`, `service-landing.html`, `online-cinema.html`, `blog.html`, and `tech-blog.html`. Schema.org markup improves how search engines like Google understand and display your web content, such as showing prices, reviews, or maps in search results. All descriptions are based on the official [Schema.org documentation](https://schema.org) (last updated April 2025) and incorporate practical recommendations from Google where applicable. They are crafted to be clear, detailed, and useful for anyone working with these files. This guide avoids examples and focuses on comprehensive, beginner-friendly explanations, adhering to modern web standards.

## Table of Contents

1. [Properties for `Product` (Used in `product-landing.html`)](#properties-for-product-used-in-product-landinghtml)  
2. [Properties for `LocalBusiness` (Used in `service-landing.html`)](#properties-for-localbusiness-used-in-service-landinghtml)  
3. [Properties for `BlogPosting` (Used in `blog.html`)](#properties-for-blogposting-used-in-bloghtml)  
4. [Properties for `TechArticle` (Used in `tech-blog.html`)](#properties-for-techarticle-used-in-tech-bloghtml)
5. [Properties for `Movie` and `VideoObject` (Used in `online-cinema.html`)](#properties-for-movie-and-videoobject-used-in-online-cinemahtml)

## Properties for `Product` (Used in `product-landing.html`)

- **`@context`**  
  This tag specifies the JSON-LD context, set to "https://schema.org". It is a required element that tells search engines which vocabulary to use, ensuring the markup is recognized and processed correctly according to Schema.org standards.

- **`@type`**  
  This tag defines the type of item being described, set to "Product". It is essential for search engines to identify the content as a sellable item, enabling features like price or review snippets in search results.

- **`name`**  
  This field holds the product’s name, such as "Wireless Headphones". It appears in search result titles and snippets, and should be kept between 60 and 70 characters in length to prevent truncation and maintain readability.

- **`image`**  
  This field contains the URL pointing to the product’s primary image. It is used by search engines to display a visual in rich snippets. Schema.org accepts any image format accessible by URL, though Google recommends JPEG, PNG, or WebP, with a minimum resolution of 1200 pixels in width and 630 pixels in height, and a file size not exceeding 8MB for optimal performance in search results.

- **`description`**  
  This field provides a textual summary of the product, such as "High-quality headphones with noise cancellation". It is displayed in search engine snippets and should be between 50 and 160 characters long to ensure it fits well and remains informative.

- **`sku`**  
  This field represents the stock keeping unit, a unique identifier for the product, such as a catalog number. It assists search engines and inventory systems in tracking individual items, with no specific format required beyond ensuring uniqueness (e.g., it can be numeric, alphanumeric, or symbolic).

- **`brand`**  
  This field identifies the product’s manufacturer through a nested object with `@type` set to "Brand". It includes a `name` field (e.g., for the brand name), which helps link the product to its originating company, improving categorization in search results.

- **`offers`**  
  This field describes the commercial offer for the product using a nested object with `@type` set to "Offer". It includes the following subfields, each critical for e-commerce visibility:
  - `priceCurrency`: Specifies the currency code using the ISO 4217 standard (e.g., "USD" for U.S. dollars, "RUB" for Russian rubles), a mandatory field for price interpretation.
  - `price`: Indicates the product’s price as a decimal number (e.g., 29.99), essential for displaying cost in rich snippets.
  - `availability`: Denotes the stock status using a Schema.org URL (e.g., "https://schema.org/InStock" or "https://schema.org/OutOfStock"), vital for informing users of availability.
  - `priceValidUntil`: Sets the expiration date of the price, formatted in ISO 8601 (e.g., "2025-12-31"), ensuring the price remains accurate over time.
  - `url`: Provides the canonical URL of the product page, linking directly to the offer source.
  - `seller`: A nested object with `@type` set to "Organization" and a `name` field, identifying the entity selling the product.
  - `itemOffered`: A nested object with `@type` set to "Product" and a `name` field, referencing the product being offered.
  - `acceptedPaymentMethod`: Lists the payment methods accepted, using Schema.org URLs (e.g., "https://schema.org/Cash", "https://schema.org/CreditCard"), helping users understand payment options.

- **`review`**  
  This field represents a customer review through a nested object with `@type` set to "Review". It includes the following subfields to provide detailed feedback:
  - `reviewRating`: A nested object with `@type` set to "Rating", containing `ratingValue` (a number from 0 to 5) and `bestRating` (set to 5), quantifying the review’s score.
  - `author`: A nested object with `@type` set to "Person" and a `name` field, indicating the reviewer’s identity.
  - `reviewBody`: Contains the textual content of the review, offering detailed user opinions.
  - `datePublished`: Specifies the review’s publication date in ISO 8601 format (e.g., "2025-04-03T10:00:00Z"), providing temporal context.

- **`aggregateRating`**  
  This field summarizes the overall customer ratings through a nested object with `@type` set to "AggregateRating". It includes:
  - `ratingValue`: The average rating as a decimal number (e.g., 4.5), reflecting collective user feedback.
  - `reviewCount`: The total number of reviews contributing to the average, indicating the sample size (e.g., 200).

- **`shippingDetails`**  
  This field outlines the shipping information through a nested object with `@type` set to "OfferShippingDetails". It includes the following subfields to detail logistics:
  - `shippingRate`: A nested object with `@type` set to "MonetaryAmount", containing `value` (the shipping cost, e.g., 5.99) and `currency` (ISO 4217 format, e.g., "USD"), specifying the fee.
  - `shippingDestination`: A nested object with `@type` set to "DefinedRegion", containing `addressCountry` (ISO 3166-1 code, e.g., "US"), defining where shipping is available.
  - `deliveryTime`: A nested object with `@type` set to "ShippingDeliveryTime", describing the expected delivery schedule.
  - `handlingTime`: A nested object with `@type` set to "QuantitativeValue", including `maxValue` (maximum handling days, e.g., 2), indicating preparation time.
  - `transitTime`: A nested object with `@type` set to "QuantitativeValue", including `minValue` (minimum transit days, e.g., 3) and `maxValue` (maximum transit days, e.g., 5), outlining shipping duration.

- **`hasMerchantReturnPolicy`**  
  This field details the return policy through a nested object with `@type` set to "MerchantReturnPolicy". It includes the following subfields to clarify return terms:
  - `returnPolicyCategory`: A Schema.org URL (e.g., "https://schema.org/MerchantReturnFiniteReturnWindow"), indicating the type of return policy.
  - `merchantReturnDays`: Specifies the number of days allowed for returns (e.g., 14), defining the return window.
  - `returnFees`: A Schema.org URL (e.g., "https://schema.org/FreeReturn"), indicating who bears the cost of return shipping.
  - `returnMethod`: A Schema.org URL (e.g., "https://schema.org/ReturnByMail"), indicating how the item must be returned.
  - `applicableCountry`: The country code using ISO 3166-1 (e.g., "RU"), specifying where the policy applies.

## Properties for `LocalBusiness` (Used in `service-landing.html`)

- **`@context`**  
  This tag specifies the JSON-LD context, set to "https://schema.org". It is a required element that ensures search engines recognize the Schema.org vocabulary.

- **`@type`**  
  This tag defines the type as "LocalBusiness", indicating a physical business location. It enables features like map displays and local search results.

- **`name`**  
  This field holds the business name, such as "City Repair Shop". It is displayed in local search results and should be clear and concise.

- **`url`**  
  This field provides the URL of the business website, enhancing online discoverability and linking to the official site.

- **`address`**  
  This field details the physical location through a nested object with `@type` set to "PostalAddress". It includes:
  - `streetAddress`: The street name and number (e.g., "123 Main St").
  - `addressLocality`: The city or locality name (e.g., "Moscow").
  - `addressRegion`: The state or region code (e.g., "Moscow Region").
  - `postalCode`: The postal code (e.g., "12345").
  - `addressCountry`: The country code using ISO 3166-1 (e.g., "RU").

- **`telephone`**  
  This field specifies the business phone number in international format (e.g., "+7-495-123-4567"). It provides a direct contact method for users.

- **`email`**  
  This field contains the business email address (e.g., "info@repairshop.com"), offering an additional contact option.

- **`openingHoursSpecification`**  
  This field defines the business operating hours through a nested object with `@type` set to "OpeningHoursSpecification". It includes:
  - `dayOfWeek`: Specifies the days of operation (e.g., "Monday" through "Friday").
  - `opens`: The opening time in 24-hour format (e.g., "09:00").
  - `closes`: The closing time in 24-hour format (e.g., "17:00").

- **`priceRange`**  
  This field indicates the approximate pricing range as a text value (e.g., "$$-$$$"). It provides a quick cost estimate and can be represented in various formats, such as dollar signs ($ for low cost, $$ for moderate, $$$ for high, $$$$ for premium) or other textual descriptions, depending on the implementation.

- **`review`**  
  This field represents a customer review through a nested object with `@type` set to "Review". It includes:
  - `reviewRating`: A nested object with `@type` set to "Rating", containing `ratingValue` (a number from 0 to 5).
  - `author`: A nested object with `@type` set to "Person", containing `name`.
  - `reviewBody`: The textual content of the review.
  - `datePublished`: The publication date in ISO 8601 format (e.g., "2025-04-03").
  - `reviewAspect`: The specific aspect being reviewed (e.g., "service").

- **`sameAs`**  
  This field is an array of URLs linking to the business’s social media profiles (e.g., "https://facebook.com/business"). It enhances online presence and credibility.

- **`geo`**  
  This field specifies the geographic coordinates through a nested object with `@type` set to "GeoCoordinates". It includes:
  - `latitude`: The latitude value (e.g., 55.7558), representing the north-south position.
  - `longitude`: The longitude value (e.g., 37.6173), representing the east-west position.

## Properties for `BlogPosting` (Used in `blog.html`)

- **`@context`**  
  This tag specifies the JSON-LD context, set to "https://schema.org". It is a required element for search engine recognition of the Schema.org markup.

- **`@type`**  
  This tag defines the type as "BlogPosting", indicating a blog article. It enables rich snippets such as author names or publication dates in search results.

- **`headline`**  
  This field contains the blog post’s title, such as "How to Cook Pasta". It is displayed in search snippets and should be kept to approximately 60 characters to avoid truncation.

- **`description`**  
  This field provides a summary of the blog post, such as "A simple guide to making perfect pasta at home". It appears in search snippets and should be between 50 and 160 characters for optimal display.

- **`datePublished`**  
  This field specifies the publication date of the blog post in ISO 8601 format with UTC (e.g., "2025-04-03T10:00:00Z"). It helps search engines index the article’s release timeline accurately.

- **`dateModified`**  
  This field indicates the last modification date of the blog post in ISO 8601 format with UTC (e.g., "2025-04-03T12:00:00Z"). It ensures search engines reflect the most recent updates.

- **`author`**  
  This field identifies the author through a nested object with `@type` set to "Person". It includes:
  - `name`: The author’s full name (e.g., "Jane Doe").

- **`image`**  
  This field defines the primary image for the blog post through a nested object with `@type` set to "ImageObject". It includes:
  - `url`: The URL of the image, which can be in formats like JPEG, PNG, WebP, or GIF, depending on search engine support.
  - `width`: The image width in pixels, with a minimum of 1200 pixels recommended for optimal display.
  - `height`: The image height in pixels, with a minimum of 630 pixels recommended.

- **`keywords`**  
  This field lists relevant keywords in a comma-separated string (e.g., "cooking, pasta, recipe"). It helps search engines categorize and index the content effectively.

- **`mainEntityOfPage`**  
  This field links to the canonical page through a nested object with `@type` set to "WebPage". It includes:
  - `@id`: The canonical URL of the blog post (e.g., "https://example.com/blog/pasta").

- **`BreadcrumbList`**  
  Google's Breadcrumb rich result requires `BreadcrumbList` to be its own top-level item, not a nested property of `BlogPosting`. In `blog.html` it is declared as a second object alongside `BlogPosting`, inside the same JSON-LD array. It includes:
  - `itemListElement`: An array of objects with `@type` set to "ListItem", each containing `position` (an Integer indicating order, e.g., 1), and `item` (an object with `@id` for the step's URL and `name` for its label).

## Properties for `TechArticle` (Used in `tech-blog.html`)

- **`@context`**  
  This tag specifies the JSON-LD context, set to "https://schema.org". It is a required element that ensures search engines interpret the markup using the Schema.org vocabulary.

- **`@type`**  
  This tag defines the type as "TechArticle", indicating a technical article or tutorial. It enables search engines to categorize the content as educational or instructional, potentially enhancing visibility for technical searches.

- **`headline`**  
  This field contains the article’s title, such as "How to Optimize Code Performance". It appears in search snippets and should be concise, ideally around 60 characters, to avoid truncation.

- **`description`**  
  This field provides a summary of the article, such as "A detailed guide with tips to make your code run faster". It is used in search snippets and should range between 50 and 160 characters for clarity and fit.

- **`datePublished`**  
  This field specifies the publication date in ISO 8601 format with UTC (e.g., "2025-04-03T10:00:00Z"). It establishes the article’s initial release date for search engine indexing.

- **`dateModified`**  
  This field indicates the last modification date in ISO 8601 format with UTC (e.g., "2025-04-03T12:00:00Z"). It ensures search engines display the most current version of the content.

- **`author`**  
  This field identifies the article’s author through a nested object with `@type` set to "Person". It includes:
  - `name`: The author’s full name (e.g., "John Doe").
  - `url`: A URL linking to the author’s profile or page (e.g., "https://example.com/about").

- **`mainEntityOfPage`**  
  This field links to the canonical page through a nested object with `@type` set to "WebPage". It includes:
  - `@id`: The canonical URL of the article (e.g., "https://example.com/blog/code-optimization"), ensuring accurate page association.

- **`image`**  
  This field specifies the primary image through a nested object with `@type` set to "ImageObject". It includes:
  - `url`: The image URL, which can be in formats like JPEG, PNG, WebP, or GIF, depending on search engine support.
  - `width`: The image width in pixels, with a minimum of 1200 pixels recommended for optimal display.
  - `height`: The image height in pixels, with a minimum of 630 pixels recommended.

- **`keywords`**  
  This field lists relevant keywords as a text string, such as "coding, optimization, performance, javascript". Per Schema.org documentation (https://schema.org/keywords), this property expects a single text value where multiple keywords are separated by commas. In `tech-blog.html`, it is implemented as a string, which conforms to the Schema.org standard. Search engines like Google often parse this format correctly. It aids search engines in indexing and categorizing the technical content.

- **`proficiencyLevel`**  
  This field indicates the intended skill level of the audience, such as "Intermediate". It helps search engines match the content to users with appropriate technical expertise. Possible values include:
  - "Beginner": For readers with little to no prior knowledge.
  - "Intermediate": For readers with some experience or basic understanding.
  - "Advanced": For readers with extensive knowledge or expertise.
  - "Expert": For highly skilled professionals in the field.

- **`dependencies`**  
  This field specifies the technical prerequisites or tools required, such as "JavaScript, Node.js". It informs readers and search engines about necessary knowledge or software.

- **`articleSection`**  
  This field categorizes the article’s topic, such as "Code Optimization Techniques". It assists in organizing content for search engine results and user navigation.

- **`about`**  
  This field describes the subject matter through a nested object with `@type` set to "Thing". It includes:
  - `name`: The topic name (e.g., "Code Performance"), clarifying the article’s focus.

- **`learningResourceType`**  
  This field defines the content type, such as "Tutorial". It signals to search engines that the article serves an educational purpose. Possible values include:
  - "Article": A standard informational piece.
  - "Tutorial": Step-by-step instructional content.
  - "Guide": A comprehensive overview or manual.
  - "Reference": A detailed resource for lookup or consultation.
  - "FAQ": A question-and-answer format.
  - "Course": Structured educational material.
  - "Video": Multimedia instructional content.
  - "Exercise": Practical tasks or challenges.

- **`inLanguage`**  
  This field specifies the language of the content using an IETF BCP 47 code (e.g., "en-US"). It ensures accurate language targeting for search engine users.

- **`audience`**  
  This field identifies the target audience through a nested object with `@type` set to "Audience". It includes:
  - `audienceType`: The audience category (e.g., "Developers"), refining the content’s intended readership. Possible categories include:
    - "Developers": Software engineers or programmers.
    - "Students": Learners in educational settings.
    - "Educators": Teachers or instructors.
    - "Researchers": Academic or scientific professionals.
    - "General Public": Non-specialized readers.
    - "Business Professionals": Managers or industry workers.
    - "Enthusiasts": Hobbyists or passionate amateurs.

- **`genre`**  
  This field denotes the content style, such as "Technical". It helps search engines classify the article’s tone and purpose. Possible values include:
  - "Technical": Focused on specialized, technical topics.
  - "Educational": Aimed at teaching or informing.
  - "Narrative": Storytelling or descriptive content.
  - "Opinion": Personal views or commentary.
  - "News": Current events or updates.
  - "Review": Evaluations or critiques.
  - "Instructional": How-to or procedural content.

- **`BreadcrumbList`**  
  Google's Breadcrumb rich result requires `BreadcrumbList` to be its own top-level item, not a nested property of `TechArticle`. In `tech-blog.html` it is declared as a second object alongside `TechArticle`, inside the same JSON-LD array. It includes:
  - `itemListElement`: An array of objects with `@type` set to "ListItem", each containing `position` (an Integer indicating order, e.g., 1), and `item` (an object with `@id` for the step's URL and `name` for its label).

## Properties for `Movie` and `VideoObject` (Used in `online-cinema.html`)

- **`@context`**  
  This tag specifies the JSON-LD context, set to "https://schema.org". It is a required element that ensures search engines interpret the markup using the Schema.org vocabulary.

- **`@type`**  
  This tag defines the type, set to "Movie" or "VideoObject". "Movie" identifies the content as a cinematic work, enabling rich snippets like cast or ratings, while "VideoObject" describes a specific video file, supporting video previews in search results.

- **`name`**  
  This field holds the title of the movie or video, such as "Movie Title". It appears in search result titles and snippets, and should be concise, ideally around 60 characters, to avoid truncation.

- **`description`**  
  This field provides a summary of the movie or video, such as "A brief description of the movie, showcasing its plot and appeal". It is displayed in search snippets and should be between 50 and 160 characters for optimal fit and informativeness.

- **`inLanguage`**  
  This field specifies the language of the content using an IETF BCP 47 code (e.g., "en-US"). It ensures accurate language targeting for search engine users and applies to both the movie and its video.

- **`url`**  
  This field provides the canonical URL of the movie page (e.g., "https://example.com/movie-title"). It links directly to the content, enhancing discoverability and indexing by search engines.

- **`image`**  
  This field contains the URL of the movie’s primary image, typically a poster. It is used by search engines for rich snippets. Google recommends JPEG, PNG, or WebP formats, with a minimum resolution of 120x120 pixels, though 1200x675 is preferred for quality display.

- **`genre`**  
  This field lists the movie’s genres as an array (e.g., ["Action", "Adventure"]). It helps search engines categorize the content, improving relevance in genre-specific searches.

- **`datePublished`**  
  This field specifies the movie’s release date in ISO 8601 format (e.g., "2025-04-03"). It establishes the initial availability date for search engine indexing.

- **`actor`**  
  This field identifies the movie’s actors through an array of nested objects with `@type` set to "Person". Each includes:
  - `name`: The actor’s full name (e.g., "Actor One"), displayed in rich snippets to highlight the cast.

- **`director`**  
  This field identifies the movie’s director through a nested object with `@type` set to "Person". It includes:
  - `name`: The director’s full name (e.g., "Director Name"), shown in search results to credit the filmmaker.

- **`duration`**  
  This field specifies the length of the movie or video in ISO 8601 duration format (e.g., "PT2H" for 2 hours). It informs users and search engines about the runtime, enhancing content previews.

- **`contentRating`**  
  This field indicates the movie’s age or content rating (e.g., "PG-13"). It uses standard rating systems (e.g., MPAA), helping search engines filter content by audience suitability.

- **`aggregateRating`**  
  This field summarizes overall ratings through a nested object with `@type` set to "AggregateRating". It includes:
  - `ratingValue`: The average rating as a decimal (e.g., 4.5), reflecting user feedback.
  - `reviewCount`: The number of reviews (e.g., 100), indicating the sample size.
  - `bestRating`: The maximum rating scale value (e.g., 5).
  - `worstRating`: The minimum rating scale value (e.g., 0).

- **`review`**  
  This field represents a user review through a nested object with `@type` set to "Review". It includes:
  - `author`: A nested object with `@type` set to "Person" and `name` (e.g., "Reviewer Name"), identifying the reviewer.
  - `reviewBody`: The text of the review (e.g., "Great movie with stunning visuals!"), providing detailed feedback.
  - `reviewRating`: A nested object with `@type` set to "Rating", containing `ratingValue` (e.g., 5), `bestRating` (e.g., 5), and `worstRating` (e.g., 0), quantifying the score.
  - `datePublished`: The review’s publication date in ISO 8601 format (e.g., "2025-04-03T10:00:00Z"), adding temporal context.

- **`video`**  
  This field embeds video details within the `Movie` type through a nested object with `@type` set to "VideoObject". It links the movie to its video content, supporting video-specific rich results.

- **`trailer`**  
  This field provides details of the movie’s trailer through a nested object with `@type` set to "VideoObject". It connects the movie to its promotional video, enhancing discoverability.

- **`thumbnailUrl`**  
  This field contains the URL of the video’s thumbnail image. It is required for `VideoObject` by Google, with a minimum resolution of 120x120 pixels, though 1200x675 is recommended for quality.

- **`uploadDate`**  
  This field specifies the video’s upload date in ISO 8601 format (e.g., "2025-04-03T10:00:00Z"). It indicates when the video was made available online, aiding search engine indexing.

- **`contentUrl`**  
  This field provides the direct URL to the video file (e.g., "https://example.com/video.mp4"). It allows search engines to access the raw video content, though it’s optional if `embedUrl` is provided.

- **`embedUrl`**  
  This field provides the URL for embedding the video (e.g., "https://example.com/embed/video"). It enables video playback via an iframe, supporting rich video previews in search results.

- **`interactionStatistic`**  
  This field tracks user interactions with the video through an array of nested objects with `@type` set to "InteractionCounter". Each includes:
  - `interactionType`: The type of interaction, using Schema.org URLs (e.g., "https://schema.org/WatchAction" for views, "https://schema.org/LikeAction" for likes, "https://schema.org/CommentAction" for comments, "https://schema.org/ShareAction" for shares).
  - `userInteractionCount`: The number of interactions (e.g., 10000 for views), reflecting engagement metrics.

- **`regionsAllowed`**  
  This field lists regions where the video is available (e.g., "US, UK, CA") using ISO 3166-1 country codes. It specifies geographic accessibility, though it’s optional—if omitted, the video is assumed available everywhere.

- **`mainEntityOfPage`**  
  This field links the movie to its canonical page through a nested object with `@type` set to "WebPage". It includes:
  - `@id`: The canonical URL of the movie page (e.g., "https://example.com/movie-title"), ensuring accurate page association.