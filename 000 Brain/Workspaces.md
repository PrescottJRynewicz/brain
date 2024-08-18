---
Created On: 2024-06-07, 16:36
Unique ID: 202406071636
---
**Status:** #review 

**Tags:** #TurborepoCards

# Workspaces

#### How do packages in a monorepo share code?
?
They specifically have an `export` keyword in their `package.json` that points to entry points that other packages are allowed to import.
<!--SR:!2024-07-03,12,250-->

#### What are barrel files and how should they be used?
?
Barrel files are a common way to expose available code to other developers - i.e. it's one file that re-exports a bunch of other code in other files to have a single place where other developers can import code from. 
But, it is difficult for bundlers to parse and tree shake these files, so they are not recommended.
<!--SR:!2024-07-05,14,250-->

#### Should we keep dependency versions 


---
# References
