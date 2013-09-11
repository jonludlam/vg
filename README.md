Vg — Declarative 2D vector graphics for OCaml
-------------------------------------------------------------------------------
Release %%VERSION%%

Vg is an OCaml module for declarative 2D vector graphics. In Vg,
images are values that denote functions mapping points of the
cartesian plane to colors. The module provides combinators to define
and compose these values.

Renderers for PDF, SVG and the HTML canvas are distributed with the
module. An API allows to implement new renderers.
     
Vg depends only on [Gg][1]. The SVG renderer has no dependency, the
PDF renderer depends on [Uutf][2] and [Otfm][3], the HTML canvas
renderer depends on [js_of_ocaml][4]. All these components are
distributed under the BSD3 license.
     
[1]: http://erratique.ch/software/gg
[2]: http://erratique.ch/software/uutf
[3]: http://erratique.ch/software/otfm
[4]: http://ocsigen.org/js_of_ocaml/ 

Home page: http://erratique.ch/software/vg
Contact: Daniel Bünzli `<daniel.buenzl i@erratique.ch>`


## Installation

Vg can be installed with `opam`:

    opam install uutf otfm js_of_ocaml vg  # all renderers
    opam install vg                        # SVG renderer only
    
If you don't use `opam` consult the [`opam`](opam) file for
build instructions and a complete specification of the dependencies.


## Documentation

The documentation and API reference is automatically generated by
`ocamldoc` from the interfaces. It can be consulted [online][5] and
there is a generated version in the `doc` directory of the
distribution.

[5]: http://erratique.ch/software/vg/doc/


## Sample programs and images

A database of sample images can be found in the `db` directory. An
online rendering of the database is available [here][6].

[6]: http://erratique.ch/software/vg/demos/rhtmlc.html

Sample programs are located in the `test` directory of the
distribution. They can be built with:

    ocamlbuild -use-ocamlfind tests.otarget

The resulting binaries are in `_build/test` :

- `rsvg.native`, renders images of the Vg image database to SVG files.
- `rpdf.native`, renders images of the Vg image database to PDF files.
- `min_svg.native`, minimal example to render an image to an SVG file. 
- `min_htmlc.byte`, minimal example to render with the HTML canvas.
