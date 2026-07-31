# Your Store Is Invisible to AI. llms.txt Fixes That in Under an Hour.

Ask your AI to "recommend a store for X" and see if your business shows up. For most online stores, it doesn't, because most sites are a wall to a model.

A browser renders JavaScript, images, and scripts into something a human can read. A model wants clean, structured text it can index. If an AI can't parse your pages, it can't recommend you, and that matters more than it did a year ago. Shopping is starting to move from "browse and pick" to "ask an agent, let it compare and buy." You spent a decade optimizing for Google. There's a new reader now and it reads differently.

The fix is a single plain-text file. llms.txt is a proposal from Jeremy Howard, published in 2024 (original post), for a markdown file placed at the root of your site, like /llms.txt. It tells an AI what you sell, which pages matter, and how to understand your content. Think of it as a sitemap written for a language model instead of a crawler.

Setting it up genuinely takes under an hour. Here's what a real one looks like, for a fictional store:

```
# Example Store

> Example Store sells handmade leather bags and accessories,
> made to order in Portland, Oregon.

## About
We are a small workshop making leather goods since 2012.
Ship worldwide, 30-day returns.

## Products
- [All products](/products)
- [Leather bags](/products/bags)
- [Wallets](/products/wallets)
- [Shoes](/products/shoes)

## Contact
- [Shipping policy](/shipping)
- [Returns](/returns)
- [Contact](/contact)
```

Three fields do most of the work: a title line, a short description with the ">" prefix, and a list of links to your key pages. Keep each link's anchor text descriptive ("Leather bags," not "click here"), because that's what the model uses to decide what's on the page. Drop the file at your domain root, then check that `curl https://yourstore.com/llms.txt` returns it as plain text. That's the whole setup.

It's early, which is the point. Very few merchants have done this yet, so a readable store is the exception rather than the norm. That's a small thing in your favor, but it's not a race you need to win this week. Do it once, correctly, and it stays done.

The template above works as-is. If you want the longer version with the extra sections people add, I keep one up on my site, free.

#llms.txt #AIAgents #Ecommerce #AgenticCommerce
