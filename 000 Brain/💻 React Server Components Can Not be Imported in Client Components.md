---
Created On: 2023-08-08, 15:00
Unique ID: 202308081500
---
**Status:** #thought 

**Tags:**  #SoftwareCards [[React.js]] [[Software Engineering]] 

# React Server Components Can Not be Imported into Client Components

### Can React Server Components Be Used in Client Components? 
?
They can, but they need to be passed to the client component through props (as children). 
You cannot import a server component in the client component and have it rendered. 
##### **Bad**
```typescript
'use client'
 
// This pattern will **not** work!
// You cannot import a Server Component into a Client Component.
import ExampleServerComponent from './example-server-component'
 
export default function ExampleClientComponent({
  children,
}: {
  children: React.ReactNode
}) {
  const [count, setCount] = useState(0)
 
  return (
    <>
      <button onClick={() => setCount(count + 1)}>{count}</button>
 
      <ExampleServerComponent />
    </>
  )
}
```
##### **Good**
```typescript
'use client'
 
import { useState } from 'react'
 
export default function ExampleClientComponent({
  children,
}: {
  children: React.ReactNode
}) {
  const [count, setCount] = useState(0)
 
  return (
    <>
      <button onClick={() => setCount(count + 1)}>{count}</button>
 
      {children}
    </>
  )
}
```
<!--SR:!2023-08-22,7,230-->





---
# References
[Next.js ref](https://nextjs.org/docs/getting-started/react-essentials#nesting-server-components-inside-client-components)

