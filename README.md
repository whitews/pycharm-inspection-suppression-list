# pc-inspection-suppression-list
[List of text strings for suppressing inspections in PyCharm](https://github.com/whitews/pc-inspection-suppression-list/blob/master/suppress-inspection.csv "View List")

These can be found in the PyBundle.properties file inside the pycharm.jar bundle. Just grep for comments with "Inspection":

grep Inspection pycharm/com/jetbrains/python/PyBundle.properties | grep -i ^#
