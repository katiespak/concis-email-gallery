# Concis Labs — email templates

Six HTML email templates for Concis Labs, with a gallery for viewing them.

**[View the gallery →](https://katiespak.github.io/concis-email-gallery/)**

```
index.html   gallery — live renders of all six, with a zoom control
r2/          the five broadcast templates
lyndon/      the transactional template
assets/      image assets
```

| Template | Kind | Notes |
|---|---|---|
| Welcome / Onboarding | Broadcast | Cream card, illustration, three onboarding steps |
| Weekly Digest | Broadcast | Lime badge; cream state cards plus a peach "coming up" card |
| PA Criteria Update | Broadcast | Peach badge; dark card with dash bullets, then a key-takeaway card |
| Alert / Market Insight | Broadcast | Mint badge; dark card, three dash-bulleted items |
| Feature Launch | Broadcast | Cream card with three screenshot + heading + body sections |
| Lyndon — Roster Response | Transactional | Roster table, three columns, no unsubscribe |

The transactional template is shown with **sample data — all names and
organizations in it are fictional.** It carries no unsubscribe link by design:
it's a reply to a question the recipient asked, not a campaign.

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
