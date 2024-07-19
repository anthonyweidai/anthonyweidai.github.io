This is a folk from a Github Pages template for academic websites (https://github.com/OleVik/personal-academic-website),  which was again forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md. Meanwhile, I took [xingjunm](https://github.com/xingjunm)/**[xingjunm.github.io](https://github.com/xingjunm/xingjunm.github.io)** and [a-paxton](https://github.com/a-paxton)/**[a-paxton.github.io](https://github.com/a-paxton/a-paxton.github.io)** as reference.

# I want to write something for Windows users

## Environment configuration

* Download Ruby in [RugbyInstaller](https://rubyinstaller.org/downloads/). I selected [Ruby+Devkit 2.7.3-1 (x64)](https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-2.7.3-1/rubyinstaller-devkit-2.7.3-1-x64.exe) , which is regarded as compatible version by official.

* Download bundler, type the following command and run in command windows:

  ```
  gem install bundler
  ```

* Download node.js in https://nodejs.org/en/.

## Run Locally

- Run the following in command windows


```
bundle clean
```

(no need to use --force)

```
bundle install --verbose
```

- If it occurs [Unable to load the EventMachine C extension; To use the pure-ruby reactor, require 'em/pure_ruby'](https://github.com/oneclick/rubyinstaller2/issues/96), then fix it by：

In your ruby installing path, like

  ```
S:\Ruby27-x64\lib\ruby\gems\2.7.0\gems\eventmachine-1.2.7-x64-mingw32\lib
  ```

Add the following command on the first line of the file **eventmachine.rb**

  ```
require 'em/pure_ruby' if not defined?(EventMachine)
  ```

or try:

```
gem uninstall eventmachine
gem install eventmachine --platform ruby
bundle install
```

- Run

```
bundle exec jekyll serve -l
bundle exec jekyll liveserve
```

# Other bugs fixing advice

## Bundler v2 is running, but your lockfile was generated with v1. Installing Bundler v1 and restarting using that version.

Delete  Gemfile.lock

## Why I can not see icon images such as GitHub icon when I deploy my page?

The cause of the problem is that html webpage cannot find the icons.

What you need to do is: put the following codes in any free space of **_includes/head.html**, if you fork from my repo, you won't get the problem.

```html
<link rel="stylesheet" href="{{ base_path }}/assets/css/academicons.min.css"/>
```

and

```html
<script src="https://kit.fontawesome.com/42df25671e.js" crossorigin="anonymous"></script>
```

I think the character **42df25671e** is from my registered account. Thus, you are recommended to register fa account to get your own one. And it is free: https://fontawesome.com/start

Or, you use the wrong code to call it, eg. github icon

```html
<i class="fab fa-github"></i>
```

I was wrong because I used

```html
<i class="fa fa-github"></i>
```

Recently, I found that if I doesn't **open private network**, I also can't see these "Font Awesome icons". In other words, it is nothing about the problem of your source codes.

## ERROR NoMethodError: undefined method `key?' for nil

Use gem "jekyll", "3.9.3" in Gemfile

## No source of timezone data could be found. Exception on jekyll serve (Uninitialized constant) 


```c
`rescue in create_default_data_source': No source of timezone data could be found. (TZInfo::DataSourceNotFound)
```

Add the following commands in Gemfile

```c
platforms :mingw, :x64_mingw, :mswin, :jruby do
  gem 'tzinfo', '>= 1', '< 3'
  gem 'tzinfo-data'
end
```

## An error occurred while installing wdm (0.1.1), and Bundler cannot continue.

```c
gem install wdm -- --with-cflags=-Wno-implicit-function-declaration
or
gem install wdm --platform=ruby
```

## For  more information about pages' icons

The packages are free to use:

[Academicons](https://jpswalsh.github.io/academicons/)

[Font Awesome](https://fontawesome.com/)
