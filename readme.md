daysLeft
========

shows the days left in relation to a given date

Parameter
---------

```
usage: daysLeft [-h] -d DATE [-w] [-e EXCLUDEDAYS [EXCLUDEDAYS ...]] [-v]

gets days left in relation to a given date

optional arguments:
  -h, --help            show this help message and exit
  -d DATE, --date DATE  target date, format YYYY-mm-dd (default: None)
  -w, --excludeWeekends
                        exclude weekends (default: False)
  -e EXCLUDEDAYS [EXCLUDEDAYS ...], --excludeDays EXCLUDEDAYS [EXCLUDEDAYS ...]
                        exclude specific days, format YYYY-mm-dd (default:
                        None)
  -s SUBTRACTDAYS, --subtractDays SUBTRACTDAYS
                        substract days, not yet planed (e.g. holydays)
                        (default: None)
  -v, --verbose         show dates (default: False)
```

### Example

get days left from today (2016-05-11) until 2016-06-17 except weekends and holydays

```
$ daysLeft -d 2016-06-17 -w -e 2016-05-18 2016-05-27 2016-05-16 2016-05-26
23
```

get days left from today (2016-05-11) until 2016-06-17 except weekends and holydays. show all dates in range.

```
$ daysLeft -d 2016-06-17 -wv -e 2016-05-18 2016-05-27 2016-05-16 2016-05-26
['2016-06-17 00:00:00', '2016-06-16 00:00:00', '2016-06-15 00:00:00', '2016-06-14 00:00:00', '2016-06-13 00:00:00', '2016-06-10 00:00:00', '2016-06-09 00:00:00', '2016-06-08 00:00:00', '2016-06-07 00:00:00', '2016-06-06 00:00:00', '2016-06-03 00:00:00', '2016-06-02 00:00:00', '2016-06-01 00:00:00', '2016-05-31 00:00:00', '2016-05-30 00:00:00', '2016-05-25 00:00:00', '2016-05-24 00:00:00', '2016-05-23 00:00:00', '2016-05-20 00:00:00', '2016-05-19 00:00:00', '2016-05-17 00:00:00', '2016-05-13 00:00:00', '2016-05-12 00:00:00']
23
```

Contact
-------

Jan Frederik Hake, <jan_hake@gmx.de>. [@enter_haken](https://twitter.com/enter_haken) on Twitter.
