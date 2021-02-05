---
title: Step by Step
parent: ubem.io
nav_order: 2
---

Let's go over each step from uploading your files to downloading the umi project at the
very end.

# Upload GIS file

Todo: Zipped Files (No internal folder). Give an example how to make a good zip file.
Todo: Can upload geojson directly.

# Attribute Grouping

Unique Identifier (ID)

Building Height [m]

Primary Grouping

Secondary Grouping can be N/A

# Organize Buildings

Sort buildings into groups that you wish to be of the same archetype / be assigned the
same building template for the simulation.

todo: Range editing

{: .hint }

> It is possible to not select any templates.
>
> In this case, the umi project will not contain any
> [Template Library Files](../template_library/index.md#the-template-library-file) and a
> user can import one of their own. In Rhino, the following warning will be shown:
>
> ![107074015-1fca6a00-67b6-11eb-9c3d-4bf7dbb40136](/umiverse-docs/assets/images/107074015-1fca6a00-67b6-11eb-9c3d-4bf7dbb40136.png)
> {: .d-flex.flex-justify-around }

# Assign Values and Templates

Assign building templates to each of the groups you identified.

{: .hint }

> It is also possible to input the template names manually. For users who wish to assign
> templates by name, this can now be done at step 4 (
> [Organize Buildings](#organize-buildings)) under the ArchetypeID column. The name must
> match perfectly the
> [building template name](../template_library/building_template.md#building-template) in
> the UMI Template Library File. Then users can go directly to the download umi project
> page without choosing any templates.

# Verify and Export

Verify and download the UMI model of your building stock. The table bellow is a summary of
simulation parameters for each building.
