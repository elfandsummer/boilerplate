# 前端代码格式化配置（sublime）

## 插件安装:
* 打开sublime,Tools->Command Palette…(快捷键：Ctrl+Shift+P)

![](./docs/image/1.jpg)

* 搜索Install Package Control并单击安装

![](./docs/image/2.jpg)

* Preferences->PackageControl，搜索installpackage并单击，进入插件查找界面

![](./docs/image/3.jpg)

![](./docs/image/4.jpg)

* 搜索Html-css-js prettify，单击安装

![](./docs/image/5.jpg)

## 插件格式化规则配置：

* Preferences->package setting->Html-css-js prettify->Set Prettify Preferences
* 用以下代码替换掉原来所有代码

![](./docs/image/6.jpg)

```
{
  // The plugin looks for a .jsbeautifyrc file in the same directory as the
  // source file you're prettifying (or any directory above if it doesn't exist,
  // or in your home folder if everything else fails) and uses those options
  // along the default ones.
  // Details: https://github.com/victorporof/Sublime-HTMLPrettify#using-your-own-jsbeautifyrc-options
  // Documentation: https://github.com/einars/js-beautify/
  "html": {
    "allowed_file_extensions": ["htm", "html", "xhtml", "shtml", "xml", "svg"],
    "brace_style": "collapse", // [collapse|expand|end-expand|none] Put braces on the same line as control statements (default), or put braces on own line (Allman / ANSI style), or just put end braces on own line, or attempt to keep them where they are
    "end_with_newline": false, // End output with newline
    "indent_char": " ", // Indentation character
    "indent_handlebars": false, // e.g. {{#foo}}, {{/foo}}
    "indent_inner_html": false, // Indent <head> and <body> sections
    "indent_scripts": "normal", // [keep|separate|normal]
    "indent_size": 2, // Indentation size
    "max_preserve_newlines": 2, // Maximum number of line breaks to be preserved in one chunk (0 disables)
    "preserve_newlines": true, // Whether existing line breaks before elements should be preserved (only works before elements, not inside tags or for text)
    "unformatted": ["a", "span", "img", "code", "pre", "sub", "sup", "em", "strong", "b", "i", "u", "strike", "big", "small", "pre", "h1", "h2", "h3", "h4", "h5", "h6"], // List of tags that should not be reformatted
    "wrap_line_length": 0 // Lines should wrap at next opportunity after this number of characters (0 disables)
  },
  "css": {
    "allowed_file_extensions": ["css", "scss", "sass", "less"],
    "end_with_newline": false, // End output with newline
    "indent_char": " ", // Indentation character
    "indent_size": 2, // Indentation size
    "newline_between_rules": true, // Add a new line after every css rule
    "selector_separator": " ",
    "selector_separator_newline": true // Separate selectors with newline or not (e.g. "a,\nbr" or "a, br")
  },
  "js": {
    "allowed_file_extensions": ["js", "json", "jshintrc", "jsbeautifyrc"],
    // Set brace_style
    //  collapse: (old default) Put braces on the same line as control statements
    //  collapse-preserve-inline: (new default) Same as collapse but better support for ES6 destructuring and other features. https://github.com/victorporof/Sublime-HTMLPrettify/issues/231
    //  expand: Put braces on own line (Allman / ANSI style)
    //  end-expand: Put end braces on own line
    //  none: Keep them where they are
    "brace_style": "collapse-preserve-inline",
    "break_chained_methods": false, // Break chained method calls across subsequent lines
    "e4x": true, // Pass E4X xml literals through untouched
    "end_with_newline": false, // End output with newline
    "indent_char": " ", // Indentation character
    "indent_level": 0, // Initial indentation level
    "indent_size": 2, // Indentation size
    "indent_with_tabs": false, // Indent with tabs, overrides `indent_size` and `indent_char`
    "jslint_happy": false, // If true, then jslint-stricter mode is enforced
    "keep_array_indentation": false, // Preserve array indentation
    "keep_function_indentation": false, // Preserve function indentation
    "max_preserve_newlines": 2, // Maximum number of line breaks to be preserved in one chunk (0 disables)
    "preserve_newlines": true, // Whether existing line breaks should be preserved
    "space_after_anon_function": false, // Should the space before an anonymous function's parens be added, "function()" vs "function ()"
    "space_before_conditional": true, // Should the space before conditional statement be added, "if(true)" vs "if (true)"
    "space_in_empty_paren": false, // Add padding spaces within empty paren, "f()" vs "f( )"
    "space_in_paren": false, // Add padding spaces within paren, ie. f( a, b )
    "unescape_strings": false, // Should printable characters in strings encoded in \xNN notation be unescaped, "example" vs "\x65\x78\x61\x6d\x70\x6c\x65"
    "wrap_line_length": 0 // Lines should wrap at next opportunity after this number of characters (0 disables)
  }
}
```


* 还需要配置node路径 ，Preferences->package setting->Html-css-js prettify->Set Plug Options

![](./docs/image/7.jpg)

* 将format_on_save属性置为true，就可以在保存代码时自动格式化代码

![](./docs/image/8.jpg)

* 完成以上配置后，在sublime编辑（html/css/js）代码时就可以通过右键格式化代码

![](./docs/image/9.jpg)

