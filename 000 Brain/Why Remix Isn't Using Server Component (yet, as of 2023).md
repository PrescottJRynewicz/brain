---
Created On: 2023-08-09, 21:59
Unique ID: 202308092159
sr-due: 2023-09-01
sr-interval: 13
sr-ease: 270
---
**Status:** #thought #in-progress 

**Tags:** #review [[Software Engineering]] [[Remix.run]] [[React.js]]

# Why Remix Isn't Using Server Component (yet, as of 2023)

React server components give you the ability to co-locate data with the components that own that data. But, no solution is perfect, and this architecture easily causes async render waterfalls. 

Component one fetches data, then can render its children. Now the children can fetch their data, and so on. 

Remix solves this in a different way. Every layout component can define its own loader. Loaders don't know about component hierarchy, and are run in parallel, so one loader won't know about another loader's data. 

Two solutions that would be cool to add to this API

1. Middleware that can run before or after loaders and pass context to all the loaders (I think they're working on this -> [ref](https://stackoverflow.com/a/75449035))
2. Create a new type with a `.wait` method. Each loader instantiated one of these types, as well as being passed every other loader. This way, if you know a specific loader you want to wait for data for, you can. 
	1. This is also definitely a foot gun. If you waited on the same loader promise you are in, you'd be stuck until the promise timeout and would be very hard to debug. This could be solved with linters and compile time errors, but definitely smells and feels circular.




---
# References
