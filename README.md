Confweb
---

This is a repository for easily creating conferences. To create your own conference. Create a repo in your username with your confname then type.

```
$ git clone --bare https://github.com/sods/confweb.git
$ cd confweb.git
$ git push --mirrow https://github.com/username/confname.git
$ cd ..
$ rm -rf confweb.git
```

Then you can clone the new website as normal.

The main settings can be found in the ```_config.yml``` file.

