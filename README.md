# Autopage-recipes

This is the 'master' repo of [autopage](https://github.com/geeksville/autopage) recipes. By default, autopage will fetch recipes from this repo and try to add them to your running StreamController (if it sees you are running a supported application).

# A minimal app definition

A minimal app definition will look like:
```toml
[[match]]
class = "google-chrome" # Change to your window class name, see the output of "autobutton --listen" to see what the foreground app is using

[[button]]
icon = "home"
bottom = "Hello"
actions = [ { type = "Hello +Space world" } ] # Type "Hello world" as a macro

# you can add as many buttons as you like and provide defaults, see the documentation below...
```

App recipes are always named YOURAPPNAME.ap.toml.

# How to add a new app

Adding a new app is easy!

For example recipes see these:

* [VS code](https://github.com/geeksville/autopage-recipes/blob/main/app/code.ap.toml)
* [A game](https://github.com/geeksville/autopage-recipes/blob/main/game/oni.ap.toml) (Oxygen Not Included)
* [Chrome browser](https://github.com/geeksville/autopage-recipes/blob/main/app/chrome.ap.toml)

If you want to create a new recipe, the recommended steps are:

* Copy an existing similar app into your new myapp.ap.toml file.
* Add new button definitions as you see fit. For a graphical browser of icons see [here](https://fonts.google.com/icons?icon.platform=android&icon.set=Material+Icons).
* For a full 'specification' of what you can do in an ap.toml file, see [here](https://github.com/geeksville/autopage/blob/main/doc/example-shell.ap.toml).
* You can then run "autopage --force myapp.ap.toml" to test it (--force tells autopage to reapply any changes even if you already have that page loaded on your StreamController).
* Once you are happy with it, copy it into this repo and edit the root [ap.toml](ap.toml) file to include it in the repo.
* Send in a [pull-request](https://github.com/geeksville/autopage-recipes/pulls).
* Bask in your sense of accomplishment.

Copyright 2026 Kevin Hester, kevinh@geeksville.com.  [LGPL v3 license](LICENSE.md).