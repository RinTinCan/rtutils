## WebKitGTK+

This is a replacement for the `library/desktop/webkitgtk4` package found
in the Solaris userland gate.

This package provides the latest stable webkitgtk4, which is needed
to build the epiphany browser (available in this repo).

RocketMan's patches for 2.22.x to fix JIT and the scroll bar warp have
been pushed upstream.  As of WebKitGTK+ 2.24.0, they are included in
the upstream release!

## Requirements

To build WebKitGTK+, you will need [GStreamer 1.14.4](../gstreamer/)
or later, available in this repo.  Specifically, the packages
`gstreamer`, `gst-plugins-base`, and `gst-plugins-good` are required.
(It is no longer necessary to have `gst-plugins-bad` for GL support in
WebKit.)

By default, this package depends on the icu from the userland gate.
If you are running under 11.3 and have dependencies on the existing
icu, then build the [icu-gcc](../../icu-gcc) in this repo and uncomment
the relevant lines in the Makefile to use it.

**Note:** WebKitGTK+ 2.26.0 seems to have some irregularities in media
presentation under Solaris.  If you experience any issues, revert to
version 2.24.4 (in this repo tagged as webkitgtk-2.24.4)

## Screenshot
![screenshot](https://raw.githubusercontent.com/RocketMan/solaris-ports/master/components/desktop/webkitgtk4/screenshot.png "Epiphany/WebKitGTK+")
