# Haskell
For my own reference (and anyone else in case this actually becomes useful):

UPDATE: After trying a bunch of different solutions for Atom I have (for the time being) quit. I am now using Sublime, following http://umairsaeed.com/blog/2015/05/02/sublime-text-and-haskell/. After running into issues with cabal I consulted https://www.schoolofhaskell.com/user/simonmichael/how-to-cabal-install#could-not-resolve-dependencies--cabal-hell.

Haskell + Haskell-Atom Setup on Mac

To Download Atom: https://atom.io/. I am basically following https://atom-haskell.github.io/, but am modifying steps where I found necessary.

1. To install Haskell:
Go to https://www.haskell.org/platform/prior.html and download version 8.0.2. This is because I was running into issues with Atom's haskell-ghc-mod not having support for version 8.2.2.

2. Use the command 

```apm install language-haskell ide-haskell ide-haskell-cabal haskell-ghc-mod autocomplete-haskell```.

3. Choose between Stack and Cabal:

Which should I choose?
  If you are asking this, probably just go with Stack. It seems to be easier for most things, including getting started. For some   discussion see [here](https://stackoverflow.com/questions/30913145/what-is-the-difference-between-cabal-and-stack "StackOverflow Post"). To learn more about using Stack see [here](https://haskell-lang.org/tutorial/stack-build "Stack Turtorial"), or (found later) [here](https://www.fpcomplete.com/blog/2015/08/new-in-depth-guide-stack "FP Complete Guide").
 
Make sure you have at least version 1.6.1 of Stack (I have 1.6.3). Before I was running version 1.3.2 and running into errors when trying to build with stack. I recommend completely removing stack and reinstalling using Homebrew.

4. Then run 
```stack install stylish-haskell```
```stack install ghc-mod``` as in the guide.

During the first installation I received a warning that the location at which Stack is installed is not on my PATH environment variable. If this is the case just add it using
```sudo vim /etc/paths```.
 
Then during the second installation I received Error: While constructing the build plan, along with the recommendation to use stack solver. According to https://github.com/DanielG/ghc-mod/wiki/Installing#using-the-stack-tool, it is recommended to use cabal when installing ghc-mod. Now following this post:
```cabal install cabal-install```. Then add ~/.cabal/bin to your PATH.


 
[here](link "Stack Overflow Post")
