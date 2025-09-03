# rafaeljaime.github.io

Local development instructions (Windows):

1) Install prerequisites
	- Ruby (use RubyInstaller for Windows)
	- MSYS2 toolchain (offered by RubyInstaller at the end; accept and install)
	- Git

2) Install bundler and dependencies
	- Open PowerShell in the repo folder.
	- Run:
	  - `gem install bundler`
	  - `bundle install`

3) Serve locally with livereload
	- Run: `bundle exec jekyll serve --livereload`
	- Open: http://127.0.0.1:4000/
