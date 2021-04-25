This is a folk from a Github Pages template for academic websites (https://github.com/OleVik/personal-academic-website),  which was again forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md. Meanwhile, I took [xingjunm](https://github.com/xingjunm)/**[xingjunm.github.io](https://github.com/xingjunm/xingjunm.github.io)** as reference.

## I want to write something for Windows users

### Environment configuration

* Download Ruby in [RugbyInstaller](https://rubyinstaller.org/downloads/). I selected [Ruby+Devkit 2.7.3-1 (x64)](https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-2.7.3-1/rubyinstaller-devkit-2.7.3-1-x64.exe) , which is regarded as compatible version by official.

* Download bundler, type the following command and run in command windows:

  ```
  gem install bundler
  ```

* Download node.js in https://nodejs.org/en/.

### Run Locally

- Run the following in command windows


```
bundle clean
```

(no need to use --force)

```
bundle install
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
bundle exec jekyll liveserve
```

## Other bug fixing advice

### Why I can not see icon images such as GitHub icon when I deploy my page?

The cause of the problem is that html webpage cannot find the icons.

What you need to do is: put the following codes in any free space of **_includes/head.html**, if you fork from my repo, you won't get the problem.

```html
<link rel="stylesheet" href="{{ base_path }}/assets/css/academicons.min.css"/>
```

and

<script src="https://kit.fontawesome.com/42df25671e.js" crossorigin="anonymous"></script>

I think the character **42df25671e** is from my registered account. Thus, you are recommended to register fa account to get your own one. And it is free: https://fontawesome.com/start

