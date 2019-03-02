# List of strings to suppress PyCharm inspections
[Click here for a table listing text strings for suppressing inspections in PyCharm](https://github.com/whitews/pc-inspection-suppression-list/blob/master/suppress-inspection.csv "View List")

**If you find this a useful reference, please submit a pull request with descriptions for any undocumented suppression strings.**

Inspection suppression strings can be found in the PyBundle.properties file inside the pycharm.jar bundle. Grep for comments including the string "Inspection":

    grep Inspection pycharm/com/jetbrains/python/PyBundle.properties | grep ^#

## How to suppress inspections in PyCharm

For any inspection warning that you wish to suppress, include a commented line beginning with `noinspection`, followed by the appropriate inspection string. Say you have an import that PyCharm complains about, yet you know it is satisfied by your setup file or requirements.txt file. In my experience, this happens for various NumPy or cv2 methods, or with the PIL library (because the package name differs from its import string). To suppress the inspection warning, add the suppression string on the line just before the offending code, like so:

```
# noinspection PyPackageRequirements
import cv2
```
