_confweb
---

This is a repository for easily creating conferences. To create your own conference create a repo in your username with your confname then type.

```
$ git clone --bare https://github.com/gpss/_confweb.git
$ cd _confweb.git
$ git push --mirror https://github.com/USERNAME/CONFNAME.git
$ cd ..
$ rm -rf _confweb.git
$ git clone https://github.com/USERNAME/CONFNAME.git
$ cd CONFNAME
$ git checkout gh-pages
```

Then you can clone the new website as normal.

The main settings can be found in the ```_config.yml``` file. They include conference location, name, year, days of operation.


A few layout files are provided by the base jekyll class, `gpschool/jekyll-theme`

```
_layouts/program.html
_layouts/single.html
_layouts/multi.html
_layouts/registration.html
_layouts/getting_there.html
_layouts/about.html
```

These dictate how the program is displayed. ```single.html``` and ```multi.html`` are for single and multiple track sessions. 

Also in the theme are some include files for bits of html which are need about the place.

```
_includes/listperson.html
_includes/listsponsor.html
_includes/listtalk.html
_includes/listmulti.html
_includes/listsingle.html
_includes/map.html
_includes/google_tracking_code.html
```

Then the sessions themselves are stored in the ```_posts``` directory. Each session is recorded as post in the format ```YYYY-MM-DD-session-name.md```, and inside each session is the list of speakers and talks. See example session for details.
