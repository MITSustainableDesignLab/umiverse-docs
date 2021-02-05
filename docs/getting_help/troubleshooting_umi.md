---
title: Troubleshooting umi
parent: Getting help
nav_order: 2
---

# Troubleshooting umi

While working with umi, you might encounter some warning or error messages. This chapter
provides the list of the known problem solutions and workarounds.

You can also find the recommendations for troubleshooting and performing basic diagnostics
of your working environment.



| Reported Problem                                                                                                                                                                                                                                           | Possible cause                                                | Solution                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| The following error message appears on your first attempt to start Rhino after installing umi : `Unexpected Decimal Separator`.<br>This error can sometimes result in this other error, crashing Rhino: `FATAL UNHANDLED EXCEPTION: System.IO.IOException` | Your computer is set to use `,` commas as the decimal symbol. | In Windows Region Panel -> Additional Settings, make sure `Decimal Symbol` is set to `.` period. |
|                                                                                                                                                                                                                                                            |                                                               |                                                                                                  |

