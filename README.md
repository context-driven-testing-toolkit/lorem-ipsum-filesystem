# Lorem, Ipsum, Filesystem!

Create a fake filesystem full of text files with random names.

## Synopsis

Run it like this:

    bin/lorem-ipsum-filesystem

This should produce a folder called `loremfs` in the current directory. The fake filesystem is in that folder.

### "Advanced" Usage

If you need a larger filesystem than was generated, you can _just run the script again_ and it will 
continue to add on to the already-created filesystem in the `./lormefs` folder.

Run the script over and over (using a loop if necessary) until you have as large a filesystem as you desire, or until your disk is full! All generated files will be deposited inside the same `./loremfs` folder so it is easy to clean up the generated filesystem once you are done with it.

## Installation

You will need to install the `Text::Lorem` Perl module. 
