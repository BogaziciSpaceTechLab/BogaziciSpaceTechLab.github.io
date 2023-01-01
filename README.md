This repository hosts our [LAB Website](https://BogaziciSpaceTechLab.github.io/).

Yiğit Günsür Elmacıoğlu created this website using Jekyll and github repo of [AcademicPages](https://github.com/academicpages/academicpages.github.io) for the main template. There are no single template for the entire website but many alternative website layouts have been used for different pages. Most of them can be found on [Jekyll Themes](http://jekyllthemes.org).

A Github Pages template for academic websites. This was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md.

## For future contributers
Journal articles, conference preceedings, projects etc. are stored using collections of Jekyll. If you want to add a new project just copy/paste some existing one and change it according to your needs. It will be automatically added to the main list in reverse chronological order. For the publications which are currently being prepared, include them in publication-prep folder and once it is published cut/paste it to publications folder. When transfering the existing data from [old page](http://bustlab.boun.edu.tr/)  to new one, I named files as "paper-1.md" but you don't have to use that notation, it was just to accelerate the process. Only the date of the publication, project, person etc. affects the order of the item in the list.

For neatness, I used 16:9 aspect ratio for the cover pictures of the projects. You use the image editor of windows to crop your image quickly. People photos have 1:1 ratio, please use consistent images to prevent any unpleasant results.

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
