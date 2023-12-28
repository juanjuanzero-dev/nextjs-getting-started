# Next Js Learning

Goal is to get familiar enough with NextJs to build the application that someone asked me to build. So here goes.

```shell
npx create-next-app@latest nextjs-dashboard --use-npm --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example"
```

From the root where this file resides, we create a nextjs app which creates a directory called `nextjs-dashboard`. This also uses the example starter when we provided the `--example` flag.

## Chapter 2

The layout.tsx file is the root level element.

You can use [clsx](https://www.npmjs.com/package/clsx) to conditionally style elements based on a property on a component.

## Chapter 3

Next js has fonts that you can just add in. We added the `fonts.ts` file in app/ui directory so that we can bring in the Inter font, we used fonts in the `page.tsx` file

You can use nexts <Image> component which comes with a few optimizations.

### Chapter 4

### Creating the dashboard routes using the file-system routing

nextjs uses file system routing where folders are used to create nested routes. It follows the directory structure. Recall that we used `page.tsx`, this is a special files that exports a React component. Remember we just played with one recently. This was one that responds to the home route which is `/`.

So here we create a dashboad route by creating a page.tsx file under the dashboard directory (root here being the project folder `nextjs-dashboard`)
```shell
code ./app/dashboard/page.tsx
```

```js
export default function Page() {
    return <p>Dashboad Page</p>
}
```

We did the same for customers and pages 

### creating a nested layout that can be shared between multiple dashboard pages
the `layout.tsx` file is a special file that next.js uses, this layout is shared between multiple pages. 

When we created the layout component under dashbaord, this layout receives as `children` prop, this child can either be a page or another layout. For our case it will be the pages we created under the `app/dashboard/` directory i.e. customers and invoices and the main dashboard page.

There is a technology here called partial rendering. Where the page components would only render when you click into the invoices and customers pages. The dashboard does not render because of partial rendering on the layout. Thats the advantage of the layout component.

There is also the rootLayout under the app directory. This is the most base layout. Anything you add here will be shared across other layouts, where as the one under dashboard is unique to that only.

### Understand what colocation, partial rendering, and the root layout are

# Resources

- https://nextjs.org/learn/dashboard-app/getting-started
