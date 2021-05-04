---
title: "About"
---
wxWidgets is an excellent framework that enables the creation of multi-platform
applications with and without a graphical user interface. There are several
applications that help create dialogs visually, even so, some practical problems
have led me to start the development of a new application. Those problems include,
the limited set of widgets or the impossibility to include non-graphical components.

wxFormBuilder aims to be an application that as well as enabling visual development
and generating the corresponding code, allow the inclusion of non-graphical components,
as well as providing facilities for extending the set of widgets easily via plugins,
like other applications such as qt-designer.

An interesting aspect of wxFormBuilder, is the storage of the information in XML
documents instead of embedding it in the code itself. This, as well as simplifying
the application’s code, eases the the further modification of both the properties
of an object and the generated code without needing to recompile.

The code generation makes use of a series of “templates” defined in the document
of the class information, which are processed to generate the corresponding code.
The code generator includes a small parser that allows us to use in the templates
a simple set of directive to be able to process functions such as referring
the an object’s properties, do a conditional code generation, bucles,
and other possibilities.

This way the application’s code is simplified while at the same time providing a
simple mechanism for adding components. The visual components also require the
implementation of a plugin to be able to use it in the visual editor, but that
doesn’t mean losing the ability to “personalize” the generation of code
(with templates) for that component and the plugin would be as simple as a routine
that creates an instance of the object based on the values of its properties.

## Developers

{%- include wxfb/team.liquid -%}
