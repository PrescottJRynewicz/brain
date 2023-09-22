---
Created On: 2023-08-08, 15:15
Unique ID: 202308081515
---
**Status:** #thought 

**Tags:**  [[Next.JS]] [[Software Engineering]] #SoftwareCards 
# Next.JS App Routing

#### Does the `app` directory or `page` directory take priority?
? 
The `app` router takes priority.


#### What is the default type of components in the next.js `app` directory?
?
Server components. But you can still use client components. 
<!--SR:!2023-10-13,24,170-->

#### How does Next.js App Routing Define Routes
?
With the folder structure. Special file names are used to describe specific react conventions, and these special files are nested within each other. 
![[Pasted image 20230808152541.png]]
![[Pasted image 20230808152555.png]]
<!--SR:!2023-10-04,27,210-->


#### What is the difference between a Page and a Layout in Next.js? 
?
A page is a unique URL that is displayed on a website, when a Layout is shared between multiple pages. 
A Layout component must take in React Children.
A Layout and a Page can be used together - **the Layout will wrap the Page.**
```typescript
export default function DashboardLayout({
  children, // will be a page or nested layout
}: {
  children: React.ReactNode
}) {
  return (
    <section>
      {/* Include shared UI here e.g. a header or sidebar */}
      <nav></nav>
 
      {children}
    </section>
  )
}
```
<!--SR:!2023-09-25,26,223-->


 


---
# References
[Next.JS Routing](https://nextjs.org/docs/app/building-your-application/routing)

