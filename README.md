### Wat?

Hi! I'm `blogric`. I'm a tiny little [Fabric](http://www.fabfile.org/) library
for blogging with [Pelican](http://blog.getpelican.com/) and
[Github Pages](https://pages.github.com/). I make a looooot of assumptions,
because _mostly_ I'm for @gastove to use for his [assorted](blog.gastove.com)
[blags](food.gastove.com). If you wanna use me, you should probably:

1. not.

But if you're gonna anyways, do like this!

1. I need to live in your blogs gitrepo; `Fabric` needs to be able to find me as
your `fabfile`. This means:
```bash
                ## Just name the repo fabric:
                        git clone git@github.com:Gastove/blogric.git fabfile

                                ## OR
                                        git clone git@github.com:Gastove/blogric.git && ln -s ./blogric ./fabfile
```
2. (This says 1 again because Github is a Jerk about Numbers. So I'm going to
sulk, and you can meet me at the next enumeration.)
3. ANYWAYS, I also need `fabric`. I've got a requirements file, so probably `pip
   install -r fabfile/requirements.txt` is what you want (though you could also
   manually add the fab version I need to your blags' reqs. You know, you do you.)
3. I assume your development branch is named `dev` and your published branch is
named `master`.
3. I've got a really spiffy `new_post` command; it'll ask you for a name, then
make a post like `content/posts/<today's date, iso
formatted>_words_from_your_name.markdown`. I'll set default `Pelican`
metadata at the top, then try and pop the new post open in `$EDITOR`.
4. I may at basically any moment explode.

Assuming this works, you now have some Blaggening Commands!
```bash
$ fab --list
Available commands:

    clean              Remove old content
    devserver_start    Run server; reload if output changes
    devserver_stop     Stop the devserver
    drafts
    gen                Generate static blog content
    generate           Generate static blog content
    generate_new_post  Make a new post
    list_drafts
    list_published
    np                 Make a new post
    publish            Publishes the current master branch to GH Pages
    published
    start              Run server; reload if output changes
    stop               Stop the devserver
```

Have fun!
