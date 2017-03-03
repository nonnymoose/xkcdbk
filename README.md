# xkcdbk
Downloads xkcd comics and converts them to a book

# Usage
    xkcdbk [--no-pdf] [--toc] [--page-width PAGE_WIDTH] [--page-height PAGE_HEIGHT] RANGE OUTPUT

		--no-pdf						Do not convert to pdf, write html to output file instead.
		--toc							Insert a table of contents at the beginning of the pdf (PDF ONLY).
		--page-width    PAGE_WIDTH		Make the page width PAGE_WIDTH (must be in real units, ex. 4in).
		--page-height   PAGE_HEIGHT		Make the page height PAGE_HEIGHT (must be in real units, ex. 4in).
		--help							Print this message
		--uninstall						Take a guess. ;)

    	RANGE			  	A comma-seperated list of ranges to download, ex. 4-6,20,22.
							Also accepts the special value "today" as the upper bound.
    	OUTPUT				The full filename of the output file. A file extension will not automatically be added.

	The exit code will be 1 if an error is encountered, 2 if an unknown option is encountered, otherwise 0.
	Note that it is usually safe to ignore HTTP errors in wkhtmltopdf output. The script will behave as so.
	If you'd like to reconfigure xkcdbk, then delete \`$HOME/.xkcdbk\`.

# Installing
Dependencies:
 - wkhtmltopdf (I recommend that you download and install it from their [website](http://wkhtmltopdf.org), or else you will not be able to use the toc feature)
 - wget
 - bash (duh)
 - GNU getopt
 
It can automatically resolve the first two.

Then simply download and run the main script, `xkcdbk`, from the releases page. It can take care of the rest.
