## Vim setup

I’m assuming you know something about vim; if not, you’re missing out! Also,
follow tpope's [install instructions for fireplace](https://github.com/tpope/vim-fireplace),
his [pathogen plugin](https://github.com/tpope/vim-pathogen) makes it easy
to install other plugins and I highly recommend it.

You’ll want to start lein from the root of the project, where the project.cis
and put you in the namespace of . This way the lein repl will load all the
dependencies and such for your project. Then, at a different command prompt,
start vim or gvim or mvim. This always worked best for me when I actually
launch gvim from the command prompt, not starting from the app menu. Once
you load a .cfile, fireplace should kick in automatically. If it doesn’t,
type :Connect and you’ll get a few prompts to get connected.

**Here are a few of the commands I use most**:

* cpr loads the current file ns
* cqc starts a commandline for the repl
* cpp runs the current form under the cursor, so if you have this code:
`(println (* 2 3))` and your cursor is inside the `(* 2 3)` form, that’s what
will get evaluated. To get the entire form to evaluate, you need to make
sure your cursor is at the outer `()`.

Code gets evaluated to a commandline window in vim, so it’s a bit small,
but it should be useful enough to play around with code (repl driven
development for the win!). You'll need to evaluate any new functions
before you can call them and you'll need to evaluate them if you make any changes.

#### For working with a ring server:
When you create a new project using “lein new compojure-app guestbook”, you’ll
get some ring entries in your project.c You’ll want to add the following to
the :ring key; I added mine to the main ring key, not the ones under the
:profiles. I assume this is not a good idea for production, but I really don’t know.

    :auto-reload? true
      :auto-refresh? true
         :nrepl  {:start? true :port 5555}

Then start your project with `lein ring server` and start vim (or some other,
less awesome editor). Now as you edit code, the ring server should listen
for changes and refresh your code. This should also tie the ring server
into the nrepl so when you’re in fireplace (or cider or whatever), you can
evaluate code directly to the ring server.
