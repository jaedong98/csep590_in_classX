# In-classX 

Jae Dong Hwang


## Questions

### 1. Did SpotBugs discover any bugs related to nullness? 

No

### 2. Did you find a bug in the code? Why didn’t SpotBugs find it?

```bash
/Users/haujd98/Documents/UW/csep590_sp19/nullness-exercise/src/main/java/nullness/exercise/FileAlterationObserver.java:173: error: [argument.type.incompatible] incompatible types in argument.
        this(directory, null);
                        ^
  found   : null
  required: @Initialized @NonNull FileFilter
/Users/haujd98/Documents/UW/csep590_sp19/nullness-exercise/src/main/java/nullness/exercise/FileAlterationObserver.java:183: error: [argument.type.incompatible] incompatible types in argument.
        this(directory, fileFilter, null);
                                    ^
  found   : null
  required: @Initialized @NonNull IOCase
2 errors


```

### 3. How many @Nullable annotations did you need to write to convince the Nullness Checker that the code is safe after you fixed all bugs?

### 4. How difficult was the Nullness Checker to use? Would you consider it in your own projects? Why or why not?