### Overview

This code supplements my poster from the 2016 Ocean Sciences Meeting, entitled "Visualizing ecosystem energy flow in complex food network graphs."  I've also written a series of blog posts on my website ([here](http://kellyakearney.net/2016/01/19/food-webs-as-network-graphs-1.html), [here](http://kellyakearney.net/2016/01/19/food-webs-as-network-graphs-2.html), and [here](http://kellyakearney.net/2016/01/19/food-webs-as-network-graphs-3.html)) which explain the theory behind this set of code, and go through an example of using it.

For additional information, please read the documentation in the headers of each .m file.

### Installation

To download the code:

```
git clone git@github.com:kakearney/foodwebnetworkgraph-pkg.git
```

In Matlab, add all first-level child folders of the new `foodwebnetworkgraph-pkg` folder (except the .git folder) to your Matlab path:

```matlab
tmp = regexp(genpath('foodwebnetworkgraph-pkg'), pathsep, 'split');
n = cellfun(@(x) length(regexp(x,filesep,'split')), tmp);
toadd = (n == 2) & cellfun('isempty', regexp(tmp, '\.git'));
addpath(tmp{toadd});
```

Follow the example [from the blog post](http://kellyakearney.net/2016/01/19/food-webs-as-network-graphs-3.html) to get started.

