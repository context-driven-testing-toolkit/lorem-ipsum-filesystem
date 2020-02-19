# Lorem, Ipsum, Filesystem!

Create a fake filesystem full of text files with random names.

Note that **if all you want to do is fill up disk** (you don't actually need the payload to be a filesystem) you can just use one of the following two commands depending on whether you use Linux or Mac:

    fallocate -l 50G big_file    # On Linux use fallocate(1)
    
    mkfile 50G big_file          # On Mac OS use mkfile(1)
    
Note that `50G` above is the desired size of the file. If you want a smaller filesize you can also specify `K` or `M`

## Synopsis

Run it like this:

    bin/lorem-ipsum-filesystem

This should produce a folder called `loremfs` in the current directory. The fake filesystem is in that folder.

### Verifying That It Worked

You can run the following commands to explore the generated filesystem and make sure it fits your needs.

    du -sh loremfs    # Shows the storage footprint of the directory, 
                      # something like "268M"

    tree loremfs | grep -E '^\d+'    # Shows total count of files and folders,
                                     # like "1309 directories, 267 files"
    
### "Advanced" Usage

If you need a larger filesystem than was generated, you can _just run the script again_ and it will 
continue to add on to the already-created filesystem in the `./lormefs` folder.

Run the script over and over (using a loop if necessary) until you have as large a filesystem as you desire, or until your disk is full! All generated files will be deposited inside the same `./loremfs` folder so it is easy to clean up the generated filesystem once you are done with it.

## Installation

You will need to install the `Text::Lorem` Perl module. 
