# Corebird

This is the readme for version 1.0.

## Shortcuts

| Key                | Description                                                                                                                                 |
| :-----:            | :-----------                                                                                                                                |
| `Ctrl + t`         | Compose Tweet                                                                                                                               |
| `Back`             | Go one page back (this can be triggered via the back button on the keyboard, the back thumb button on the mouse or  `Alt + Left`)           |
| `Forward`          | Go one page forward (this can be triggered via the forward button on the keyboard, the forward thumb button on the mouse or  `Alt + Right`) |
| `Alt + num`        | Go to page `num` (between 1 and 7 at the moment)                                                                                            |
| `Ctrl + Shift + s` | Show/Hide sidebar                                                                                                                           |
| `Ctrl + p`         | Show account settings                                                                                                                       |
| `Ctrl + k`         | Show account list                                                                                                                           |
| `Ctrl + Shift + p` | Show application settings                                                                                                                   |


  When a tweet is focused (via keynav):

  - `r`  - reply
  - `tt` - retweet
  - `f`  - favorite
  - `dd` - delete
  - `Return` - Show tweet details


## Will this work on distrubution XYZ?
  I don't know. If you can satisfy all the dependencies, probably yes but
  you'd most likely still have to compile and install it from source (that is,
  if no one else makes packages).

## Translations
  Since February 2014, there's a [Corebird project on Transifex](https://www.transifex.com/projects/p/corebird)


## Dependencies
 - `gtk+-3.0 >= 3.14`
 - `glib-2.0 >= 2.40`
 - `rest-0.7` (`>= 0.7.91` for image uploads)
 - `json-glib-1.0`
 - `sqlite3`
 - `libsoup-2.4`
 - `intltool >= 0.40`
 - `libgee-0.8`
 - `vala >= 0.26` (makedep)
 - `automake >= 1.14` (makedep)
 - `gstreamer-1.0` (disable via --disable-video, default enabled)
 - `gst-plugins-bad-1.0` (disable via --disable-video, default enabled)
 - `gst-plugins-good-1.0` (disable via --disable-video, default enabled)
 - `gst-libav-1.0` (disable via --disable-video, default enabled)

Note that the above packages are just rough estimations, the actual package names on your distribution may vary.

If you pass `--disable-video` to the configure script, you don't need any gstreamer dependency but  won't be able to view any videos (i.e. no vines and no twitter gifs).

## Compiling

```
./autogen.sh --prefix=/usr
make
make install
```

