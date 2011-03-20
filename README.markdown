Calculator
==========

An example repository used at [Git workshops](http://gitfu.cz/).

Contains very simple “application”, a calculator, in HTML/CSS/JS,
making it trivial for attendees with different programming
backgrounds to focus on the _Git_ domain, not on the code domain,
during the workshop.

Our imaginary scenario in the workshop is this one:

_How to make a hotfix while working on feature when the main line is moving_

The repository contains four branches:

* `master` — The main line of development. You cooperate with others on this branch.
* `feature` — The “feature branch” for the imaginary scenario.
* `hotfix` — A branch for making a “hotfix” in the imaginary scenario.
* `new_design` — A branch with updated GUI in our imaginary scenario.

The simplified scenario for the _feature_ part is:

    $ git checkout -b feature
    $ git add .
    $ git commit -m "TMP: Feature"

When the request for _hotfix_ comes in, this is the simplified scenario:

    $ git checkout master
    $ git checkout -b hotfix
    $ git add .
    $ git commit -m "Fixed vulnerability"
    $ git checkout master
    $ git pull
    $ git merge hotfix
    $ git push origin master

To continue work on _feature_, we can return where we were previously:

    $ git checkout feature
    $ git reset HEAD^

Please refer to the PDF handout for full scenarios and information.
