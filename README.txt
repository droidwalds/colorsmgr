An rc23-script for managing base16 colors configs

Usage guide:
	- You must have ~/.config/colorsmgr/config.rc, which will
	be sourced by script.
	- In config.rc you must to define:
		1. A 'colors' rc23 list
		2. A 'generators' rc23 list
		(for rc23 guide see man rc23, its very small manpage)
	- In colors list you must to define 16 colors in rrggbb format
	- In generators list you must to define paths to executables, which
	will generates configs (like colors.kdl or colors.toml)

Generators guide:
	- Generator gets these arguments:
		1. 16 colors (one per arg)
		2. Output directory (by default its ~/.config/colorsmgr/out)
	- Generator must write a config by self to a file in output
	directory

Examples for config and kdl generator is included in this repo
