This is a means of learning [Hugo](https://gohugo.io) by making a rough clone of the 
[Bells of the Rockies](https://www.bellsoftherockies.org/) website.

The site currently uses custom modifications to the [Ananke](https://github.com/gohugo-ananke/ananke) theme

### WIP
- Concerts/repertoire auto
    - [x] Repertoire to individual pages
    - [x] Individual concert pages
    - [x] Index for repertoire
    - [x] Index for concert pages
    - [ ] Improve formatting for composer/writer page
    - [ ] Fix links on Concert and Repertoire leaf pages
    - [ ] Mark concert(s) to show on index page
- Forms: One of
    1. Standard HTML forms
        - Add shortcode in admin UI
        - Figure out action target
        - Is existing tied to Weebly?
        - Should be able to use CloudFlare workers
        - Possibly tie into Google sheets? Email?
    2. Google Forms
        - [x] Figure out embed
        - [x] Add shortcode for embed
        - **Formatting is terrible**
        - Can extract HTML elements from something like: https://stefano.brilli.me/google-forms-html-exporter/
        - Not user-friendly. Field names abtruse Should be able to replicate in SveltiaUI and/or Hugo
        - [x] Verify working for sample Google Form with HTML form elements
- General formatting
    - [x] Titles on non-home, non-list pages no longer centered
    - [ ] Properly include menu on custom `single.html` and `term.html` pages
- Mobile formatting
    - Revisit menu collapse
    - All-caps more intrusive on mobile
- Improve social links
    - [x] Setup Facebook link properly in Contact page
    - [x] PayPal link as button
    - [ ] See [this repo](https://github.com/squidfingers/hugo-shortcodes/blob/main/layouts/_shortcodes/icon.html) for nesting
- Support page needs lots of formatting work
    - Stylesheet to auto-adjust (no `{.purple}` tags)
- Shortcode errors (see below)
- Shortcode nesting issues
    - Center shortcode block doesn't work well
    - Solution to the errors above might run into this
    - Don't really want to enable HTML in markdown mix
- Model changes
  - Video playlists

### Shortcode errors
The columns/column/endcolumns have errors as they're split into 3 separate files. Maybe look into making it a single shortcode

One option would be to process as something like:
```hugo
{{< columns >}}
Left
---
{.column-break}
Right
{{< /columns >}}
```

Then in the shortcode, split on the column break and render properly
