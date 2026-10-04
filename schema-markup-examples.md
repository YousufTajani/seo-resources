# Schema Markup Examples

Practical JSON-LD schema markup examples for common website types.

These examples are designed to help website owners and SEO professionals understand how structured data can be implemented using Schema.org vocabulary.

> Always customize the examples with your own website's real information before deploying them.

---

## Table of Contents

- [Organization](#organization)
- [WebSite](#website)
- [Article](#article)
- [FAQPage](#faqpage)
- [Product](#product)
- [BreadcrumbList](#breadcrumblist)
- [LocalBusiness](#localbusiness)
- [SEO Tool Resources](#seo-tool-resources)
- [Important Implementation Notes](#important-implementation-notes)

---

## Organization

Use `Organization` structured data to describe a company, organization, brand, or other organized entity.

```html
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "name": "Example Company",
  "url": "https://www.example.com",
  "logo": "https://www.example.com/images/logo.png",
  "description": "Example company description.",
  "sameAs": [
    "https://www.facebook.com/example",
    "https://www.linkedin.com/company/example"
  ]
}
</script>
Recommended properties
- name
- url
- logo
- description
- sameAs
Only include information that accurately represents the organization.
WebSite
Use WebSite structured data to describe the overall website.
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "name": "Example Website",
  "url": "https://www.example.com",
  "description": "Example website description."
}
</script>

Example
For an SEO tools website:
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "name": "Search Learning Tools",
  "url": "https://searchlearningtools.com",
  "description": "Free SEO tools and resources for website owners, marketers, and SEO professionals."
}
</script>

Article
Use Article structured data for editorial content, guides, tutorials, news articles, and other article-like pages.
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Example Article Title",
  "description": "A short description of the article.",
  "image": [
    "https://www.example.com/images/article-image.jpg"
  ],
  "author": {
    "@type": "Person",
    "name": "Author Name"
  },
  "publisher": {
    "@type": "Organization",
    "name": "Example Company",
    "logo": {
      "@type": "ImageObject",
      "url": "https://www.example.com/images/logo.png"
    }
  },
  "datePublished": "2026-10-01",
  "dateModified": "2026-10-01",
  "mainEntityOfPage": {
    "@type": "WebPage",
    "@id": "https://www.example.com/example-article"
  }
}
</script>

Important
Make sure the structured data accurately represents the visible content of the page.
Do not use an article schema simply to add keywords that do not appear in the article.
FAQPage
Use FAQPage structured data for pages containing frequently asked questions and answers.
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is SEO?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "SEO is the process of improving a website's visibility in search engines through technical, content, and authority-related improvements."
      }
    },
    {
      "@type": "Question",
      "name": "Why is structured data useful?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Structured data helps search engines understand the meaning and relationships of information on a webpage."
      }
    }
  ]
}
</script>

Important
The questions and answers represented in the markup should also be visible to users on the page.
Do not add hidden questions or answers solely for search-engine purposes.
Product
Use Product structured data for product pages.
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "Product",
  "name": "Example Product",
  "image": [
    "https://www.example.com/images/product.jpg"
  ],
  "description": "Example product description.",
  "sku": "EXAMPLE-001",
  "brand": {
    "@type": "Brand",
    "name": "Example Brand"
  },
  "offers": {
    "@type": "Offer",
    "url": "https://www.example.com/products/example-product",
    "priceCurrency": "USD",
    "price": "49.99",
    "availability": "https://schema.org/InStock"
  }
}
</script>

Common properties
- name
- image
- description
- sku
- brand
- offers
- aggregateRating
- review
Only add ratings and reviews when genuine reviews exist and the information follows the applicable structured-data guidelines.
BreadcrumbList
Use BreadcrumbList structured data to describe the hierarchical path to a page.
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "BreadcrumbList",
  "itemListElement": [
    {
      "@type": "ListItem",
      "position": 1,
      "name": "Home",
      "item": "https://www.example.com/"
    },
    {
      "@type": "ListItem",
      "position": 2,
      "name": "SEO Tools",
      "item": "https://www.example.com/seo-tools"
    },
    {
      "@type": "ListItem",
      "position": 3,
      "name": "Keyword Tool",
      "item": "https://www.example.com/seo-tools/keyword-tool"
    }
  ]
}
</script>

Best practice
The breadcrumb structure should match the actual navigational hierarchy shown on the webpage.
LocalBusiness
Use LocalBusiness structured data for a business that operates at a physical location or serves a defined local area.
<script type="application/ld+json">
{
  "@context": "https://schema.org",
  "@type": "LocalBusiness",
  "name": "Example Local Business",
  "image": "https://www.example.com/images/business.jpg",
  "url": "https://www.example.com",
  "telephone": "+1-555-555-5555",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "123 Example Street",
    "addressLocality": "Example City",
    "addressRegion": "Example State",
    "postalCode": "12345",
    "addressCountry": "US"
  },
  "openingHoursSpecification": [
    {
      "@type": "OpeningHoursSpecification",
      "dayOfWeek": [
        "Monday",
        "Tuesday",
        "Wednesday",
        "Thursday",
        "Friday"
      ],
      "opens": "09:00",
      "closes": "17:00"
    }
  ]
}
</script>

Important
Use the most specific appropriate LocalBusiness subtype when possible, such as:
- Restaurant
- Dentist
- Store
- MedicalBusiness
- AutomotiveBusiness
Do not use LocalBusiness markup for an online-only business that does not qualify as a local business.
SEO Tool Resources
If you need to analyze or optimize your website, see:
https://searchlearningtools.com/free-seo-tools
Search Learning Tools provides free SEO tools and resources for website owners, marketers, and SEO professionals.
Important Implementation Notes
1. Use real information
Replace all example information with accurate information about the website, organization, product, or business.
2. Match visible content
Structured data should describe content that is actually present on the corresponding webpage.
3. Use JSON-LD
JSON-LD is generally the easiest structured-data format to implement and maintain.
4. Avoid fake reviews
Never create fictional ratings, testimonials, or reviews for the purpose of obtaining search visibility.
5. Keep URLs consistent
Use the canonical URL for the relevant page whenever possible.
6. Validate your markup
After implementation, test the structured data with Google's structured-data testing and validation tools and check for warnings or errors.
7. Do not overuse schema
Only add schema types that genuinely describe the content or entity represented on the page.
8. Keep markup updated
When page titles, prices, availability, authors, dates, addresses, or other important information changes, update the corresponding structured data.
Quick Reference
Schema Type	Typical Use
Organization	Company or organization information
WebSite	Website-level information
Article	Articles, guides, and editorial content
FAQPage	Frequently asked questions
Product	Product pages
BreadcrumbList	Page hierarchy and navigation
LocalBusiness	Local businesses and physical locations


Final Reminder
Schema markup helps search engines understand webpage content, but adding structured data does not guarantee a rich result or special search appearance.
Use structured data to accurately describe the page first, and treat enhanced search presentation as a possible benefit rather than a guaranteed outcome.
```
