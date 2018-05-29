# Object-Oriented Design Class

## Dependencies

You will need:

* git
* a modern version of Ruby (1.9.3 or greater)

## Setup

Clone this repository:

```bash
$ git clone git@github.com:torqueforge/shopify-2018-ottawa.git
```

Change directories so that you are in the project:

```bash
$ cd shopify-2018-ottawa
```

Install the dependencies:

```bash
$ gem install bundler # if you don't have it
$ bundle install
```

## Sanity Check Setup

To verify that everything is set up correctly, run the following command:

```bash
$ ruby sanity_test.rb
```

You should see the following output.
```bash
$ ruby sanity_test.rb
Run options: --seed 62459

# Running:

.

Finished in 0.001317s, 759.3014 runs/s, 759.3014 assertions/s.

1 runs, 1 assertions, 0 failures, 0 errors, 0 skips
```

## Exercises

Class consists of a number of exercises. Each exercise has its own
subdirectory and README.

## Working on the exercises

We'll successively add exercises to `master` over the next few days.  This means that you'll have to `git pull` from master a number of times.  Therefore, it's best if you DON'T CHECK ANYTHING INTO MASTER on your local machine.  If you wish to save copies of your own code, make a local branch.

Therefore, to work on the 'bottles' problem you would
```bash
$ git checkout master
```

Create a new branch to hold your work on this exercise:
```bash
$ git checkout -b my-bottles-branch
```

Change to the bottles directory and work on the exercise:
```bash
$ cd bottles
```

When you want to save your work, stage and commit your changes:
```bash
$ git add . # notice the dot
$ git commit -m "Explain your change here"
```

When we start working on the next section of bottles (or move to a new exercise
altogether) save your outstanding work (as above) and then switch back to master:
```bash
$ git checkout master
```

Pull the latest version from GitHub:
```bash
$ git pull origin
```

Then create another new branch to work on the next thing.
```bash
$ git checkout -b my-bottles-branch-2 # for the next section of 'bottles'
$ # or
$ git checkout -b my-farm-branch # for a new exercise entirely
```

## Git: Troubleshooting / Recovery

### Throw it all away?

You can throw all your code away like this:

First, make sure that git knows all about the files you have:

```bash
$ git add .
```

Then throw the changes away:

```bash
$ git reset --hard
```

### Did your master diverge?

Go ahead and create a new branch with all your changes:

```bash
$ git checkout -b my-backup-branch
```

Then go back to master:

```bash
$ git checkout master
```

Make sure you have the most recent changes from GitHub:

```bash
$ git fetch origin
```

Then tell git to create a new copy of master, throwing away the old one:

```bash
$ git reset --hard origin/master
```
