# emmet 1.0 Sublime Text 3 plugin
Including previous emmet 1.0 stable version plugin for Sublime Text 3 and teaching how to revert all corrupt version back to normal

*Important, this emmet version is only try to help those user that have problem to use emmet function on sublime text 3 (snippet corrupted, shortcut no working, dun wish to update)

For the rest please try to use the new emmet version.

## 1. Disable auto upgrade for emmet

Open Package Control.sublime-settings from

Preferences -> Package Setting -> Package Control -> Setting - User

Include this code

```
{
	"auto_upgrade_ignore": [
		"Emmet",
		"Emmet Css Snippets"
	]
}
```
  
remember to put a coma if there have a exisiting element before this. eg.

```
{
	"bootstrapped": true,
	"in_process_packages":
	[
	],
	"installed_packages":
	[
		"Autoprefixer",
		"ConvertToUTF8",
		"Emmet",
		"Emmet Css Snippets",
		"HTML (C#)",
		"HTML-CSS-JS Prettify",
		"jsonnet syntax",
		"Nodejs",
		"npm",
		"Package Control",
		"SublimeGit"
	],
	"auto_upgrade_ignore": [
		"Emmet",
		"Emmet Css Snippets"
	]
}
```



## 2. Recover snippet to old version

Preferences -> Package Settings -> Emmet -> Setting - User

The old Emmet.sublime-settings structure

```
{
	"snippets": {	
		"html": {
			"snippets": {},
			"abbreviations": {}
		}
	}
}
```

new one for you to compare.

```
{
    "config": {
        "markup": {
            "snippets": {
                "foo": "ul.foo>li.foo-item*4"
            },
            "options": {
                "output.tagCase": "upper"
            }
        },
        "html": {
            "snippets": {
                "myhtml": "main.my-html>section"
            }
        },
	"stylesheet": {
            "snippets": {
                "foo": "foo-bar"
            },
            "options": {
                "stylesheet.shortHex": false
            }
        },
        "css": {
            "snippets": {
                "prop": "some-prop:${value}"
            }
        }
    }
}
```

For my experience, if you updated your snippet to new structure before, and reload the sublime text 3, the structure may change, will include some more value there. So becareful on the open and close bracket.

## 3. Fix key binding

If you haven't add in the new binding, then it should work. If not, just remove it.

Preferences -> Key Bindings

```
e.g.
ctrl+e
ctrl+alt+enter
```

from your User keymap if you just recently added for the new version.

## 4. Replace Emmet package

After that, replace emmet package, before replace this you can init a repo there to keep all the file version, so next time when you want to revert anything you can do the same way.

My portable sublime text 3 is under H:\Sublime Text Build 3211 x64\Data\Installed Packages\

*At last, please, try to backup the file before replacing, i will not promise this will fix your issue. :D
