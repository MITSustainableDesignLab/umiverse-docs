---
title: Template Library
nav_order: 7
has_children: true
has_toc: true
---

# The Template Library Editor

{: .no_toc }

<details open markdown="block">
  <summary>
    Table of contents
  </summary>
  {: .text-delta }
1. TOC
{:toc}
</details>

The Template Library Editor is an independent application provided with umi for the
creation, management and edition of Template Library Files (TLF). TLF files are the open
format used by umi to exchange and store information about materials, constructions,
schedules, thermal loads, spaces and buildings. This section explains the basic
characteristics of the TLF and the basic controls of the editor.

## The Template Library File

The Template Library File (TLF) is a `.json` type file with a specific structure in which
all building and space properties, both thermal and environmental, are stored for multiple
building types (.i.e building archetypes). It includes both a library of building
definitions, and libraries of all their data dependencies.

Within the file, these categories are listed as json objects, grouped by the previously
named types, and can be created and edited both through the use of the template editor,
and directly in any text edition software (See Figure below for a diagram of the data
structure). To know more about the TLF file format and its importance in building
performance simulation in design you can access the academic paper "Towards standardized
building properties template files for early design energy model generation", accessible
in the following
[link](http://web.mit.edu/sustainabledesignlab/publications/TemplateEditor_SimBuild2014.pdf).

![template_uml](/umiverse-docs/assets/images/template-uml.svg "Graph structure of template
library") *Source: Letellier-Duchesne, S. (2019). Planning and Integrated Design of Urban
Heat-Sharing Networks. Polytechnique Montréal.*

## Opening a TLF file and navigating contents

<div class="code-example" markdown="1">

### Opening from umi for Rhino

You can open the Template Library Editor, from the "Project" umi panel by clicking the
"Edit" button. The application will pop up in a separate window, and immediately open the
TLF file currently loaded in your umi file. If you did not change the original file, you
will see the default library file opened.

### Opening using standalone app

You can open the Template Library Editor directly from the Windows Start Menu.

The executable is located at `C:\UMI\UmiTemplateEditor.exe`.

</div>

Additional file management commands are accessible from the "File" menu at the top left.
You can open a different TLF by clicking "Open", and finding the file in the browser
window. You can as well save the file with a different name through "Save as". Finally you
can "Save" the file under its current name. Note that all changes you make on the library
will be lost if you do not save the file before closing the editor. If the file you modify
is the same one you have loaded in umi, changes will be immediately applied to your file,
but if you rename the file remember to load it in umi.

{: .hint }

> It is possible to copy components over to another library.
>
> Simply open another instance of the Template Library Editor and `drag & drop` one or
> more components from one window to the other.

## Adding and modifying components in a Template Library

Each component data type in a library file has different data fields accessible within the
Template Editor, used in different modules of umi. This section provides general
directions about how to manipulate these fields. However, in order to know more about the
specific meaning and interpretation of the fields, you can visit the "Embodied Energy" and
"Operational Energy" sections of this user guide.

