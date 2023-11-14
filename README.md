# similars
storming fast, versatile program to search similar textfiles on devices

```
At least one argument necessary - directory/dir to comapre CWD agasint
In case of two and more argumetns, first is compared against all others (all file/dir,recursive)
Other understood args:
  --min=NUMB        minimal similarity in percent
  --minws=NUMB      minimal similarity in percent with whitechars removed
                    Note, that min/minws should be 0-100 inclusive. Bigger/higher will effectively exclude the method.
  --case=true/false if false, similarity is case insensitive
  --fitler=EXPRES   file path filter regex
  --exclude[=EXPRES]sources exclude list exclude matching source files form run. Eg ".*/(Main|Test|Test1|Test2|PURPOSE|TEST.ROOT|A)\.java$"
  --eraser[=EXPRES] remove matching (comment?) lines if enabled, default is \s*[/*\*#].*
  --names=false/true/icase/NUMBER/
                    will compare only if filenames are same/similar
                    false - not used, comapre all. true filenames must be same before comaprison
                    icase - like true, only9 case insensitive. NUMBER - names must be similar (percentages) 
  --verbose         verbose mode
  --html            will add html table to stdout
  --maxsize=NUMBER  maximum filesize in KB   
                    Default is 100 (100kb), which eats about 46GB ram and taks 5-8 minutes.
                    Biggrer files may cause OOM/crash
  --minsize=NUMBER  minumum filesize in B. Default 10  
  --maxratio=DOUBLE maximum filesize diff ratio
                    Default is 10. Unless target/n < source < target*N then comparison will be skipped.
                    Processed after comment removal
  --port[=NUMBER]   port to get progress and info
                    if enabled, it will reply pid@host time since lunch/eta; default port is 4812
                    The server will block program from exit.
everything not `-` starting  is considered as dir/file which  the CWD/first file/dir should be compared against

```
