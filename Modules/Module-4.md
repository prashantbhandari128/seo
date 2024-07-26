<div align="center">

[**_``Go Back``_**](../README.md)

</div>

# Module 4: Technical SEO

## Website architecture (Site hierarchy)

Website architecture refers to the way web pages are structured and organized within a website.

**Importance:**
- ``User Experience``: A clear and logical structure helps users navigate the site easily.
- ``SEO``: Helps search engines understand the relationship between different pages and prioritize important content.

**Best Practices:**
- ``Flat Structure``: Avoid deep nesting of pages; keep important pages closer to the homepage.
- ``Internal Linking``: Use internal links to connect related pages and distribute authority across the site.
- ``Logical URL Structure``: Use descriptive URLs that reflect the content hierarchy.

### Site Hierarchy

A clear and logical site hierarchy helps search engines understand the structure of your website and improves user navigation.

- ``Hierarchy Levels``: Keep the hierarchy shallow (preferably not more than 3-4 levels deep).
- ``Breadcrumbs``: Use breadcrumb navigation to help users and search engines understand the structure.
- ``Consistent Structure``: Maintain a consistent structure across the site

**Example:**
```
Home > Courses > Programming > Python > Advanced Python
```

## Page speed optimization (Google PageSpeed Insights, GTmetrix)

Page speed optimization focuses on improving how fast a web page loads.

**Importance:**
- ``User Experience``: Faster loading times improve user satisfaction and reduce bounce rates.
- ``SEO``: Google considers page speed as a ranking factor, especially for mobile searches.

**Tools and Techniques:**
- ``Tools``: Google PageSpeed Insights, GTmetrix, WebPageTest.
- ``Optimization Techniques``: Minify CSS, JavaScript, and HTML; optimize images; leverage browser caching; use content delivery networks (CDNs).

## Mobile SEO (mobile-friendly design, AMP)

Mobile SEO ensures that websites are optimized for mobile devices.

**Importance:**
- ``Mobile Traffic``: A significant portion of internet traffic comes from mobile devices.
- ``SEO``: Google prioritizes mobile-friendly websites in mobile search results.

Best Practices:
- ``Responsive Design``: Ensure the website layout adjusts to different screen sizes.
- ``Mobile-Friendly Test``: Use Google's Mobile-Friendly Test to check and improve mobile usability.
- ``AMP (Accelerated Mobile Pages)``: Implement AMP for content-heavy pages to improve loading speed on mobile devices.

## Crawling and indexing (XML sitemaps, robots.txt)

### XML Sitemaps

XML sitemaps are files that list the URLs of a website to inform search engines about the organization of content. They help search engines crawl and index your site more efficiently. Here's how XML sitemaps work and how to use them effectively:

#### Usage and Benefits:

- ``Content Discovery``: XML sitemaps help search engines discover and crawl all the pages listed in the sitemap, especially those that might not be easily discoverable through normal crawling processes (e.g., pages with few internal links).

- ``Priority and Frequency``: You can specify the priority and update frequency of each URL in the sitemap, guiding search engines on how often they should revisit certain pages.

- ``Large Sites``: For large websites with many pages, XML sitemaps ensure that all pages are indexed, even if they are not linked directly from other pages on the site.

#### Example of an XML Sitemap:

```xml
<?xml version="1.0" encoding="UTF-8"?>
<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">
   <url>
      <loc>https://www.example.com/page1.html</loc>
      <lastmod>2024-07-14</lastmod>
      <changefreq>daily</changefreq>
      <priority>0.8</priority>
   </url>
   <url>
      <loc>https://www.example.com/page2.html</loc>
      <lastmod>2024-07-13</lastmod>
      <changefreq>weekly</changefreq>
      <priority>0.6</priority>
   </url>
</urlset>
```

**Explanation:**

- ``<urlset>``: The root element of the XML sitemap.
- ``<url>``: Each URL is enclosed within the <url> tags.
- ``<loc>``: Specifies the URL of the page.
- ``<lastmod>``: Indicates the last modification date of the page.
- ``<changefreq>``: Specifies how frequently the page is likely to change (always, hourly, daily, weekly, monthly, yearly, never).
- ``<priority>``: Provides the priority of the URL relative to other URLs on the site (range from ``0.0`` to ``1.0``).

### Robots.txt

``Robots.txt`` is a text file located in the root directory of your website that tells search engine crawlers which pages or files they can or cannot request from your site. It's a basic method for controlling and directing web crawlers.

#### Usage and Directives:

##### Disallow: Use Disallow to specify directories or pages that should not be crawled.

**Example:**

```
User-agent: *
Disallow: /admin/
Disallow: /private-page.html
```

- ``User-agent``: ``*``: Applies rules to all search engine crawlers.
- ``Disallow``: ``/admin/``: Instructs crawlers not to crawl pages within the ``/admin/`` directory.
- ``Disallow``: ``/private-page.html``: Prevents crawlers from accessing the specific page ``/private-page.html``.

##### Allow: Use Allow to override a Disallow directive for specific files or directories.

**Example:**

```
User-agent: *
Disallow: /admin/
Allow: /admin/public-page.html
```

- ``Allow``: ``/admin/public-page.html``: Allows crawlers to access the ``/admin/public-page.html`` even though ``/admin/`` is generally disallowed.

## Structured data and schema markup

Structured data and schema markup help search engines understand the content on your web pages better, enabling them to display richer and more informative results in search engine listings. Here's how structured data works and how to implement schema markup:

**Usage and Benefits:**

- ``Enhanced Search Results``: Schema markup can enhance your search listings with rich snippets, such as star ratings, product prices, event details, and more, making your listings more attractive and informative.

- ``Improved Click-Through Rates``: Rich snippets can increase click-through rates (CTR) by providing users with more context about your content before they click through to your site.

- ``Better Understanding``: Search engines use structured data to understand the relationships between different elements on your page, improving relevance and accuracy in search results.

**Example of Schema Markup:**

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Example Product",
  "image": "https://www.example.com/product-image.jpg",
  "description": "Detailed description of the product.",
  "brand": {
    "@type": "Brand",
    "name": "Example Brand"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://www.example.com/product-page.html",
    "priceCurrency": "USD",
    "price": "100.00",
    "availability": "https://schema.org/InStock"
  }
}
</script>
```

Explanation:
- ``@type``: Specifies the type of schema markup (Product in this example).
- ``name``: Name of the product.
- ``image``: URL of the product image.
- ``description``: Detailed description of the product.
- ``brand``: Specifies the brand of the product using nested schema.
- ``offers``: Specifies details about the offer (price, availability, etc.).