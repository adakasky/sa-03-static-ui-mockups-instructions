<img src="/images/ucombinator_logo.png" width="100">

# Startup Assignment 03 - Static UI Mockups

UCombinator is currently reviewing your product and feature pitches,
and will be in contact with you soon to let you know if your product
and features are accepted.  Until then, consider your product and
features *provisionally* accepted.

Now, UCombinator wants to see what your product will *look* like. It's
time to take the abstract idea you talked about in your product pitch
and turn it into HTML and CSS mockups using Bootstrap.

In addition, UCombinator wants to see a mockup of each honors
student's proposed feature. Honors students will need to participate
in the main product mockup *and* produce a mockup of their proposed
feature.

We detail everything below.

## Your Product's Git Repository

UCombinator has furnished your startup with a snazzy Git repository
equipped with modern build support. You will use this repository to
develop the frontend of your application. Below, we describe how to
use it.

### Getting and Preparing the Git Repository

Each startup team will maintain their own git repository on github. To begin, **one team member** must [fork](https://help.github.com/articles/fork-a-repo/) the [team project client template](https://github.com/umass-cs-326/team-project-client-template) github repository into their own github account as a *public* repository. After they have cloned the client template project that team member must provide access to the repository by [inviting collaborators](https://help.github.com/articles/inviting-collaborators-to-a-personal-repository/). Make sure you give each collaborator *write* access to the forked repository. Each collaborator will be sent an email to accept the invitation to collaborate. After a collaborator accepts the invitation they can then clone the git repository as usual.

Use Git to clone your startup's repository. Then, `cd` into the repository, and type `npm install`. This command will begin a one-time setup process that pulls in the tools and libraries that our build scripts depend on. When we eventually cover JavaScript, you will likely use NPM to manage your product's dependencies on external libraries.

*Note: If you ever need to clone your repository again, remember to
run `npm install` in the new repository clone.*

After the command completes, you'll notice a new folder called
`node_modules` in the repository. This folder contains all of the
dependencies that `npm` just installed. Don't mess with these
files. Also, do not add this folder to Git.

### Running a Web Server

Run `npm run serve` within the Git repository to run a webserver at
`http://localhost:8080/`.  Like with Workshop 3, this webserver will
remain open as long as you keep the terminal open.

Later on, as you add JavaScript to your project, this same command
will handle re-building your application as you change it while
simultaneously running the web server.

### Git Repository Files

* `.gitignore`: Entries in this file
  are [ignored by Git](https://git-scm.com/docs/gitignore).  We've
  added entries for automatically generated folders/files that you do
  not want to add to your repository, such as `node_modules`.
* `.eslintrc`: We'll cover this when you add JavaScript to your
  project. For now, leave this file alone.
* `webpack.config.js`: This is a
  [webpack configuration script](https://webpack.github.io/docs/configuration.html),
  which tells `npm run serve` (and `npm run build`) how to build your
  project and serve it up over HTTP. You should not need to touch this
  script.
* `app/`: This is where you will put the JavaScript/React code for
  your application.  You won't need to touch this folder just yet.
* `build/`: This is where you put the HTML, CSS, images,
  [web fonts](https://en.wikipedia.org/wiki/Web_typography#Web_fonts),
  and other assets for your application. We've pre-populated this
  folder with a "Hello World" `index.html`, and Bootstrap
  dependencies.
  * When you eventually add JavaScript to your application, webpack
    will magically bundle it into `build/js/app.js`. The `build/js`
    folder currently contains Bootstrap's JavaScript files.
* `package.json`: Contains a list of NPM dependencies that you
  installed with `npm install`, and the logic behind the `npm run
  serve` / `npm run build` commands. Do not mess with this file. The
  graders depend on the `npm run` commands working properly.

You will add your mockups in the `build/` folder as separate HTML
files.

### Collaborating Using Git

Your startup is sharing a single Git repository, and is going to need
to figure out an effective Git workflow. Communication is really
important in a team.

Some pro tips:

* Figure out an effective way to assign tasks to startup founders.
  * Your GitHub repository comes with a
    nice [issue tracker](https://guides.github.com/features/issues/),
    which you may find useful for organizing tasks. You can even
    reference issue numbers in Git commit messages (e.g. "Makes
    further progress on #12").
* Talk to one another before renaming files or making huge changes.
  * Don't be the person who changes every file in a single commit just
    before the deadline, unless you verified that it's OK with your
    team. :)
* Get comfortable with merge conflicts.
  * Even the most organized teams will encounter merge
    conflicts. Everyone in your team has had to handle one in a
    workshop setting; the merge conflicts you'll encounter on your
    project are no harder than that.
* Did you just create a new file? Remember to `git add` it!
  * Git needs to know about any new files you've created. It's easy to
    forget to add a new file. **If it's not in Git, we cannot grade
    it!**

## Product Mockups

UCombinator wants to see *static* (non-interactive) UI mockups of your
product that you've created using HTML, CSS, and Bootstrap. Each
individual HTML file should illustrate a single *screen* of your
application.

A *screen* is either a distinct visual change on a webpage, or a
different page of your application. Let's illustrate this with
Twitter.

Screen 01: My Twitter feed. This is what the UCombinator Vice
President sees after he logs into Twitter:

![Twitter Screen 1](/images/twitter_screen_01.png)

Screen 02: The same Twitter feed with a tweet selected. After the user
clicks on the tweet, Twitter unfolded a series of snarky comments
about the tweet, and a *reply* box. Both of these things were not
there before:

![Twitter Screen 2](/images/twitter_screen_02.png)

Screen 03: A Twitter view of a single tweet in isolation. If the user
shares the URL to the tweet with someone, this is the page they are
brought to.

![Twitter Screen 3](/images/twitter_screen_03.png)

Screen 04: The UCombinator Vice President's Twitter page. This page
contains all of his tweets and retweets.

![Twitter Screen 4](/images/twitter_screen_04.png)

Screen 05: Search results for "cute kittens". This screen comes up
when a user searches for something.

![Twitter Screen 5](/images/twitter_screen_05.png)

Screen 06: Composing a new tweet. This box comes up when the user hits
the "Tweet" button in the upper-right corner.

![Twitter Screen 6](/images/twitter_screen_06.png)

...make sense? Each screen contains new visual widgets that were not
there before.  Your startup's screen mockups should give UCombinator a
feel for what it's like to use your product.

Each screen should be in a separate HTML file in the `build/`
directory of your repository (e.g. `build/new_tweet.html`,
`build/tweet_feed.html`, etc).  You're likely going to need to do a
bit of copy + pasting to copy common elements shared between screens.

For your mockups, please make the following assumptions:

* **A user is logged in to your service.** Your mockups should
  illustrate what your product looks like to a registered user.

UCombinator will **NOT** grade:

* **Log in/log out/account creation screens.** We encourage startups
  to explore these screens *if they have time*, but they will go
  unused until we cover how to securely support user accounts and user
  logins much later on in the course.

### Submission & Grading Rubric

UCombinator expects that your startup will submit:

* **At least as many screens as you have startup founders.** As
  mentioned earlier, each screen should be in its own HTML document in
  the `build/` directory.
  * As mentioned above, login/logout/account creation screens will
    *not* count toward this total, and are *not* required for this
    submission.
  * This is a *minimum number*. In practice, you should submit as many
    screens as needed for your application. UCombinator will be
    disappointed if an application has 8 large menu buttons that point
    to different parts of the application, but only 4 are mocked up.
* **A written report.** The report should be included in your Git
    repository as `reports/submission_02.pdf`. It should include:
  * A tour of your UI, with screenshots. Explain what each of the
    screens is for, and the transitions between screens.
  * A description of what each startup founder worked on. We expect
    that each startup founder is responsible for the UI of at least
    one major widget on the webpage.
      * A "widget" is a major HTML element of the application. For
        Facebook, a status update, the left sidebar, the top
        navigational bar, and the notifications menu are all
        "widgets".
      * We are going to check your repository's Git history to verify
        that your report is accurate.
      * It is not acceptable for a startup founder to just write the
        report; everyone must "get their hands dirty" with HTML/CSS.

The grading rubric is as follows:

* 30% Written report
  * 15% Contains a clear, understandable tour of your product's UI,
    using screenshots of your mockups
  * 15% Contains a clear explanation of what each startup founder
    contributed to the submission
* 20% Screens use custom CSS to style Bootstrap components / elements
  on the page
  * 10% Use a consistent custom color scheme
      * There are a [bunch](http://paletton.com/) [of free](https://coolors.co/)
      [color scheme](https://color.adobe.com/) generators online that use
      [color theory](https://en.wikipedia.org/wiki/Color_theory) to generate
      aesthetically-pleasing themes.
      * Don't use default Bootstrap colors for everything. While it
        looks nice, UCombinator wants startups to differentiate
        themselves in the market.
  * 10% Appropriately manipulates element margin/padding space to
    avoid awkward whitespace between elements
      * If there's weird, unnatural empty space between things, we
        will question it. There are at least three occasions in
        Workshop 3 where we have to manipulate these CSS properties to
        fix spacing issues with Bootstrap.
* 20% Includes enough screens to understand how major features of
  product will look, and includes *at least* as many screens as
  startup members
  * If there's a search box, but no search results screen, we will be
    sad.
* 30% [Individually] Created the UI of a major product feature, and
  accurately portrayed contribution in report

UCombinator reserves the right to scale individual scores further if
we perceive that a founder is not pulling their weight, or that a
founder is doing extra work to make up for a lackluster
founder. However, since everyone in the class seems pretty awesome,
UCombinator doubts that it will need to do this.

**Before the due date, please verify from a fresh clone of your
repository that your mockups display properly.** It is easy to forget
to `git add` files. We are going to grade *what's in your Git
repository on GitHub*, and not *what's on your computer's hard
drive*. Also, if you break the `npm run serve` command, we will dock
points from your submission.

## Honors Students: Feature Mockups

*This section only applies to semesters when an honors section is
provided*

**In addition to the group submission**, honors students must make a
mockup of the UI of their feature. The mockup must consist of at least
one screen.

### Submission & Grading Rubric

* 30% Written report contains a clear, understandable tour of your
  feature's UI, using screenshots of your mockups
  * This should be put into a separate section of the group report.
* 40% Includes enough screens to understand what the feature will look
  like, and how it will behave
* 30% Screens use custom CSS to style Bootstrap components / elements
  on the page
  * 15% Use a consistent custom color scheme
  * 15% Appropriately manipulates element margin/padding space to
    avoid awkward whitespace between elements
