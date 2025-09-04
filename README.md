# Hi, I'm Andrew!

I'm Andrew Lees, recently graduated from studying Mathematics at the University of Warwick.

I'm a programmer (focused mostly on backend and tooling) looking for entry-level software development jobs, either based in the UK or remote.

## Skills

I have experience with Rust, Python, Lua (Factorio modding + bindings for a school project I did),
C# (both standalone and in Unity), as well as completing some small projects in C, C++, Go, Dart and
JavaScript.

Using Docker, I host various services on my home server, including [a private Forgejo instance](#whys-it-so-empty-here),
my personal password manager, a Factorio server, and various custom monitoring and reporting systems.

Nowadays I mainly focus on Rust, with Python being used mainly for small projects/temporary scripts,
but am always willing to learn new languages and technologies.

## What do you have to show?

### The Python talk

I'm very proud to have given a Lightning Talk for UWCS (the University of Warwick Computing Society)
that was recorded and uploaded to YouTube, available [here](https://www.youtube.com/watch?v=t863QfAOmlY).
I decided to give a talk because I wasn't particularly used to giving talks, and felt like talking about
something I was comfortable speaking about would be a good experience.[^1]

It's a whirlwind tour of various "cursed" Python techniques I've come across over the years - from
strange places variables get created and deleted, to experiments with Python's type hints, turning
entire Python programs into a single line (no semicolons/`exec`!) to absolutely breaking the `import` system.

Looking back, I should have removed the one-line section from the talk and gone through it separately.
I had (for Python 3.9, so not working with any new syntax) a program that could procedurally convert _almost_
any Python program into a one-line version, but couldn't explain what it does or how it works in the video
due to time limitations.

My two favourite bits from the talk are the title slide and the module importing. The title slide alone took
three days to make - if you've seen it, you likely understand why it took so long - and was made entirely by
hand, i.e. without using the onelineriser I discuss above[^2]. The importing section led to my single favourite
line for me to say: "[the module] one plus [the module] one is two, and we now have a file called `two.py`".

Also the fun program at the end - a _syntactically invalid_ program that nonetheless runs - is explained
[in this Gist](https://gist.github.com/a-n-d-r-e-w-l/9f09b901a879bad5cc46d0c9607201d9).

When planning for this talk, I was worried about not having enough content to fill the 15 minutes - after my first
practice run-through I discovered that I'd written about _30_ minutes of content and had to trim it down.
This is what caused the breakneck pace of the talk, and also means that I have more cursed knowledge and ideas
that didn't make the cut. Maybe someday I'll make a followup with the rest.

[^1]: Unfortunately, it had to be re-recorded for technical reasons and the version that made it onto YouTube
didn't have an audience in the room for the actual talk, so it sounds like nobody's watching.

[^2]: It's not clear in the video, but at the [twelve minute mark](https://youtu.be/t863QfAOmlY?t=720), evaluating
the program results in a full-screen photo of the Spanish Inquisition (from Monty Python), while earlier simply
_running_ the program does not result in that. In [my Gist with the title slide](https://gist.github.com/a-n-d-r-e-w-l/c3fd7067debe512d8b02ca70ae712871),
I explain how it works.

### [covenant](https://github.com/a-n-d-r-e-w-l/covenant)

I've developed an experimental key-value store in Rust with some _very_ promising speed results.

The benchmark I currently have reports (roughly) 2x write speeds and ~4-10x read speed improvements over sqlite, though
of course sqlite is battle-tested and has full relational query support.

It's built on top of the _excellent_ [fst](https://crates.io/crates/fst) library, which provides bytes-to-`u64`
mapping in a very creative (and performant!) manner.

It is currently in an MVP state and is still missing a number of major features that would be desired
in any proper storage backing, which I intend to add later.

### Brainfuck

I did the [packet-storm](https://www.coretechsec.com/operation-packet-storm) graduate challenge
(code [here](https://github.com/a-n-d-r-e-w-l/packet-storm)) normally in Rust, reading file specs and the
Wireshark wiki, but then I had a terrible thought:

> This just reads a file byte-by-byte, performs some computation, and prints some text.\
> ...wouldn't this be possible in [brainfuck](https://en.wikipedia.org/wiki/Brainfuck)?

At that point, it was too late - once that idea had formed in my head, I felt compelled to _actually do it_.
Thus, next to my Rust solution there is a [`program.bf`](https://github.com/a-n-d-r-e-w-l/packet-storm/blob/main/program.bf)
file and a directory containing the preprocessor I made to help make it.

I'd previously come across brainfuck but never done anything in it, let alone any large project.
As such, I had to learn _a lot_ of techniques to construct a functioning non-trivial program.
I wouldn't do this again - however painful you're guessing this was, it was worse than that -
but working in such a restricted language did force me to think about solving normal problems in
novel ways (division was an interesting one), and the feeling of creating solid building blocks
and composing them felt far more significant than doing so in a ~~sensible~~ normal language.

## Why's it so empty here?

I don't use GitHub for my code hosting - all my projects live on a private
[Forgejo](https://forgejo.org/) instance that I host, and only a few get mirrored over here.

I have also historically used a different GitHub account dating back to 2015, but moved to
this account in April 2020 after having significant difficulty logging into the other account.
