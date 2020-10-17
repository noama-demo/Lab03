# Lab-03
## Exercise 1 - Merging two branches
### Overview
In this exercise, we will work with branches and merges  
We have 2 branches, feature/FeatureA and feature/FeatureB which we will merge to master.

#### <u> Cloning a repo </u>
- Go to a playground folder using explorer (c:\temp, for example)
- Right click inside the folder and select 'GitExt Clone...'
- Paste the URL C:\GitServer\labs\Lab03-ex1 and choose clone
- Right click inside/on the folder and select 'GitExt open repository'


#### <u> Merge feature/featureA </u>
- On the left pane, right click <i>Remotes -> Origin -> feature/FeatureA</i> branch and select <i>Fetch & Checkout</i>. This will create our local <i>feature/FeatureA</i> branch. Press <i>Checkout</i> if required.
- On the left pane, right click <i>Remotes -> Origin -> master</i> branch and select <i>Fetch & Checkout</i>. This will create our local master branch. Press <i>Checkout</i> if required.
- On the history window, right click <i>feature/FeatureA</i> and choose <i>merge into current branch -> feature/FeatureA </i>
- Select <i>always create new merge commit</i> and click <i>Merge</i>
- Review the new commit merge
    - Select the new merge commit
    - In the <i>Split View -> diff</i>, review the differences between the last merge commit and its two parents

#### <u> Merge feature/featureB </u>
- Checkout master branch (if not already checked out)
- On the left panel, right click feature/featureB and choose 'merge' (this is an alternative to clicking on the commit itself)
- Select 'always create new merge commit' and click merge
- Review the new commit merge
    - Select the new merge commit
    - In the <i>Split View -> diff</i>, review the differences between the last merge commit and its two parents

#### <u> Mail the results </u>
- To: <TBD>
- Topic: merge and rebase ex1
- Body: What are the differences between master and feature/FeatureB?


## Exercise 2 - Merging
### Overview
In this excercise, we have 2 features in 2 branches, which prints the output of their feature name: <i>feature/featureA</i> and <i>feature/featureB</i>  
Another branch, named <i>feature/featureAB</i> contains a fix that requires both classes A and B to output the feature name (Console.WriteLine("FeatureA"),Console.WriteLine("FeatureB"))  
However, these outputs exist only on the master branch and not on the <i>feature/featureAB</i> branch  
We need to update our feature/FeatureAB</b> branch with the master content prior to merging <i>feature/featureAB</i> back to master.

#### <u> Cloning a repo </u>
- Go to a playground folder using explorer (c:\temp, for example)
- Right click inside the folder and select 'GitExt Clone...'
- Paste the URL C:\GitServer\labs\Lab03-ex2 and choose clone

#### <u> Viewing the environment </u>
- In the history pane, select <i>feature/featureAB</i> commit and explore the <i>Split View -> File Tree</i> for the content of 
    1. gitDemo\ClassA.cs
    2. gitDemo\ClassB.cs. 
    - See that they have no Console.WriteLine(feature) output
- In the history pane, select <i>master</i> commit and explore the <i>Split View -> File Tree</i> for the content of 
    1. gitDemo\ClassA.cs
    2. gitDemo\ClassB.cs. 
    - See that they do contain Console.WriteLine(feature) output

Thereof, in order to fix <i>feature/featureAB</i>, we need to get the <i>master</i> branch content (of both features A and B).
We have 2 options:
1. merge master to <i>feature/featureAB</i> - which will add the <i>master</i> content to our branch
or
2. rebase <i>feature/featureAB</i> on the <i>master</i> branch, which will rebuild our commits on top of the <i>master</i>.

#### <u> Merge master to feature/featureAB </u>
- In this excercise, we will choose option 1. This will merge the master content to feature/FeatureAB branch.
    - On the left pane, right click <i>Remotes -> Origin -> feature/FeatureAB</i> branch and select <i>Fetch & Checkout</i>. This will create our local feature/FeatureAB branch. Press <i>Checkout</i> if required.
    - On the left pane, right click <i>master</i> branch and choose <i>merge</i>
    - Select <i>always create new merge commit</i> and <i>merge</i>
- Verify that <i>feature/featureAB</i> now contains both outputs:
    - On the history pane, select the <i>feature/featureAB</i> branch and check the <i>Split View -> File Tree</i>. See that both classes have outputs.
    - On the history pane, select <i>feature/featureAB</i> branch and the <i>master</i> branch. See their diff in the Split View.

#### <u> Merge feature/featureAB to master </u>
- Merge <i>feature/featureAB</i> branch to <i>master</i> to complete the <i>feature/featureAB</i> and apply its content in <i>master</i> branch
    - Checkout <i>master</i> branch (if not already checked out)
    - On the left panel, right click <i>feature/featureAB</i> and choose <i>merge</i> (this is an alternative to clicking on the commit itself)
    - Select <i>always create new merge commit</i> and <i>merge</i>

#### <u> Mail the results </u>
- To: <TBD>
- Topic: merge and rebase ex2
- Body: What are the differences between master and feature/FeatureAB?

## Exercise 3 - Rebasing
### Overview
In this excercise, we have 2 features in 2 branches, which prints the output of their feature name: <i>feature/featureA</i> and <i>feature/featureB</i>  
Another branch, named <i>feature/featureAB</i> contains a fix that requires both classes A and B to output the feature name (Console.WriteLine("FeatureA"),Console.WriteLine("FeatureB"))  
However, these outputs exist only on the master branch and not on the <i>feature/featureAB</i> branch  
We need to update our feature/FeatureAB</b> branch with the master content prior to merging <i>feature/featureAB</i> back to master.

#### <u> Cloning a repo </u>
- Go to a playground folder using explorer (c:\temp, for example)
- Right click inside the folder and select 'GitExt Clone...'
- Paste the URL C:\GitServer\labs\Lab03-ex3 and choose clone

#### <u> Viewing the environment </u>
- In the history pane, select <i>feature/featureAB</i> commit and explore the <i>Split View -> File Tree</i> for the content of 
    1. gitDemo\ClassA.cs
    2. gitDemo\ClassB.cs. 
    - See that they have no Console.WriteLine(feature) output
- In the history pane, select <i>master</i> commit and explore the <i>Split View -> File Tree</i> for the content of 
    1. gitDemo\ClassA.cs
    2. gitDemo\ClassB.cs. 
    - See that they do contain Console.WriteLine(feature) output

Thereof, in order to fix <i>feature/featureAB</i>, we need to get the <i>master</i> branch content (of both features A and B).
We have 2 options:
1. merge master to <i>feature/featureAB</i> - which will add the <i>master</i> content to our branch
or
2. rebase <i>feature/featureAB</i> on the <i>master</i> branch, which will rebuild our commits on top of the <i>master</i>.

#### <u> Rebase feature/featureAB on top of master </u>
- In this excercise, we will choose option 2. This will rebase <i>feature/FeatureAB</i> branch on top of the <i>master</i>.
    - On the left pane, right click <i>Remotes -> Origin -> feature/featureAB</i> branch and select <i>Fetch & Checkout</i>. Select <i>checkout</i> if required.
    - On the left pane, right click <i>master</i> branch and choose <i>rebase (rebase current branch to this branch)</i>
    - Leave all settings on default and click Rebase
- Verify that <i>feature/featureAB</i> now contains both outputs:
    - On the history pane, select the <i>feature/featureAB</i> branch and check the <i>Split View -> File Tree</i>. See that both classes have outputs.
    - On the history pane, select <i>feature/featureAB</i> branch and the <i>master</i> branch. See their diff in the Split View.

#### <u> Merge feature/featureAB to master </u>
- Merge <i>feature/featureAB</i> branch to master to complete the <i>feature/featureAB</i> and apply its content in <i>master</i> branch
    - Checkout <i>master</i> branch (if not already checked out)
    - On the left panel, right click <i>feature/featureAB</i> and choose <i>merge</i> (this is an alternative to clicking on the commit itself)
    - Select <i>always create new merge commit</i> and <i>merge</i>

#### <u> Mail the results </u>
- To: <TBD>
- Topic: merge and rebase ex3
- Body: What are the differences between master and feature/FeatureAB?
