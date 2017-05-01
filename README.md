
# ucsb-cs-ce-profiles.github.io

Profiles of CS and CE alums, as well as current undergrads doing interesting work in research, internships, student orgs, etc.

# To contribute

1. Fork the repo
2. Add an .md file for your profile under the appropriate directory, following the naming convention (`lastname_firstname.md`) 
3. Add the "front matter", i.e. the part that looks like this.  Be sure it starts and ends exactly with the three hyphens `---`, and that the rest is key value pairs with the appropriate syntax.   For most folks, the degree will be either `BS CS` or `BS CE`.   For other degrees, e.g. 5 year BS/MS, various BA degrees that were offered in the past, etc., see the guide in the section below.
   ```
   ---
   name: "Chris Gaucho"
   affiliation: "Awesome Computer Company, Inc."
   city: "San Mateo, CA"
   class_of: "2012"
   ucsb_degrees: "BS CS"
   ---
   ```
4. Add a subdirectory that has the same name as your .md file (i.e. `lastname_firstname`).  In that subdirectory, put a file called `orig.jpg`, `orig.png`, or `orig.gif` that has a good picture of you.  This one can be at any reasonable resolution and size.

5. (Optional, but helpful).   Create jpg versions that are 300 pixels and 50 pixels high (width is whatever is needed to preserve the aspect ratio), with the names `300h.jpg` and `50h.jpg`.   (If you obtain the free and open source program ImageMagick, you can do this at the command line quickly and easily---see below.)  If you don't do this, then the webmasters of the site will do it for you.

6. Do a pull request to incorporate your bio into the site.

# How to abbreviate various degrees

| Degree | Abbreviation | Notes |
|---|---|---|
| Bachelors of Science in Computer Science | `"BS CS"` |  |
| Bachelors of Science in Computer Engineering | `"BS CE"` |  |
| 5 year combined BS/MS program in Computer Science | `"BS/MS CS"` | For `class_of`, use the year you completed the MS |
| Bachelor of Arts in Computer Science with Emphasis in Computational Biology, Geography or Economics | `"BA CS"` | Put the fact that your emphasis was in Computational Biology, Geography, or Economics in your bio.|
| Any BS degree or BS/MS in CS, followed by completion of Ph.D. degree from UCSB | "BS CS" or "BS/MS CS" | For `class_of`, use the year you completed your BS or the combined "BS/MS".  Mention the Ph.D. studies in your biography |


# Technical Details

This is a Jekyll-based website

website: https://ucsb-cs-ce-profiles.github.io

To test locally:
* One time setup:
    * `git clone` the repo
    * Install rvm (the Ruby version manager)
    * Run `./setup.sh` to install correct ruby version, bundler version, and bundle the gems
* From then on, to test the site locally:
    * Run `./jekyll.sh
    * Point browser to localhost:4000

# Resizing images with Imagemagick

The `convert` command line utility is available in the Imagemagick package,
which is available on CSIL, and can be [installed on Mac via homebrew](http://stackoverflow.com/questions/7053996/how-do-i-install-imagemagick-with-homebrew)

To convert orig.jpg of arbitrary size to 300 pixels of height, while maintaining aspect ration, use:

```
convert -resize x300 orig.jpg 300h.jpg
convert -resize x50 orig.jpg 50h.jpg
```

If your original image is a png or gif, this still works:

```
convert -resize x300 orig.png 300h.jpg
convert -resize x50 orig.png 50h.jpg
convert orig.png orig.jpg
```

OR

```
convert -resize x300 orig.gif 300h.jpg
convert -resize x50 orig.gif 50h.jpg
convert orig.gif orig.jpg
```

# Creating a blank image as a placeholder

If a contributor doesn't provide an image, a blank placeholder can be created
like this:

```
convert -size 300x300 xc:white orig.jpg
```