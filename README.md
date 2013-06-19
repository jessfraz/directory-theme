# Directory Theme
A simple, customizable theme for your Apache directory listing.
Be sure you have ```mod_autoindex``` loaded. Here is a demo of what the result looks like: [gif library](http://hugtheef.com).

## Features

- search the directory and display results, as the user inputs the search term
- custom styling of the default directory indexing
- ```.html``` files are linked to without the file extension (ex. http://localhost/example.html -> http://localhost/example)

	- if you would rather like this to be removing the file extention for ```.php``` files replace these lines 

		```
		RewriteCond %{REQUEST_FILENAME}\.html -f
		RewriteRule ^(.*)$ $1.html
		```

		in [.htaccess](https://github.com/jfrazelle/directory-theme/blob/master/.htaccess) with the following

		```
		RewriteCond %{REQUEST_FILENAME}\.php -f
		RewriteRule ^(.*)$ $1.php
		```
- changes "Last modified" column to display time as time since (ex. 2 minutes ago, 4 days ago, etc)
- ```htaccess-txt.txt``` is included because ```.htaccess``` might be hidden by your computer after downloading, copy the contents into a file you name ```.htaccess``` if this is the case

## Installation

1. Download.
2. Add the contents of directory-theme to the ```root``` folder of your localhost (ex. Sites)
3. Go!

## Configurations

- Change any styles in [style.css](https://github.com/jfrazelle/directory-theme/blob/master/theme/style.css)
- Add any elements or customize the header:  [header.html](https://github.com/jfrazelle/directory-theme/blob/master/theme/header.html)
- Add any elements or customize the footer:  [footer.html](https://github.com/jfrazelle/directory-theme/blob/master/theme/footer.html)
- Ignore certain files or directorys by customizing [.htaccess](https://github.com/jfrazelle/directory-theme/blob/master/.htaccess) by adding to the line ```IndexIgnore .htaccess /theme favicon.ico *.tmproj 404.html htaccess```
- Swap out, add, or custumize any icon by changing [.htaccess](https://github.com/jfrazelle/directory-theme/blob/master/.htaccess) and editing the lines starting with ```AddIcon``` and changing the file reference, ```/theme/icons/gif.png``` or file extension, ```.gif```, result should look like this ```AddIcon /theme/icons/gif.png .gif```


### Credits

Based off [apaxy](https://github.com/AdamWhitcroft/Apaxy) by Adam Whitcroft 