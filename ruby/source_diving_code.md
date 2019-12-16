# Source diving code

Steps to diving into code

1. Find the largest file or longest line of code in the directory. In this example, it is in the models folder.

```
find models -type f | xargs wc -l | sort -r | head
```

2. Search for the source of error or any string
```
$ ag 'something'
$ ag -i 'something' # case sensitive search
$ ag 'some.*thing' # regular expression search
$ ag --ruby 'something' # search by file type. this command is to search only ruby file
```
 
Another method to search something is to use `referral` gem

High level view of search method 
- see something interesthing
- search for it
- GOTO 1

3. Try tracing if you want to debug. Just try to print something. `puts something`
You can also find ruby gem source file by
 ```
  $ echo $GEM_HOME
  $ ls $GEM_HOME/gems # to list all gems
 ```

Using `pry-byebug`. Require it by `require 'pry-byebug'`
```
# first binding.pry on point of interest
pry(main)> step # step into the function
pry(main)> next # to go to next line
pry(main)> finish # will step out of the function
pry(main)> continue # stop debugging + move on
pry(main)> whereami # print the code around you
pry(main)> backtrace # print the current stack trace
pry(main)> !!! # exit program
pry(main)> help
```

---

Tracing backwards
- start at your point of interest
- Text search / referra;

---

Tracing
- Searching for references ("I am inside method, where does this method get call from")
  - Check includes / extends
  - metaprogramming
  - use ag to search the whole codebase
- Check gem files

## Summary
The Kuchta 3ish step process
1.  Take me to your leader
 - entry points
 - big files
2. Text Search
 - Ag
 - Repeated searching
3. Trace 
 - Puts statements
 - Debugger

[Source : RubyConf 2019 - Source-Diving for Fun and Profit by Kevin Kuchta](https://www.youtube.com/watch?v=2YobJGkSSrU&t)