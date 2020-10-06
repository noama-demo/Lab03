# Lab-03
## Exercise 1 - Merging two branches
In this excercise, we have 2 branches, feature/FeatureA and feature/FeatureB which we will merge to master.

#### Cloning a repo
- Go to a playground folder using explorer (c:\temp, for example)
- Right click inside the folder and select 'GitExt Clone...'
- Paste the URL https://github.com/noama-demo/Lab03-ex1.git and choose clone

#### Merge feature/featureA
- On the left pane, right click master branch and select Checkout (if not already checkout out)
- On the history window, right click feature/featureA and choose 'merge into current branch' -> feature/featureA
- Select 'always create new merge commit' and click Merge
- Review the new commit merge
    - Select the new merge commit
    - In the Split View -> diff, review the differences between the last merge commit and its two parents

#### Merge feature/featureB
- Checkout master branch (if not already checked out)
- On the left panel, right click feature/featureB and choose 'merge' (this is an alternative to clicking on the commit itself)
- Select 'always create new merge commit' and click merge
- Review the new commit merge
    - Select the new merge commit
    - In the Split View -> diff, review the differences between the last merge commit and its two parents

#### Mail the results
- To: <TBD>
- Topic: merge and rebase ex1
- Body: What are the differences between master and feature/FeatureB?


## Exercise 2 - Merging and Rebasing
In this excercise, we have 2 branches, feature/FeatureA and feature/FeatureB which contains the output of their feature name   
Another branch, named feature/featureAB contains a fix that requires both classes A and B to output the feature name (Console.WriteLine("FeatureB"),Console.WriteLine("FeatureA"))  
However, these outputs exist only on the master branch and not on the feature/featureAB branch  
We need to apply the master content to feature/featureAB branch prior to merging feature/featureAB to master

#### Cloning a repo
- Go to a playground folder using explorer (c:\temp, for example)
- Right click inside the folder and select 'GitExt Clone...'
- Paste the URL https://github.com/noama-demo/Lab03-ex2.git and choose clone

#### Viewing the environment
- In the history pane, select feature/featureAB commit and explore the Split View -> File Tree for the content of 
    1. Lab-03-ex2\gitDemo\ClassA.cs
    2. Lab-03-ex2\gitDemo\ClassA.cs. 
    - See that they have no Console.WriteLine(feature) output
- In the history pane, select master commit and explore the Split View -> File Tree for the content of 
    1. Lab-03-ex2\gitDemo\ClassA.cs
    2. Lab-03-ex2\gitDemo\ClassA.cs. 
    - See that they do contain Console.WriteLine(feature) output

Thereof, in order to fix feature/featureAB, we need to get the master branch content (of both features A and B).
We have 2 options:
1. merge master to feature/featureAB - which will add the master content to our branch
or
2. rebase feature/featureAB on the master branch, which will rebuild our commits on top of the master.

#### Merge master to feature/featureAB
- In this excercise, we will choose option 1. This will merge the master content to feature/FeatureAB branch.
    - On the left pane, right click feature/featureAB branch and select Checkout
    - On the left pane, right click master branch and choose 'merge'
    - Select 'always create new merge commit' and merge
- Verify that feature/featureAB now contains both outputs:
    - On the history pane, select the feature/featureAB branch and check the Split View -> File Tree. See that both classes have outputs.
    - On the history pane, select feature/featureAB branch and the master branch. See their diff in the Split View.

#### Merge feature/featureAB to master
- Merge feature/featureAB branch to master to complete the feature/featureAB and apply its content in master branch
    - Checkout master branch (if not already checked out)
    - On the left panel, right click feature/featureAB and choose 'merge' (this is an alternative to clicking on the commit itself)
    - Select 'always create new merge commit' and merge

#### Mail the results
- To: <TBD>
- Topic: merge and rebase ex2
- Body: What are the differences between master and feature/FeatureAB?

## Exercise 3 - Merging and Rebasing
In this excercise, we have 2 branches, feature/FeatureA and feature/FeatureB which contains the output of their feature name   
Another branch, named feature/featureAB contains a fix that requires both classes A and B to output the feature name (Console.WriteLine("FeatureB"),Console.WriteLine("FeatureA"))  
However, these outputs exist only on the master branch and not on the feature/featureAB branch  
We need to apply the master content to feature/featureAB branch prior to merging feature/featureAB to master

#### Cloning a repo
- Go to a playground folder using explorer (c:\temp, for example)
- Right click inside the folder and select 'GitExt Clone...'
- Paste the URL https://github.com/noama-demo/Lab03-ex3.git and choose clone

#### Viewing the environment
- In the history pane, select feature/featureAB commit and explore the Split View -> File Tree for the content of 
    1. Lab-03-ex3\gitDemo\ClassA.cs
    2. Lab-03-ex3\gitDemo\ClassA.cs. 
    - See that they have no Console.WriteLine(feature) output
- In the history pane, select master commit and explore the Split View -> File Tree for the content of 
    1. Lab-03-ex3\gitDemo\ClassA.cs
    2. Lab-03-ex3\gitDemo\ClassA.cs. 
    - See that they do contain Console.WriteLine(feature) output

Thereof, in order to fix feature/featureAB, we need to get the master branch content (of both features A and B).
We have 2 options:
1. merge master to feature/featureAB - which will add the master content to our branch
or
2. rebase feature/featureAB on the master branch, which will rebuild our commits on top of the master.

#### Rebase feature/featureAB on top of master
- In this excercise, we will choose option 2. This will merge the master content to feature/FeatureAB branch.
    - On the left pane, right click feature/featureAB branch and select Checkout
    - On the left pane, right click master branch and choose rebase ('rebase current branch to this branch')
    - Leave all settings on default and click Rebase
- Verify that feature/featureAB now contains both outputs:
    - On the history pane, select the feature/featureAB branch and check the Split View -> File Tree. See that both classes have outputs.
    - On the history pane, select feature/featureAB branch and the master branch. See their diff in the Split View.

#### Merge feature/featureAB to master
- Merge feature/featureAB branch to master to complete the feature/featureAB and apply its content in master branch
    - Checkout master branch (if not already checked out)
    - On the left panel, right click feature/featureAB and choose 'merge' (this is an alternative to clicking on the commit itself)
    - Select 'always create new merge commit' and merge

#### Mail the results
- To: <TBD>
- Topic: merge and rebase ex2
- Body: What are the differences between master and feature/FeatureAB?
