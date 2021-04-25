This is a folk from a Github Pages template for academic websites (https://github.com/OleVik/personal-academic-website),  which were again forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md.

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

