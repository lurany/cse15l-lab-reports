# Researching Commands

For this particular report, I've decided to look for alternate ways of using the command line  `find`. In class, we have went through the
`-name` command so I would not be using that command.

### Command Line Argument #1| -empty
The `-empty` command is one of the alternate command line arguments for `find`. The goal of the `-empty` is to go through the given directory and its sub-directories to check for if there are any other files that are empty. For example, if we look at the *example* file, we can perform the `-empty` command. First, I perform 
`$ mkdir new` to have a empty directory, so that the `-empty` command would be able to seek it. So if I were to use `$ find example -empty` I would get `example/new`. This was the goal because I was able to find out all the emprty files in *example*. Another example would be when I tried finding an empty file on *plos* which is located on the *docsearch* directory. I used `$ find plos - empty` but the results doesn't show anything. This is because there are no empty files in plos.

### Command Line Argument #2| -user
If you ever wonder how to find files/directories that are owned by a specific user, you can use the `-user` command, which basically goes through all the files owned by the name of the user you input. For example, 
when I perform `$ find /home -user luran` with luran being my pc name, the results shows a lot of files such as:
`luran/wavelet/.git/refs/tags
luran/wavelet/.gitignore
luran/wavelet/Handler.class
luran/wavelet/NumberServer.java
luran/wavelet/README.md
luran/wavelet/SearchEngine.class
luran/wavelet/Server.class
luran/wavelet/Server.java
luran/wavelet/ServerHttpHandler.class
luran/wavelet/StringServer.class
luran/wavelet/StringServer.java
luran/wavelet/URLHandler.class`
because it went through all the files that are in my laptop as long as I own it. Though this is not the best way to find a specific file, it can still be helpful when you are trying to find a file that was owned by someone else. If we to test it on a unknown name, for example `$ find /c -user mi` if will show the result `find: ‘mi’ is not the name of a known user`. The reason for this is because *mi* does not exist in my laptop nor does it own any files in my laptop.
I got this command line argument from [geekflare](https://geekflare.com/linux-find-commands/)

## Command Line Arguments #3| -delete
The `-delete` command is very useful for getting rid of files and directories that has been found. For example, if I were to want to delete a file like *plos* in the *technical* directory, I just need to use `$ find plos -delete` and *plos* should be deleted. Now if I try to put `$ find plos` it would show up 

<img width="292" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/de14cd75-81b2-4ee6-bef4-fd32b9821f8e">

because it is deleted. Another example would be to combine the `-empty` with `-delete` like `$ find example -empty -delete`. Once this is done, there should be nothing empty within the *example* directory. Doing `$find example -empty` will just shows `$`.

## Command Line Arguments #4| -type n
If you ever want to look for things specific to files/directories and doesn't want to `ls` all the time since it can be very hard to find a speficic file, the command `-type` would be the best way. If you want to see how many directories are in the *technical* directory because you want to isolate each directory for it's specific purpose, you would do `$ find technical -type d`. After performig this, it would show 
`$ find technical/ -type d
technical/
technical/911report
technical/biomed
technical/government
technical/government/About_LSC
technical/government/Alcohol_Problems
technical/government/Env_Prot_Agen
technical/government/Gen_Account_Office
technical/government/Media
technical/government/Post_Rate_Comm`

which gives all the directories that have access within the *technical* directory. If you also want to see all the files in general, then you should put `$ find technical -type f` which gives 

<img width="225" alt="image" src="https://github.com/lurany/cse15l-lab-reports/assets/130108693/bfcf9be6-4189-4608-afbf-3987de063aee">

because it list all the files inside the *technical* directory. This is useful as it becomes a tool to find things in realtion to their typing
