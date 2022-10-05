# Bibliography
+ Made paper titles into links by editing `_layouts/bib.html`: 
  + I changed `<div class="title">{{entry.title}}</div>` to `<div class="title"><a href="{{entry.html}}">{{entry.title}}</a></div>` and added `html = {URL-HERE},` to the entry in `papers.bib`. 
  + To remove the now redundant `html` button that will now appear, I commented out the lines `{%- if entry.html %} <a href="{{ entry.html }}" class="btn btn-sm z-depth-0" role="button">HTML</a>{%- endif %}` 

# Make "cv" in the navbar go directly to the pdf:
+ Right before the `{%- if site.enable_darkmode %}` in `_includes/header.html` add the following: 

        <li id="show-cv" class="nav-item">
          <a class="nav-link" target="_blank" href="{{ '/assets/pdf/CV.pdf' | prepend: site.baseurl | prepend: site.url }}">
          cv
          </a>
        </li> 
+ Set `nav: false` in `_pages/cv.md` so you don't end up with two cv pages

# Various changes in `_config.yml`
+ `rss_icon: false`
+ `footer_fixed: false`
+ Modify `footer_text` to be less verbose
+ `enable_navbar_social: true`
+ `last_updated: true`

# Misc. other small changes:
+ `social: false` in `_pages\about.md` to remove the social links at the bottom of the about page
+ `--global-bg-color: #{$white_color};` and `--global-theme-color: #{$purple-color};` and ` --global-hover-color: #{$purple-color};` for both light and dark (scoll down for dark) mode can be controlled from `_sass\_themes.scss` and the color available can be viewed or changed in `_sass\_variables.scss`
