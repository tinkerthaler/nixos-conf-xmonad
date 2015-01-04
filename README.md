nixos-conf-xmonad
=================

Mostly note to self (due to regular out-of-brainmemory exceptions)

* Installed xmonad, xmonad contrib and xmonad extras using nix-env (ghc 7.8.4 versions)
* Ensure the version installed correspond to the ghc version that is installed

At some point I got this error: 

    xmonad.hs:3:18
    Could not find module 'XMonad.StackSet'
    use -v to see a list of the files searched for.

The issue was that I had a ghc-7.6.3

To troubleshoot I ran ```ghc-pkg list``` with the ghc-7.6.3 version: no xmonad packages

I then switched to ghc-7.8.4 and reran the ```ghc-pkg list``` command: xmonad packages where listed 
