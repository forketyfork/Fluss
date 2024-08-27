from:: private chat
url:: [Nix on MacOS - The Good, the Bad and the Ugly](https://drakerossman.com/blog/nix-on-macos-the-good-the-bad-and-the-ugly)
on:: 2024-08-27 08:23

>In general, using Nix on macOS is rather pleasant. Nix-darwin, however, is not as satisfactory.

I would say there's nothing remotely satisfactory about nix on macOS. Update of nix still doesn't work, to my knowledge.

>Put simply - brew sucks. Everything else sucks. Nix replaces them all.

This is laughable. In terms of local package management, nix isn't even close to brew when it comes to the quality of package support. Everything breaks constantly.

>With Nix, it's just a matter of `nix profile install nixpkgs#app-of-some-specific-version`. I

Yes, if you follow a specific way of installing and using nix; last time I checked, determinate systems don't even set up the nixpkgs channel, you're supposed to use flakes.

>I am not sure Nix and Nix-darwin are extensively tested on older (or even the latest minus one) MacOS versions.

Yet brew somehow sucks.

> "...Nix is the worst package manager on MacOS except for all the other package managers that have been tried from time to time."

Okay, I'll allow it.

