# Moving around
## pwd
**P**rint **wo**rking **di**rectory: displays the current working directory where all commands will be executed
```shell
~> pwd
/Users/theozanchi
```

## cd
**C**hange **d**irectory: can be used with an absolute or relative path.
```shell
~> cd /home/Desktop/some_directory
```

`..` brings you one directory up
```shell
~> cd ..
```

`~` takes you to your home directory
```shell
~> cd ~
```

## ls
**L**i**s**t shows you everything in your current working dircetory
```shell
~> ls
Applications/                               Library/                                   
Desktop/                                    Movies/                                    
Documents/                                  Music/                                     
Downloads/                                  Pictures/                                   
```

`-a` flag includes hidden files in the display
```shell
~> ls -a
./                                          .condarc                                    .npm/                                       .wakatime.cfg
../                                         .config/                                    .p2/                                        .zoomus/
.CFUserTextEncoding                         .cups/                                      .pylint.d/                                  .zsh_history
.DS_Store                                   .docker/                                    .python_history                             .zshrc
.QtWebEngineProcess/                        .eclipse/                                   .python_history-02547.tmp                   Applications/
.Rhistory                                   .gitconfig                                  .python_history-27745.tmp                   Desktop/
```

`-l` flag uses long output for the display 
```shell
~> ls -l
total 8
drwx------	 5 owner  group   160  7 fév 16:52 Applications/
drwx------   5 owner  group   160 28 oct 13:59 Desktop/
drwx------  18 owner  group   576  9 fév 21:56 Documents/
drwx------  69 owner  group  2208 11 fév 20:13 Downloads/
drwx------ 106 owner  group  3392  4 aoû  2023 Library/
drwx------   5 owner  group   160 10 avr  2023 Movies/
drwx------   7 owner  group   224 10 avr  2023 Music/
drwx------   6 owner  group   192 10 avr  2023 Pictures/
drwxr-xr-x   6 owner  group   192 10 avr  2023 Public/
drwxr-xr-x  22 owner  group   704 17 mai  2023 francinette/
drwxr-xr-x   3 owner  group    96 29 aoû  2016 lib/
-rw-r--r--   1 owner  group     6 16 oct 17:11 test.txt
```
The output contains the following information:
* `drwxrwxrwx`: the first letters indicates the type of object (among which `d` for directories, `-` for standard files). The next three `rwx` blocks indicates `r`ead, `w`rite and e`x`ecute permissions for the user, the group and others.
* Number of links to the object
* The owner
* The group
* The size
* The last modification date
8 The name

## mkdir
**M**a**k**e **dir**ectory creates a new directory
```shell
~> mkdir new_directory
```

# Output
## cat
Con**cat**enate and print: displays the content of a file in the terminal
```shell
~> cat test.txt
hello world
```

## head
Display the top 10 lines of a file in the terminal
```shell
~> head hhgttg.txt 
The Hitch Hiker's Guide to the Galaxy 
for Jonny Brock and Clare Gorst 
and all other Arlingtoniansfor tea, sympathy, and a sofa
Far out in the uncharted backwaters of the unfashionable  end  of
the  western  spiral  arm  of  the Galaxy lies a small unregarded
yellow sun.
```

## tail
Display the last 10 lines of a file in the terminal
```shell
~> tail hhgttg.txt 
of all possibility.
  
The Vogon turned on the light himself. He picked up the
piece of paper again and placed a little tick in the little box.
Well, that was done. His ship slunk off into the inky void.
In spite of having taken what he regarded as an extremely
positive piece of action, the Grebulon Leader ended up having
a very bad month after all. It was pretty much the same as all
the previous months except that there was now nothing on the
television any more. He put on a little light music instead.
```

## wc
**W**ord **c**ount displays the number of lines, words and bytes of a particular file.
```shell
~> wc hhgttg.txt 
   39776  263723 1534289 hhgttg.txt
```
The information can be accessed independently with flags `-c`/`--bytes` for bytes, `-m`/`--chars` for characters and `-l`/`--lines` for lines
```shell
~> wc -l hhgttg.txt 
   39776 hhgttg.txt
```

## echo
Display text in the terminal
```shell
~> echo hello world 
hello world
```

# Dealing with files
## cp
**C**o**p**y files from `source` to `target`
```shell
~> cp temp.txt new.txt
```

`.` and `..` can be used for relative paths
```shell
~> cp ../some_file.txt .
```
```shell
~> cp some_other_file.txt ..
```

## mv
**M**o**v**e files, with absolute or relative paths
```shell
~> mv temp.txt ../another_directory
```

## rm
**R**e**m**ove files or directories.
```shell
~> rm some_file.txt
```

`-r` is required to remove a directory
```shell
~> rm some_directory -r
```

## wget
Downloaded from a URL with the wget method: 
```shell
~> wget https://some_content.tar.xz
```

## touch
Finally, if a file does not have the correct timestamp, it can be modified with the touch command. If the file does not exist, it is created
```shell
~> touch temp.txt
```

# Searching
## find
Now, if you need to find something on your machine, you can use the find command. You will need to specify where you want to search, and the name of the file you are looking for. 
You can use wildcards here to narrow your search. To learn more about wildcards, subscribe to our channel and wait for our upcoming video on the topic!
```shell
~> find ~/Downloads -name "*.png"
/Users/theozanchi/Downloads/bauges.png
/Users/theozanchi/Downloads/gr54.png
/Users/theozanchi/Downloads/IMG_1910.png
/Users/theozanchi/Downloads/stevenson.png
/Users/theozanchi/Downloads/Stoner_s Odyssey/7.background-mountains.png
/Users/theozanchi/Downloads/Stoner_s Odyssey/2.flowers-top.png
/Users/theozanchi/Downloads/Stoner_s Odyssey/8.planet.filters-scroll-horizontal+10.png
/Users/theozanchi/Downloads/Stoner_s Odyssey/1.face-dj-booth.png
/Users/theozanchi/Downloads/Stoner_s Odyssey/alternative-2.flowers-3.pillers-4.flowers-merged.png
/Users/theozanchi/Downloads/Stoner_s Odyssey/5.boat.filters-scroll-horizontal+30.png
/Users/theozanchi/Downloads/Stoner_s Odyssey/6.orb.filters-scroll-vertical+45.png
/Users/theozanchi/Downloads/Stoner_s Odyssey/4.flowers-bottom.png
/Users/theozanchi/Downloads/gr10.png
/Users/theozanchi/Downloads/IMG_1993.png
/Users/theozanchi/Downloads/IMG_2024.png
/Users/theozanchi/Downloads/balise_gr.png
```

## grep
Find allows you to look for files, grep allows you to look for specific informations in files. Let’s take back our example of the Hitchhiker’s guide to the Galaxy, the following command will return us all lines containing our search. Grep works line by line
```shell
~> grep hello hhgttg.txt 
could have come and said a big hello to planet Earth, he thought,
the swamps of Squornshellous Zeta are very thoroughly killed  and
underwear, the piles of Squornshellous  mattresses  and  the  man
voice, "and we'll be saying a big hello to all  intelligent  life
"Why hello there!" they said (ticker tape, ticker tape).  "All  I
"Well," he said, "hello my Captain of Vogons Prostetnic, and  how
"I am not a ... hello, can you hear me?"
"Goodbye artificial Universe," he said, "hello real one!"
"Er ..." he said, "hello. Er, look, I'm sorry  I'm  a  bit  late.
"Ah, hello, Number  Two,"  said  the  Captain,  waving  a  cheery
"Er ... hello," they said.
"Oh, hello there," he said to them, "Excuse me  not  getting  up,
"Excuse  me,"  he  said,  "hello.  My  friend  and  I  were  just
"Hello Agda, hello Mella," said Ford.
Dent?  Ah,  hello,  yes. This is Arthur Dent speaking. Don't hang
just  the  end  of  the  game.  We  ought  to get out. Oh, hello,
The moment passed as it regularly  did  on  Squornshellous  Zeta,
Very often on Squornshellous Zeta, whole days would  go  on  like
which live quiet private lives in the marshes  of  Squornshellous
meaning  of  the  word  "vollue",  buy  a  copy of Squornshellous
being  delivered  on  Squornshellous  Zeta,  and certainly not by
revitalize  the  economy of the Squornshellous System. They spent
the entire economy of the Squornshellous System building it. They
"Er, hello?" he said.
creature  from  the  swamps of Squornshellous Zeta had recognized
After an initial flurry of opening hellos, he and Russell  -  the
"Oh, hello, Arthur Dent here. Look, sorry I haven't been  in  for
"Oh hello, is that the Old Elms Hospital? Yes, I was just phoning
the Universe, on Squornshellous Beta to be exact, two  worlds  in
into the life of a simple cushion from Squornshellous Beta.
that really get me down. Oh hello, you again."
he recognised in the distance, and hurried along to say hello,
`Princess Hooli? If I had to stand around saying hello to
villagers he passed said hello, but there was a sense of nervousness
standing there. I go up to say hello, then suddenly I see that
```

# Permissions and ownership
As you noticed in the long output of the ls utility, files and directories have permissions and owner. They can be changed with two commands: 
## chmod
To change permissions, use the change modes function. The codes used to change modes are in the manual, I will demonstrate 000 that removes all of them, and 777 that adds all of them
```shell
~> chmod 000 hhgttg.txt
```

```shell
~> chmod 777 hhgttg.txt
```

## chown
To change the owner, simply mark their name before the name of the file
```shell
~> chown another_user hhgttg.txt
```
