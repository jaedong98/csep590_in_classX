# In-classX 

Jae Dong Hwang, Kurtis Eveleigh


## Questions

### 1. Did SpotBugs discover any bugs related to nullness? 

No

### 2. Did you find a bug in the code? Why didn’t SpotBugs find it?

Yes, there were some methods that tried to add null to the list of listeners. SpotBugs couldn't find it because it didn't check to see if the parameter could be referenced in a way elsewhere in the program where null would cause issues.

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

We wrote 13 `@Nullable` annotations after fixing two bugs related to not checking for `null` before adding the listener to the list.

### 4. How difficult was the Nullness Checker to use? Would you consider it in your own projects? Why or why not?

It was pretty easy to use the Nullness Checker. Yes, we'd consider using it in our own projects. The annotations help with static analysis (like in code reviews) and it can help make the signature more descriptive.
