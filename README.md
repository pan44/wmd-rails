# WMD Editor for rails

Using assets pipeline, base on https://github.com/chloerei/wmd version, witch fork from https://github.com/ChiperSoft/wmd .

## History

Original WMD and Showdwon code copyright (c) 2007 John Fraser  
Modifications and bugfixes (c) 2009-2010 Chris Jester-Young, Dana Robinson, Anand Chitipothu  
Further modifications (c) 2010-2011 Jarvis Badgley, Wenqiang Wang, Helder Ribeiro, Chad Burggraf

## Dependency

Rails 3.1 or higher

## Install

In you Gemfile

```ruby
gem 'wmd-rails'
```

Then `bundle install`

## Usage

In app/assets/javascripts/editor.js or other js

```javascript
//= require wmd/wmd
//= require wmd/showdown

$(function(){
  new WMDEditor({
    input: "editor-input",
    button_bar: "editor-button-bar",
    preview: "editor-preview",
    helpLink: "http://daringfireball.net/projects/markdown/syntax"
  });
})
```

More wmd document: https://github.com/chloerei/wmd

In app/assets/stylesheets/editor.css or other css

```css
/*
 *= require 'wmd/wmd'
*/
```

## Precompile (optional)

In config/application.rb

```ruby
config.assets.precompile += %w(editor.js editor.css)
```

Then `rake assets:precompile`

## LICENSE

MIT-LICENSE
