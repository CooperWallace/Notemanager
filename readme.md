# Description

Contains a collection of shell scripts designed for managing and maintaining
course notes taken on the users computer. It aims to provide an easy way to
create, edit, and view notes for each Course on the system automatically.

The `notemgr` scripts are to be used as a back-end for managing the notes on a
system. I plan to implement a `rofi` script or another menu system to
conveniently use the scripts.

# Planned Tools

The following tool set is broken up into the following sub tools:

`notemgr` - Used for managing the Lectures that exist on the users system for
specific courses.

- Provides a Path to the desired lecture
- Provides a Path to the desired Course
- To be used when creating a new Note file for a specific course
	- Add all of the Prefix and Post fix data specified in the Database to the file
	- Generic headers, et al.

`notemgr-edit` - Used for creating or editting courses in the database to be
used by `notemgr`.

- Allow for editing variables to be used with courses

`notemgr-compile` - Used to compile notes for a course

- Shall use the directory path given in the Course information
- (?) Allow for specific courses to have different render functions
- (?) Allow for a specific prefix to be used for different Courses.
	- Should follow a "(PREFIX)(Number).(EXT)" scheme

`notemgr-view` - Used to view notes for specific Lecture

- List all of the Lectures that belong to a lecture.
- Return the path to the compiled file
