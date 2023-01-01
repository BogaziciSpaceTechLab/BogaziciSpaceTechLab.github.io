This repository hosts our [LAB Website](https://BogaziciSpaceTechLab.github.io/).

Yiğit Günsür Elmacıoğlu created this website using Jekyll and github repo of [AcademicPages](https://github.com/academicpages/academicpages.github.io) for the main template. There are no single template for the entire website but many alternative website layouts have been used for different pages. Most of them can be found on [Jekyll Themes](http://jekyllthemes.org).

A Github Pages template for academic websites. This was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md.

## For future contributors
Journal articles, conference preceedings, projects etc. are stored using collections of Jekyll. If you want to add a new project just copy/paste some existing one and change it according to your needs. It will be automatically added to the main list in reverse chronological order. For the publications which are currently being prepared, include them in publication-prep folder and once it is published cut/paste it to publications folder. When transfering the existing data from [old page](http://bustlab.boun.edu.tr/)  to new one, I named files as "paper-1.md" but you don't have to use that notation, it was just to accelerate the process. Only the date of the publication, project, person etc. affects the order of the item in the list.

For neatness, I used 16:9 aspect ratio for the cover pictures of the projects. You can use the default image editor of windows to crop your image quickly. People photos have 1:1 ratio, please use consistent images to prevent any unpleasant results.

If you ever need to add another collection, i.e. ted-x talks, you need to,
1. create a folder by the name of your collection having a _ at the beginning
2. use some existing collection element as template
3. add
```
  collections:
    CollectionName:
      output: true
      permalink: /:collection/:path/
```  
  and
```
  defaults: 
    # _CollectionName
    - scope:
        path: ""
        type: CollectionName
      values:
        layout: single
        author_profile: true
```
  in _config.xml file. **defaults:** and **collectons:** lines are already exist, just add the rest to the end.

4. Each element of the collection has to include 
```  
  collection: CollectionName
```  

5. to create a for loop to show list items, you can use a code like
```
{% for post in site.CollectionName reversed %}
  {% include archive-CollectionName.html %}
{% endfor %}
```
**archive-CollectionName.html** file should be in the *include* folder. If you want, you can use an existing file like archive-publication.html. To change layout of the display to a completely different one, you have to learn css and html (don't worry they are very simple). 

### Create Local Server
If you are planning to make substantial changes, using a local server on your PC may highly increase the speed of your process. Unfortunately, most techniques for creating a local server doesn't work for Jekyll. Please follow the steps in [https://jekyllrb.com/docs/installation/windows/](https://jekyllrb.com/docs/installation/windows/) to install Jekyll to your windows PC. Once you are happy with the result, you can simply push it to Github and this will update the website in a couple of minutes. The progress can be checked from *Actions* segment of the repo.
