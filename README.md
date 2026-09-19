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
- Admin rendering
    - Could theoretically do full page renders
    - Worth it or no?
    - [ ] Should at least get coloring
    - [ ] Reference main CSS?
- Shortcode errors (see below)
- Debug/fix Concert YouTube edit
  - shortcode seems broken, need to fix
  - YouTube *playlist* on concert
    - [x] Link with logo for individual songs
    - Run to pull all playlists and videos, then have data for Admin UI to quick add
- Model changes
  - Video playlists
  - [x] External songs
    - ~~Option A: Have a direct text entry of some form~~
    - [x] Option B: Put in full repertoire, but exclude from indexing

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
