[![openage](/assets/logo/banner.png)](http://openage.sft.mx)
============================================================

**openage**: a volunteer project to create a free engine clone of *Age of Empires II*,
primarily aimed at POSIX platforms such as **GNU/Linux**,
comparable in its goals to projects like [OpenMW](https://openmw.org/), [OpenRA](http://openra.net/), [OpenTTD](https://openttd.org/) and [OpenRCT2](https://openrct2.org/)

openage uses the original game assets (such as sounds and graphics), but (for obvious reasons) doesn't ship them.
To play, you require *an original AoE II : TC installation or [AoE II: HD](http://store.steampowered.com/app/221380/)*
(installation via [Wine](https://www.winehq.org/) or [Steam-Linux](doc/media_convert.md#how-to-use-the-original-game-assets)).

[![github stars](https://img.shields.io/github/stars/SFTtech/openage.svg)](https://github.com/SFTtech/openage/stargazers)
[![#sfttech on Freenode](https://img.shields.io/Freenode/%23sfttech.png)](https://webchat.freenode.net/?channels=sfttech)
[![#sfttech on matrix.org](https://img.shields.io/badge/matrix-%23sfttech-blue.svg)](https://riot.im/app/#/room/#sfttech:matrix.org)
[![quality badge](https://img.shields.io/badge/cuteness-overload-orange.svg)](http://www.emergencykitten.com/)


[<img src="https://www.redditstatic.com/about/assets/reddit-logo.png" alt="reddit" height="45"> /r/openage forum](https://www.reddit.com/r/openage/)


The foundation of **openage**:

Technology     | Component
---------------|----------
**C++14**      | Engine core
**Python3**    | Scripting, media conversion, in-game console, code generation
**Qt5**        | Graphical user interface
**Cython**     | Glue code
**CMake**      | Build system
**OpenGL2.1**  | Rendering, shaders
**SDL2**       | Cross-platform Audio/Input/Window handling
**Opus**       | Audio codec
**Humans**     | Mixing together all of the above

Our goals *include*:

* Fully authentic look and feel
  * This can only be approximated, since the behaviour of the original game is mostly undocumented,
    and guessing/experimenting can only get you this close
  * We will not implement useless artificial limitations (max 30 selectable units...)
* Multiplayer (obviously)
* Matchmaking and ranking with a [haskell masterserver](https://github.com/SFTtech/openage-masterserver)
* Optionally, [improvements](/doc/ideas/) over the original game
* AI scripting in Python, you can use [machine learning](http://scikit-learn.org/stable/)
* Re-creating [free game assets](https://github.com/SFTtech/openage-data)
* An easily-moddable content format: [**nyan** yet another notation](https://github.com/SFTtech/nyan)
* An integrated Python console and API, comparable to [blender](http://blender.org/)
* Awesome infrastructure such as our own [Kevin CI service](https://github.com/SFTtech/kevin)

But beware, for sanity reasons:

* No network compatibility with the original game.
  You really wanna have the same problems again?
* No binary compatibility with the original game.
  A one-way script to convert maps/savegames/missions to openage is planned though.


Current State of the Project
----------------------------

 - What features are currently implemented?
   - See [doc/status.md](/doc/status.md).

 - What's the plan?
   - See [doc/milestones.md](/doc/milestones.md). We also have a [list of crazy xor good ideas](/doc/ideas).


Dependencies, Building and Running
----------------------------------

 - How do I get this to run on my box?
   - See [doc/building.md](/doc/building.md).

 - I compiled everything. Now how do I run it?
   - Execute `./run`.
   * [The convert script](/doc/media_convert.md) will transform original assets into openage formats, which are a lot saner and more moddable.
   - Use your brain and react to the things you'll see.

 - Waaaaaah! It
   - segfaults
   - prints error messages I don't want to read
   - ate my dog

All of those are features, not bugs.

To turn them off, use `./run --dont-segfault --no-errors --dont-eat-dog`.


If this still does not help, try our [troubleshooting guide](/doc/troubleshooting.md), the [contact section](#contact)
or the [bug tracker](https://github.com/SFTtech/openage/issues).


Development Process
-------------------

What does openage development look like in practice?
 - extensive [synchronization](#contact)!
 - [doc/development.md](/doc/development.md).

Can I help?
 - [doc/contributing.md](/doc/contributing.md).


All documentation is also in this repo:

- Code documentation is embedded in the sources for Doxygen (see [doc readme](/doc/README.md)).
- Have a look at the [doc directory](/doc/). This folder tends to outdate when code changes.


OS X Version
------------

Running openage on OS X worked in the past,
and might or might not work right now.

Setting up continuous integration for this platform has some complications. Running a hackintosh VM seems to be not so legal, while buying dedicated hardware for it seems to be not so cheap. If you know of a legal and cost-free way of doing so or want to sponsor a semi-recent Mac Mini, please open a ticket in our issue tracker. Until then, PRs untested on OS X will make their way into the master branch and occasional breakage will occur.


Windows Version
---------------

None of us uses Windows, so a port has low priority.

However, we're using cross-platform libraries wherever possible,
so a port should be "pretty easy" to accomplish.

If you want to beat us to it, go for it!


Contributing
============

* Being typical computer science students, we hate people.
* Please don't contact us.
* Nobody likes Age of Empires anyway.
* None of you is interested in making openage more awesome anyway.
* We don't want a community.
* Don't even think about trying to help.

Guidelines:

* No **bugreports** or **feature requests**, the game is perfect as is.
* Don't try to **fix any bugs**, see above.
* Don't implement any features, your code is crap.
* Don't even think about sending a **pull request**.
* Please ignore the [easy tasks](https://github.com/SFTtech/openage/issues?q=is:issue+is:open+label:%22easy%22) that [could just be done](https://github.com/SFTtech/openage/issues?q=is:issue+is:open+label:%22just+do+it%22).
* Absolutely never ever participate in this [boring community](https://www.reddit.com/r/openage/).
* Don't note the irony, you idiot.

To prevent accidental violation of one of those guidelines, you should *never*

* [learn git](http://git-scm.com/book/en/Git-Basics)
* [fork the repo](https://help.github.com/articles/fork-a-repo)
* [learn python](http://docs.python.org/3/tutorial/appetite.html)
* [learn c++14](http://www.cplusplus.com/doc/tutorial/)
* read the code and documentation
* [contribute](/doc/contributing.md) anything to the code
* [contact us](#contact)

cheers, happy hecking.


Contact
-------

Most of the developers hang around on our **IRC** channel (`#sfttech` on `freenode.net`).
Alternatively, you can join `#sfttech:matrix.org`, which is bridged to the IRC channel.
Do not hesitate to ping us, we might not see your message otherwise.

For all technical discussion (ideas, problems, ...), use the [issue tracker](https://github.com/SFTtech/openage/issues)!
It's like a mailing list.

For all interactive chit-chat, use our [/r/openage subreddit](https://www.reddit.com/r/openage/)!


License
-------

**GNU GPLv3** or later; see [copying.md](copying.md) and [legal/GPLv3](/legal/GPLv3).

I know that probably nobody is ever gonna look at the `copying.md` file,
but if you want to contribute code to openage, please take the time to
skim through it and add yourself to the authors list.
