This is a means of learning [Hugo](https://gohugo.io) by making a rough clone of the 
[Bells of the Rockies](https://www.bellsoftherockies.org/) website.

The site currently uses custom modifications to the [Ananke](https://github.com/gohugo-ananke/ananke) theme

### WIP
- [x] Change defaults on most to text left-align
    - [x] Add shortcode to center text
- [x] Work on Image align
    - [x] Need to be shortcode?
    - [x] CSS for before/after
- [x] Add a banner/callout
    - [x] .full-ringers on audition page
- Concerts/repertoire auto
    - Repertoire to individual pages
    - [ ] Individual concert pages
    - Index for repertoire
    - [ ] Index for concert pages
    - [ ] Mark concert(s) to show on index page
- Forms: One of
    1. Standard HTML forms
        - Add shortcode in admin UI
        - Figure out action target
        - See if need to adjust action target code
    2. Google Forms
        - Figure out embed
        - Add shortcode for embed
- Mobile formatting
    - Revisit menu collapse
    - All-caps more intrusive on mobile
- Improve social links
    - Setup Facebook link properly in Contact page
    - PayPal link as button
- Support page needs lots of formatting work
    - Stylesheet to auto-adjust (no `{.purple}` tags)
- Admin rendering
    - Could theoretically do full page renders
    - Worth it or no?
    - [ ] Should at least get coloring
    - [ ] Reference main CSS?
- Admin Deployment
    - [x] Setup CF deployment as separate
    - [x] Remove from main hugo-botr
    - [ ] **Switch hugo-botr to review workflow**
- Shortcode errors (see below)
- Debug/fix Concert YouTube edit
  - shortcode seems broken, fix or prefer below
  - YouTube *playlist* on concert
    - Link with logo for individual songs
    - Can auto-pull/auto-match songs from playlist

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
