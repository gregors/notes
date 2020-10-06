# Wget

## Backing up web site

[Linux journal](https://www.linuxjournal.com/content/downloading-entire-web-site-wget)

```bash
wget \
   --recursive \
   --no-clobber \
   --page-requisites \
   --html-extension \
   --convert-links \
   --domains website.org \
   --no-parent \
   --random-wait \
   www.website.org/tutorials/html/
```

--recursive: download the entire Web site.
--domains website.org: don't follow links outside website.org.
--no-parent: don't follow links outside the directory tutorials/html/.
--page-requisites: get all the elements that compose the page (images, CSS and so on).
--html-extension: save files with the .html extension.
--convert-links: convert links so that they work locally, off-line.  --no-clobber: don't overwrite any existing files (used in case the download is interrupted and resumed).

In the comments
 --random-wait
 -r -p -e robots=off -U
