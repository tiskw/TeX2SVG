TeX2SVG
================================================================================

Converter from Tex source file to SVG image file.
This software allow us to insert TeX expressions on vector graphic editor,
like Inkscape.


Requirement
--------------------------------------------------------------------------------

- Python >= 3.6.5
- Potrace >= 1.14
- pdfTeX >= 3.14159265-2.6-1.40.18 (TeX Live 2017/Debian)
- dvipng >= 1.15


Installation
--------------------------------------------------------------------------------

tex2svg needs Python3, Potrace and TeX distribution like TeXLive.
You can install these softwares on Ubuntu if you don't have it:

```console
$ apt install python3 potrace texlive-bin
```

If you prefer mathmetical font other than computer modern, you need to install
other mathematical tex fonts. You can install extra mathematical fonts by
the following command if you are using texlive on Ubuntu:

```console
$ apt install texlive-fonts-extra texlive-science
```


Usage
--------------------------------------------------------------------------------

The following command generate SVG image which is correspond to
the TeX command '$f(x) = x^2$'.

```console
$ ./tex2svg '$f(x) = x^2$'
```

Default output file is `tex2svg_TIMESTAMP.svg`, and you can change output
filename by `-o` option:

```console
$ ./tex2svg '$f(x) = x^2$' -o output.svg
```

Also you can change the math font by `-f` option:

```console
$ ./tex2svg '$f(x) = x^2$' -o output.svg -f txfonts
```

You can see all available font name by `-l` option:

```console
$ ./tex2svg -l
```


License
--------------------------------------------------------------------------------

MIT License (https://opensource.org/licenses/mit-license.php)


Author
--------------------------------------------------------------------------------

Tetsuya Ishikawa ([EMail](mailto:tiskw111@gmail.com), [Website](https://tiskw.github.io/about_en.html))
