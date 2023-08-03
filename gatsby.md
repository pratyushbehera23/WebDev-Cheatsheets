# GatsbyJs

Gatsby - is a Static Site Generator
produce static HTML files that we load up on to a server

Other sites: Vist a website - it query a database or do some programming on the server in order to serve you web pages

Using Gatsby it will have all of the stuff already pre-configued ahead of time and just serve the web pages.

Here static site dont mean not interactive, we can load JS into the HTML files that Gatsby serves as well as make API calls, do interactions and build incredibly rich and immersive sites even though they are static in nature of just being HTML files served up without server-side programming language running.

So, Gatsby is a tool that help us build the final product ie. Gatsby static site.

In order to do this generation Gatsby is going to use NodeJs.
NodeJs will be running in a development environment on your computer, however the final site wont need NodeJs on the server.

It will use the GraphQL querying language to get data from anywhere.

GraphQL - is an evolution of how to make API calls simpler and more efficient.

We can get data into a Gatsby site from anywhere we could use Markdown files, we can access databases, we could hook into common CMS like WordPress and other headless CMS, as well as even a CSV file.

Gatsby will use React for the templates and CSS for the styling.

So, GraphQL will pull in our data, React will take care of what the template should look like and the styling is what CSS. Finally everything will be exported out into that final super fast static Gatsby site.
Gatsby is build with a plug-in architecture

Why use? Speed Security DevExperience

Static site - HTML - seo ready | slow as each page is requested from server & hard to maintain
Single Page Application (SPA) - React / Vue - fast as react takes over & easy to maintain components | not seo friendly
Server Side Rendering (SSR) - Node+Express / php - good seo & easy to  maintain templates | slow as generated from server
Static Site Generator (SSG) - Gatsby / Next / Nuxt - seo  fast  easy to maintain

## Start

```sh
npm install --global gatsby-cli
gatsby new app-name
cd app-name
gatsby develop
```
