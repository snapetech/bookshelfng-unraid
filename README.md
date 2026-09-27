# BookshelfNG for Unraid

This repository publishes the standalone BookshelfNG Unraid Docker template.
BookshelfNG is a Snapetech NG fork of Bookshelf for ebook and audiobook library
management and acquisition. It works independently; SeerrNG integration is optional.

## Community Apps submission

Submit this repository URL: https://github.com/snapetech/bookshelfng-unraid

Run Validate and Scan, then submit for review. The application source repository
contains unrelated XML test fixtures and should not be submitted as a template
repository. This repository contains one app XML and its repository profile.

## Installation and setup

Use the BookshelfNG entry once it is published in Community Apps. For a manual
install, use [the template XML](templates/bookshelfng.xml) with Unraid's Docker
template workflow. The image is `ghcr.io/snapetech/bookshelfng:hardcover`.

- Map persistent appdata to `/config` and your media to `/data`.
- Map downloads to `/download`, matching your download client's container paths.
- Set a personal Hardcover API token in `HARDCOVER_AUTH` or BookshelfNG settings.
- Open the web interface on port 8787 and configure indexers and download clients.
- One instance can manage ebooks and audiobooks. SeerrNG can use two service
  entries with the same URL and API key when requesting both formats.
- Existing Readarr or softcover databases require migration before using the
  Hardcover image; changing the image tag alone is not a migration.

## Source and support

- [BookshelfNG application source and documentation](https://github.com/snapetech/bookshelfng)
- [Unraid package and SeerrNG integration support](https://github.com/snapetech/seerrng/issues)

BookshelfNG is derived from Bookshelf and Readarr and distributed under GPLv3.
This template repository uses the same GPLv3 license.
