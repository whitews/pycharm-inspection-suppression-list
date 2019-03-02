# List of strings to suppress PyCharm inspections
[Click here for a table listing text strings for suppressing inspections in PyCharm](https://github.com/whitews/pc-inspection-suppression-list/blob/master/suppress-inspection.csv "View List")

**If you find this a useful reference, please submit a pull request with descriptions for any undocumented suppression strings.**

Inspection suppression strings can be found in the PyBundle.properties file inside the pycharm.jar bundle. Grep for comments including the string "Inspection":

    grep Inspection pycharm/com/jetbrains/python/PyBundle.properties | grep ^#
