+++
title = "How I made the Growing Wiki (and how it works)"
author = ["James"]
date = 2025-12-27T15:58:00+00:00
draft = false
+++

## <span class="org-todo todo TODO">TODO</span> Content {#content}

This website is essentially my notebook that's kept in the open for everyone and anyone to see. I treat this as something like an [Obsidian](https://obsidian.md/) vault.
The only difference being that it's public. I designed it to be this way to keep it as simple as possible, to reduce the friction to write and publish.

My workflow is something like:

<style>.org-center { margin-left: auto; margin-right: auto; text-align: center; }</style>

<div class="org-center">

`Write / Edit → Sync → Publish`

</div>

The underlined tools and programmes that I use are:

[Emacs](/emacs/#content) ( [Doom Emacs](https://github.com/doomemacs/doomemacs) )
: For editing `.org` files, which is the base file format.

[Ox-Hugo](https://ox-hugo.scripter.co/)
: For exporting `.org` files to `.md` files.

[Hugo](https://gohugo.io/)
: Static site generator, or _"The world's fastest framework for building websites"_.

Git ( and currently [GitHub](https://github.com) )
: For version control and syncing remotely.

[Cloudflare](https:www.cloudflare.com)
: For domain management and hosting.
