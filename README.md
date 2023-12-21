# Next Js Training
Goal is to get familiar enough with NextJs to build the application that someone asked me to build. So here goes.

```shell
npx create-next-app@latest nextjs-dashboard --use-npm --example "https://github.com/vercel/next-learn/tree/main/dashboard/starter-example"
```

From the root where this file resides, we create a nextjs app which creates a directory called `nextjs-dashboard`. This also uses the example starter when we provided the `--example` flag.

## Chapter 2

The layout.tsx file is the root level element.

You can use [clsx](https://www.npmjs.com/package/clsx) to conditionally style elements based on a property on a component.

# Chapter 3
Next js has fonts that you can just add in. We added the `fonts.ts` file in app/ui directory so that we can bring in the Inter font, we used fonts in the `page.tsx` file

You can use nexts <Image> component which comes with a few optimizations.


# Resources 
- https://nextjs.org/learn/dashboard-app/getting-startedF