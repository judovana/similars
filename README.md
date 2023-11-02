# similars
storming fast, versatile program to search similar textfiles on devices

```
At least one argument necessary - directory/dir to comapre CWD agasint
In case of two and more argumetns, first is compared against all others (all file/dir,recursive)
Other understood args:
  will comapre only if filenames are same/similar
                                     --names=false/true/icase/NUMBER/
    false - not used, comapre all. true filenames must be same before comaprison. icase - like true, only9 case insensitive. NUMBER - names must be similar (percentages) 
  minimal similarity in percent      --min=NUMB
  minimal similarity in percent with whitechars removed
                                     --minws=NUMB
Note, that min/minws should be 0-100 inclusive. Bigger/higher will effectively exclude the method.
  file path filter regex             --fitler=EXPRES
  sources exclude list               --exclude=EXPRES
    exclude matching source files form run. Eg ".*/(Main|Test|Test1|Test2|PURPOSE|TEST.ROOT|A)\.java$"
  remove matching (comment?) lines   --eraser[=EXPRES]
    if enabled, default is \s*[/*\*#].*
  verbose mode                       --verbose
  will add html table to stdout      --html
  maximum filesize in KB             --maxsize=NUMBER
    Default is 100 (100kb), which eats about 46GB ram and taks 5-8 minutes. Biggrer files 
  maximum filesize diff ratio        --maxratio=DOUBLE
    Default is 10. Unless target/n < source < target*N then comparison will be skipped. Processed after comment removal
everything not `-` starting  is considered as dir/file which  the CWD/first file/dir should be compared against
```
