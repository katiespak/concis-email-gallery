# Concis Labs — email templates

Five HTML email templates for Concis Labs, with a gallery for viewing them.

**[View the gallery →](https://katiespak.github.io/concis-email-gallery/)**

```
index.html   gallery — live renders of all five, with a zoom control
r2/          the templates
assets/      image assets
```

| Template | Notes |
|---|---|
| Welcome / Onboarding | Cream card, illustration, three onboarding steps |
| Weekly Digest | Lime badge; cream state cards plus a peach "coming up" card |
| PA Criteria Update | Peach badge; dark card with dash bullets, then a key-takeaway card |
| Alert / Market Insight | Mint badge; dark card, three dash-bulleted items |
| Feature Launch | Cream card with three screenshot + heading + body sections |

## Design system

600px container on a `#053330` canvas, 24px content gutters, 620px mobile
breakpoint, dark color scheme only.

- Cream card `#fef9f6`, border `#71dfd6`, radius 14px, hairline `#d4efec`.
  A second variant uses border `#e2d1c7` for takeaway cards.
- Dark card `#063e3a`, border `rgba(126,239,230,0.2)`, radius 14px
- Closing band and footer share one `#0a4a44` wrapper
- Accents: mint `#7eefe6`, lime `#ccff00`, peach `#ffc7a5` / `#7a2e00`
- Type: Switzer, 25/31 headlines at weight 500

Buttons are table-based rather than inline-block anchors, with an `!important`
color rule defending the label against clients that recolor links. The mint
header button is a fixed 302px; the lime closing button is sized to its label.

## Notes

Merge tags (`{{{contact.first_name|there}}}`, `{{{RESEND_UNSUBSCRIBE_URL}}}`)
render literally when a template is opened directly — they resolve at send time.

Asset URLs are absolute, since email clients can't resolve relative paths.
