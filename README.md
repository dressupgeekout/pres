# pres -- Presentation software which sucks less

by Christian Koch -- cfkoch@sdf.lonestar.org

-----

**pres** is a stupid-simple slideshow presentation program thing written in
Ruby and Curses. In order for it to suck even less it should be written in
C, but at least this is written in non-sucky Ruby, using core and stdlib
only.

The `pres` executable takes one argument, which is a path to a presentation
file. This is a plain text file of slides, where each slide is separated
with a line containing nothing but a form feed (i.e., "\n\f\n"). Cool text
editors let you enter a literal form feed by typing ^L. It is the
presentation author's responsibility to make sure that the slides are
properly formatted (max. 23 lines and 80 columns per slide). The 24th line
is the "status indicator" (see below).

The first line of each slide is "stood out" (from Curses jargon), so it's
best to make that line the title of that particular slide. All other text is
written as-is. There's also a small status indicator at the bottom of the
display.

If you run `pres` without any arguments, it prints version information to
the standard output.

You navigate a slideshow with these key bindings:

  l, n -- next slide
  h, p -- previous slide
  q    -- quit


## Example presfile

    HOW TO OPEN A DOOR

    Foobar Quux
    January 1, 1999
    ^L
    PRELIMINARIES

    You need the following:

    - A door.
    - On a hinge.
    - A doorknob.
    
    I think you can figure it out from here.
    ^L
    THANK YOU!

    Questions?


## License (2-clause BSD-style)

Copyright (c) 2013 Christian Koch.
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:

  - Redistributions of source code must retain the above copyright notice,
    this list of conditions and the following disclaimer.

  - Redistributions in binary form must reproduce the above copyright
    notice, this list of conditions and the following disclaimer in the
    documentation and/or other materials provided with the distribution.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS"
AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE
IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE
ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE
LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR
CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF
SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS
INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN
CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE)
ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE
POSSIBILITY OF SUCH DAMAGE.
