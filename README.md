# Job title: Application Calendar 

## 📃 Content

- Description of semester work (:construction: in process)
- Required functionality (:construction: in process)
- Where can polymorphism be used? (:construction: in process)
- Other information / references ✅

# Description

This semester's work belongs to the category of interactive applications. Your goal is to create an application that the user interactively controls (e.g. using commands on standard input). Do not try to define any application parameters directly in the code (even using constants). Place them in the configuration files (one or more) that your program will load.

Your goal is to implement an application to manage calendars and events in them.

## Implement the following functionality:

* The calendar must display at least a daily, weekly and monthly overview of events.

* For events, we want to keep at least the following information: event name, date and time, duration, location, participants, tags, and a text note. As part of its implementation, you can add other interesting attributes (e.g. participation: compulsory, transferable, optional,...).

* Events can be one-time or recurring. Allow to define the frequency of repetitions at least at the level of days.

* The calendar must be able to search for events by individual attributes, including combinations containing the conjunctions " and " and "or"(e.g. events before 23.1.2022 and at the same time in Prague,...).

* Enable export and import of events. You can also export search-defined selections.

* The calendar must not allow a collision, in the event of a collision, it must allow you to find the nearest free date or move the event (if possible). Alternatively, you can enable max. number of collisions (P. 24 collisions for the classroom, according to the number of students that may be in it,...), but collisions can not be ignored.

## Where can polymorphism be used? (best)

* calendar view: daily, weekly, monthly, …

* collision resolution strategy: finding the nearest possible date, moving max. X other events at free slots, …

* exported event formats: proprietary, iCalendar, CSV, …

* user interface: console, ncurses, SDL, OpenGL (various variants), …

* types of events (think in advance whether in your case it is a polymorphism)


## Other information / references:

* http://en.cppreference.com/w/cpp/chrono

* https://en.wikipedia.org/wiki/ICalendar

* It is not necessary to implement an understanding of the ICalendar format, you can choose your own proprietary format that will work well for you.

* When implementing individual views, focus on how to cleverly use polymorphism here. Thus, if you add a new view, then such a view should mean creating a new class and "registering it in one single place".
