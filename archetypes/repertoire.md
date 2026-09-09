---
id: '{{ replace .File.ContentBaseName " " "-" }}'
title: '{{ replace .File.ContentBaseName "-" " " | title }}'
composer: # or generic (Spiritual, etc)
arranger: # for "arr. ~"
adapted: # for "Adapted by ~"
sheet_music: # URL
# Note, will back-fill from performances for videos
# Could use body for optional type, or an into
---
