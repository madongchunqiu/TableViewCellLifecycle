# Description
The UITableViewCell+Lifecycle category (with MDTableViewDelegate) provide lifecycle events for UITableViewCell, just like UIViewController:
* cellWillAppear
* cellDidAppear
* cellDidLayoutSubviews
* cellDidDisappear

# Why
I'm a big fan of UITableView, since it provides the flexibility of organizing contents dynamically.
And with more and more animations in the UI, I found it hard to locate my code elegantly.
On the otherhand, UIViewController is nice with viewWillAppear, willDidAppear, viewDidLayoutSubviews, viewWillDisappear and viewDidDisappear etc. 
I though I shall make this happen to UITableViewCell.

# How to Use
see the sample code
1. include UITableViewCell+Lifecycle.h/m and MDTableViewDelegate.h/m into your projects. Subclass MDTableViewDelegate, and put your tableView's dataSource and delegate code in this class. And these events will be triggerred in the cells.
2. include UITableViewCell+Lifecycle.h/m and subclass UITableViewController (this subclass shall explictly conform to protocol UITableViewDelegate), and the events will be triggerred in the cells.

# Known Issues
These events won't be triggerred if the whole tableView is going on-screen or off-screen. (Currently I don't see the need to fix this.)
It only happens when the UITableViewCell is scrolling into the screen or scrolling out-side of the screen.