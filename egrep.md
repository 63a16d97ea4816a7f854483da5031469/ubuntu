#egrep


	egrep

	egrep [options] [regexp] [files]

Search one or more files for lines that match an extended regular expression regexp. egrep doesn't support the regular expressions \(, \), \n, \<, \>, \{, or \}, but it does support the other expressions, as well as the extended set +, ?, |, and ( ). Remember to enclose these characters in quotes. Regular expressions are described in Chapter 7. Exit status is 0 if any lines match, 1 if none match, and 2 for errors.

See grep for the list of available options. Also see fgrep.

	Examples

Search for occurrences of Victor or Victoria in file:

	egrep 'Victor(ia)*' file egrep '(Victor|Victoria)' file

Find and print strings such as old.doc1 or new.doc2 in files, and include their line numbers:

	egrep -n '(old|new)\.doc?' files