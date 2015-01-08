this is billo's crappy blog publishing script

Essentially:
 1. write Markdown files with a .txt extension. 
 2. Arrange them in a directory structure YYYY/MM
 3. create a CSS file header and footer shtml files
 4. enable apache server side includes to parse .shtml files
 5. run this script

This project contains an unaltered copy of Markdown.pl so it can run
"out of the box." If you have any special Markdown implementations you
use, just replace it or alter the script to use a different one.

Directories needed

    blogdir: this is where the .txt (Markdown) files should live
    masterdir: this is where some static boilerplate include files are

Files needed in blogdir. These are not altered by the script:

    index.shtml: this is not touched by the update script.
    header.shtml: when the script creates pages, this is the top chunk
    footer.shtml: when the script creates pages, this is the bottom chunk
    footerbar.shtml: visible contents of the footer on all pages
    monthheader.shtml: for the generated monthly index, this file is the top chunk
    monthfooter.shtml: for the generated monthly index, this file is the bottom chunk
    feed/index.shtml: the shell of the RSS feed

Files needed in masterdir:

    monthindex.shtml: This is the master template for each generated index.shtml in the month folders
    tweet.shtml: this includes the "tweet" button which is placed at the top of the archive index.

files generated by this script:

    blogdir/sidebar.shtml - this is the top level index of all the months where there is a post
    blogdir/contents.shtml = top level meat middle section of the main index file
    blogdir/feed/items.ihtml - the RSS feed items
    blogdir/YYYY/MM/contents.shtml - the contents of each month index page
    blogdir/YYYY/MM/index.shtml - the index page of each month
