

# Introduction #

vs-android was a natural evolution to using the 'makefile project' method of working with Android apps in Visual Studio.

I started working on it largely in an experimental fashion, taking the Microsoft cl compiler MSBuild scripts and modifying them. This was the first time I have worked with MSBuild, so this project in itself has been a learning experience.

In light of this, the MSBuild scripts which make up vs-android may not be the 'correct' way of doing things. For some aspects I may well be going 'round the houses' instead of a more succinct and efficient route.

Anyhow, the culmination of the work was an environment I felt matched the native Microsoft Cl compiler pretty decently. I could compile single files; I have Intellisense working completely; I could have static library sub-projects. All the stuff I wanted.



# Why bother with this, why not just use Eclipse and ndk-build? #

Well, when someone has used an IDE for well over a decade every day for their day job, they get a little attached to it! :) Ask a devout emacs user, I'm sure you'd pry that editor out of their cold dead hands.

All in all though, there are a few very positive points over using the ndk-build scripts that Google provide.
  * Less than half the time to do a full rebuild on large projects, and also half the time for incremental (one file) changes.
  * Ability to compile single files very quickly, without dependency checking the whole project.
  * It's a very good cross-platform solution if you wish to maintain a Win32 port of your software. These can be maintained as well within the same project file.

So having those, and using the fully-featured text editor I've been used to for years is a pretty easy sell to me. I'm sure Eclipse is great, I've tried using it a few times now but I just can't get on with it to the same degree.

For more background on my motivations, see here:
  * http://www.gavpugh.com/2011/02/04/vs-android-developing-for-android-in-visual-studio/



## Static libraries ##

Set these up the same way as with Win32 projects. In the properties pane, under "General" there's a "Configuration Type" which would be "Static Library (.lib)".

Static lib dependencies though work differently to previous versions of Visual Studio. I was a little caught out on this one! Take a look at this post on StackOverflow for how to set them up:

  * [StackOverflow Post](http://stackoverflow.com/questions/3795567/visual-studio-2010-not-autolinking-static-libraries-from-projects-that-are-depend)


# Future Plans #

My TODO list:

  * [TODO\_List](TODO_List.md)


# Useful Links #

I definitely recommend checking out this blog post:
  * http://ian-ni-lewis.blogspot.com/2011/01/its-like-coming-home-again.html
It details how to use WinGDB to debug NDK code within Visual Studio.


# References #

A great book for getting to grips with MSBuild:
  * ["Inside the Microsoft Build Engine: Using MSBuild and Team Foundation Build"](http://www.amazon.com/Inside-Microsoft-Build-Engine-Foundation/dp/0735645248/mutomagaby-20) by Sayed Ibrahim Hashimi, William Bartholomew.