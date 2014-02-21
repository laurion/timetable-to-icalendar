timetable-to-icalendar
======================

Exports school timetable to a calendar format

## Install

Install the icalendar module

`easy_install icalendar`

## Configure

Describe your timetable in a text file (see `FMI 134.txt`)
* first line the start and end dates of the semester
`17 02 2014  23 05 2014`
* second line the start and end dates of the exam period
`24 05 2014  13 06 2014`
* the next lines describe the classes in your timetable

Example:
```
	Algebra (S) - 214 
	2 18 20 2
```

		* first line is a summary:
			* the name of the class
			* the type of the class (S for seminar, C for course etc.)
			* and the classroom (214)
		* second line is a description:
			* day of the week (0 - monday, 1 - friday, ...)
			* start and end hour (18-20)
			* (optional) even or odd week (1 for odd, 2 for even)

## Run
```./convert < [inputfile] > [outputfile.ics]```

Example:
```./convert < FMI\ 134.txt > FMI\ 134.ics```
