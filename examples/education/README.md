# Adding Educational Background to VIVO

To add education backgrounds to VIVO, we need to know several pieces of information for each degree awarded:

1. Who obtained the degree?
1. What degree was obtained? (BA, MS, PhD, etc)
1. From what institution?
1. What is the date of the degree?
1. What is the field of study for the degree?

As with all data in VIVO, each of these is optional.

## Managing Enumerations

Each piece of information for the awarded degree is represented by an enumeration:

1. person_enum for who
1. degree_enum for what
1. school_enum for where
1. date_enum for when
1. field_enum for field of study

The python program `make_enum.py` can be used to update four of these enumerations from your VIVO.  To run 
`make_enum.py` use:

    python make_enum.py

The field of study enumeration is managed by hand -- if you have fields of study that you would like to be able to 
represent in VIVO, edit the field_enum.txt file with a text editor and add a row for each such field of study.  Notice
that the two columns in `field_enum.txt` are identical, separated by a tab.  This is intentional and provides a 
"controlled vocabulary" for a text field such as field of study.  Your source file must contain fields of study
found in the enumeration or have a blank value or the value None.

