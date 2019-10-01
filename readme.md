# Description

Contains a collection of shell scripts designed for managing and maintaining
course notes taken on the users computer. It aims to provide an easy way to
create, edit, and view notes for each Course on the system automatically.

The `notemgr` scripts are to be used as a back-end for managing the notes on a
system. I plan to implement a `rofi` script or another menu system to
conveniently use the scripts.

**Note**: Compilation commands, `pandocOutput` and `pandocWatch` can be found
[Here](https://github.com/CooperWallace/dotfiles/tree/master/.scripts)

# Usage:

## Note Manager

```
Usage: ./notemgr [OPTIONS]
./notemgr			Display all non-archived courses
./notemgr [Course]		Display all Lectures in course
./notemgr [Course] [Lecture]	Print path to the specific lecture

Desription:
Help maintain and manage Notes for the specified courses on the Users system.

Options:
  -h		Display usage message
  -l		List all Courses in database, including those archived.
  -c Course	Create a new Lecture for the course
  -g Course	Display the path to the course
  -a Course	Display whether course has been archived
```

## Note Manager Edit

```
Usage: ./notemgr-edit [OPTIONS]

Description:
Maintains the information of all courses that are to be used in the notemgr
command. Responsible for handling all preferences related to courses

Options:
  -h		Display usage message
  -c		Create a Course entry
  -a [Course]	Set the course as being 'archived'.
  -A [Course]	Set the course as being 'active'.
```

# TODO and Planned Tools

The following tool set is broken up into the following sub tools:

`notemgr` - Used for managing the Lectures that exist on the users system for
specific courses.

- [x] Provides a Path to the desired lecture
- [x] Provides a Path to the desired Course
- [x] To be used when creating a new Note file for a specific course
- [ ] Add all of the Prefix and Post fix data specified in the Database to the file
- [ ] Generic headers, et al.

`notemgr-edit` - Used for creating or editting courses in the database to be
used by `notemgr`.

- [ ] Allow for editing variables to be used with courses
- [ ] Archiving of Course straight to tar
- [ ] Archiving of compiled pdf straight to tar

`notemgr-rofi` - Used in combination with Rofi to display an interactive menu

`notemgr-compile` - Used to compile notes for a course

- Shall use the directory path given in the Course information
- (?) Allow for specific courses to have different render functions
- (?) Allow for a specific prefix to be used for different Courses.
	- Should follow a "(PREFIX)(Number).(EXT)" scheme

`notemgr-view` - Used to view compiled notes for specific Lecture


Compile command: Does one thing, and does it well.

- Compile singular lecture
	- Flag to open Zathura
- Compile entire directory

`notemgr-render <IN> <OUT>`
	- `<OUT>` is default is not specified
