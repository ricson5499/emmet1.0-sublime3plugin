# emmet1.0-sublime3 plugin
Including previous emmet 1.0 stable version plugin for Sublime Text 3 and teaching how to revert all corrupt version back to normal

*Important, this emmet version is only try help fix those user that have problem on sublime (snippet corrupted, shortcut no working, dun wish to update)
For the rest please try to use the new emmet version.

1. Open Package Control.sublime-settings from
Preferences -> Package Setting -> Package Control -> Setting - User
Includ this code

`{
"auto_upgrade_ignore": [
	"Emmet",
	"Emmet Css Snippets"
	]
}`
  
remember to put a coma if there habve a exisiting element before this. eg.

`{
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
}`

For how to recover snippet to old version
Preferences -> Package Settings -> Emmet -> Setting - User
The old Emmet.sublime-settings structure

`{
	"snippets": {	
		"html": {
			"snippets": {},
			"abbreviations": {}
		}
	}
}`

new one for you to compare.
`{
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
}`

for key binding, if you haven add in the new binding, then it should work. If not, just remove it.
Preferences -> Key Bindings
`
e.g.
ctrl+e
ctrl+alt+enter
`
from your User keymap if you just recently added for the new version.

After that, replace emmet package, before replace this you can init a repo there to keep all the file version, so next time when you want to revert anything you can do the same way.
My portable sublime text 3 is under H:\Sublime Text Build 3211 x64\Data\Installed Packages\

*At last, please, try to backup the file before replacing, i will not promise this will fix your issue. :D
