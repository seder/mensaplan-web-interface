Web UI for the canteens of Ulm University and other institutions where the Studierendenwerk Ulm organises the food supply.

This UI is active in test mode and can be found here: http://uni-ulm.de/mensaplan/beta

# Usage

The plan can be configured through setting the anchor or by using the UI elements which in turn change the anchor.

The anchor is structured as follows: #\<facility\>&\<date\>&\<refresh\>

The order and positions are fixed.

## Facility 

Facility can be one of the following:

> Mensa, Bistro, West, Diner, Burgerbar, Prittwitzstr, CB

If no argument is given, Mensa will be used as default. This list might be extended when the parser is extended.

## Date

Date can be a date in the form YYYY-MM-DD (ISO 8601) or can be one of the following:

> tomorrow, yesterday, today, heute, gestern, morgen, next

* If no argument is given, today/heute will be used as default.
* "next" means, that the plan of the mensa will be shown of the next time the facility is open. So during or before opening hours, today's plan and after the facility closes tomorrow's plan (or the plan for the next day the facility opens).

In any case: if the facility is closed at that day, the data from the next time it is open will be shown, given that the data is present. 

## Refresh

Refresh can be "refresh" or not set (undefined). If it is set, the plan will be refreshed every ten minutes. This can be used for static displays e.g. in the institute coffee kitchen or the student union office.

## Examples

>\<no anchor\>

Does the same as

>\#Mensa&today

>\#Mensa&heute

and the same as

>\#Mensa&next

during and before opening hours and

>\#Mensa&YYYY-MM-DD

where YYYY-MM-DD is today's date.
