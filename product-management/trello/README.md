Product management process with Trello
======================================

A Trello board is a software equivalent of a physical wall with columns of
sticky notes. In Trello terminology, the wall is called a "board." The columns
are called "lists." The sticky notes in columns are called "cards."

No two products are the same, so flexibility in the product management process
is important. Trello responds well to changing the structure of the process
"on the fly."

Our product management process with [Trello](http://trello.com) can span multiple
Trello boards:

* Product Design (Backlog)
* Current Dev

![Current](http://mctekk.com/git/trello_1.png)

"Current" is an example of a board. "In Progress" is an example of a list. "User Feeds" is an example of a card.

* Next Up
* Doing
* Offline Revision
* Online Revision (Ready for Production)
* Done (Week X)

Cards from Product Design are pulled into the Next Up
list on the Current board as described in the "Weekly Product Meeting" section
below.

The Next Up list is the single prioritized list to which the product team
refers in order to know what to work on next. It represents one week of work.

Trello cards
------------

A card represents a single user story, bug fix, engineering task, or general
todo.

Cards start out as a simple idea, 1-2 sentences long. As they are pulled through
boards, detail is added, explaining why (from a business perspective)
we're focusing on it, and maybe notes on suggested implementation (though
designers and developers may take or leave it at their discretion; it's supposed
to be helpful, not prescriptive).

Bugs
----

The cards on this board are bugs in the described state. There are multiple
lists on this board:

* Reported
* Needs Clarification
* Ready for Next Up

If a bug is labeled Critical, then it is pulled immediately into Next Up. If the
bug is not critical, it stays in Bugs until the next product meeting.

A bug has steps to reproduce the bug and optionally a screenshot or screencast.

Product Design (BackLog)
--------------

The cards on this board lists are the result of sketching user flows, usability
tests, other user research, or the designer's feel for visual design
improvements. There are multiple lists on this board:

* Features Description
* User Experience
* Ready for Next Up

Weekly Product Meeting (1-2 hours)
----------------------------------

On Monday, the product manager and lead developer meet in person. 
They load the product on a screen, focus on recent changes to it, and
use the working app and Trello boards to plan the upcoming week's iteration. The
product manager runs the meeting like this:

* Archive the two-week old "Live (Week of [date])" list.
* Review the Product Design board. Pull what we estimate to be an appropriate
  amount for this week into Next Up.
* Re-sort the entire Next Up queue according to priority. Cards that were at the
  top of the list last week may be moved to the bottom or back to the Product
  Design, Bugs, or Engineering & Refactoring boards.
* Review the Bugs board. Pull any important bugs into Next Up and prioritize
  then at the top of the queue before everything else. We want to always be
  fixing what's broken first.


Building and Shipping
---------------------

![Shipping](http://mctekk.com/git/trello_2.png)

The cards in the Next Up list are prioritized, vetted, and ready for design &
development. A designer or developer "puts their face on it" if the taks doesnt have anybody assign to it, then the devs can
do it themselves and pulling it into the In Progress list.

Designers and developers may pull any card out of Next Up that they feel they
can handle, but should consider the cards are prioritized by importance.

The cards in the Doing list are actively being designed or developed.
Etiquette is that you should never have your face on more than two cards at a
time. Work is done in a [feature branch](/protocol).

When a designer or developer creates a pull request for their feature branch,
they move the card to the Offline Revision. Any reviewers "put their face on it"
while reviewing.

There is no central chokepoint for merging into master: everyone can do it.

The cards in the Online Revision (Ready for Production) list include cards that have been accepted
on staging (Offline Revision) and are ready to be deployed (but not necessarily rolled out).

There is no central chokepoint for releasing to production: everyone can do it.

The cards in the Live (Week of [date]) lists have been released. Each week has
its own Live list so we can follow what got released when.