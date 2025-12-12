+++
author = ["James"]
date = 2025-12-12T00:00:00+00:00
draft = false
+++

baseURL = ""
languageCode = "en-us"
title = "Growing Wiki"
theme = "little-ocean"
buildFuture = true

contentDir = "content"
publishDir = "public"

[permalinks]
posts = "_:title"
notes = "/notes_:slug"

[params]

[params.styles]

[markup]
  [markup.goldmark]
    [markup.goldmark.renderer]
      unsafe = true  # Allow HTML in markdown (for ox-hugo exports)
