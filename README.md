# Tlhogi's Cakes

A static site. Three HTML pages and a folder of images. No build step, no dependencies, no server code.

```
index.html      the whole site
img/            logo, portrait, and every photo at two sizes (-t = thumbnail)
```

It's one page with three views: home, `#gallery` and `#about`. Clicking Gallery or About me swaps the view in place rather than loading another page, so nothing ever opens in a new tab. Links like `yoursite.com/#gallery` still work if you share them.

The site is written throughout in Tlhogi's own voice, first person. Keep it that way when you edit copy.

## Hosting it

**Cloudflare Pages**

1. Sign in at dash.cloudflare.com, go to Workers & Pages, Create, Pages, "Upload assets".
2. Drag this whole folder in. Deploy.
3. You get a free `*.pages.dev` address with HTTPS.

**Netlify**

1. Sign in at app.netlify.com, go to Sites, "Deploy manually".
2. Drag this whole folder onto the drop zone.
3. You get a free `*.netlify.app` address with HTTPS.

Either one lets you attach your own domain later under the site's domain settings. A `.co.za` domain is the obvious choice for a Pretoria business; check current pricing with a local registrar, and point the domain at the host by following that host's DNS instructions.

To update the site afterwards, edit the files and drag the folder in again.

## Before it goes live

**The About page.** `about.html` is written in Tlhogi's voice and everything on it is true today, so it can go live as it stands. What it does not have yet is her own story: when she started, who taught her, why she bakes. When she gives you that, it belongs in the two paragraphs beside her portrait, and a line of hers in quotation marks would sit well underneath them.

**Her details.** The WhatsApp number appears as `wa.me/27797457146` in links and as `079 745 7146` in text. Search and replace both if it ever changes.

## Notes

- Banking details are deliberately not on the site. The terms say a 50% deposit secures the order and that details are sent on WhatsApp once it is confirmed. Keep it that way.
- Fonts load from Google Fonts: Bodoni Moda for headings, Hanken Grotesk for body text. Everything else is inline, so the site works offline apart from the fonts.
- To add a new cake photo: save a large version as `img/name.jpg` and a thumbnail as `img/name-t.jpg`, then add one line to the `PHOTOS` list at the bottom of `gallery.html` in the form `["name","Title","One sentence caption.","celebration"]`. The last value is the filter: `celebration`, `kids`, `cupcakes` or `bakes`, and it can hold more than one separated by a space.
