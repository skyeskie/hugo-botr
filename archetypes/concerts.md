---
year: 2026
season: December # Season or month?
extra: '' # ex: Area 11 Festival
weight: 2026Winter # Note: sorted DESCENDING
title: Program Title
# Displays as "Season 2026 - Program Title" in index
dates: # Repeat as needed
  - id: location12 # Reference for videos. Auto-gen from location and day?
    # Option to omit time?
    # If no, separate date/time fields so can have TBA
    date: 2026-12-12 16:00
    location: ref-location # Omit for TBA
selections:
  - piece-id: ref-repertoire
    subtitle: Optional
    instrumentalists:
      - Instrument: Instrumentalist
      # Alternative form?
      # Option to reference Ringer?
      - what: Instrument
        who: Instrumentalist
    videos:
      - performance: location12 # ref from dates
        youtube: YoutubeID # See on site
        public: 2026-12-20 # Date to include link
---
