Mendeley FileSync
=================

This script stores the location of files associated with Mendeley references
in a text file and then uses that text file to update the files associated with
a document in Mendeley Desktop's database.

It is designed to be used in conjunction with Unison or a service like Dropbox
for people that would prefer not to have to use Mendeley's file storage service
and want to use Mendeley on multiple computers.

Note that you should first synchronise your Mendeley database to get any new references
before running this script, as documents won't be added to any references that have
not first been added to the Mendeley database.

Usage
-----

To run it, use::

    ./mendeleyfilesync.py mendeley_database text_database file_path

mendeley_database is the path to the sqlite database used by Mendeley, the Mendeley
website has a FAQ on how to find this file at http://www.mendeley.com/faq/#locate-database.

text_database is the location of a file to store reference locations. This should
be synchronised along with your documents using Unison/Dropbox etc and run on each computer
after synchronising references in Mendeley Desktop. On the first
run this file will be created.

file_path is the directory where your documents are stored.

Passing the --dry-run option will just show you what changes would be made but
won't write to the Mendeley database or the text database.
