## Ghost.org Blog on OpenShift

Ghost is a free, open, simple blogging platform that's available to anyone who wants to use it. Lovingly created and maintained by [John O'Nolan](http://twitter.com/JohnONolan) + [Hannah Wolfe](http://twitter.com/ErisDS) + an amazing group of [contributors](https://github.com/TryGhost/Ghost/contributors).

Visit the project's website at [http://ghost.org](http://ghost.org)!

This git repository helps you get up and running quickly w/ a Ghost.org blog
installation on OpenShift.  The backend database is MySQL and the database name 
is the same as your application name.  You can name your application whatever 
you want.

### Running on OpenShift

Create an account at http://openshift.redhat.com/ and install the client tools (run 'rhc setup' first)

Create a nodejs-0.10 application (you can call your application whatever you want)

    rhc app create ghost nodejs-0.10 mysql-5 --from-code=https://github.com/samgreen/openshift-ghost

That's it, you can now checkout your application at:

    http://ghost-$yournamespace.rhcloud.com

Note: When you upload images and themes, they'll get put into your OpenShift data directory on the gear ($OPENSHIFT_DATA_DIR). 

### Logging in For The First Time

Once you have the Ghost server up and running, you should be able to navigate to `http://localhost:2368/ghost/` from a web browser, where you will be prompted for a login.

1.  Click on the "register new user" link
2.  Enter your user details (careful here: There is no password reset yet!)
3.  Return to the login screen and use those details to log in.

Note - this is still very alpha. Not everything works yet.


## Reporting Bugs and Contributing Code

Want to report a bug, request a feature, or help us build Ghost? Check out our in depth guide to [Contributing to Ghost](https://github.com/TryGhost/Ghost/blob/master/CONTRIBUTING.md). We need all the help we can get!


## Community

Keep track of Ghost development and Ghost community activity.

* Follow Ghost on [Twitter](http://twitter.com/TryGhost), [Facebook](http://facebook.com/tryghostapp) and [Google+](https://plus.google.com/114465948129362706086).
* Read and subscribe to the [The Official Ghost Blog](http://blog.ghost.org).
* Chat with Ghost developers on IRC. We're on `irc.freenode.net`, in the `#Ghost` channel.