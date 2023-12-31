https://docs.astro.build/en/tutorial/1-setup/2/

https://github.com/withastro/blog-tutorial-demo/tree/complete

https://github.com/simorgh10/astro-tutorial/

# Setup

> npm create astro@latest

* Confirm y to install create-astro

* When the prompt asks, “Where would you like to create your new project?” type in the name of a folder to create a new directory for your project, e.g. ./astro-tutorial

* You will see a short list of starter templates to choose from. Use the arrow keys (up and down) to navigate to the “Empty” template, and then press return (enter) to submit your choice.

* When the prompt asks, “Would you like to install dependencies?” type y.

* When the prompt asks you if you plan on writing TypeScript, type n.

* When the prompt asks, “Would you like to initialize a new git repository?” type y.

* Install the Astro language support extension

*  Ctrl + J to toggle terminal

# Run

> npm run dev

# Write your first line of Astro

* modify src/pages/index.astro

# Store your repository online

* Log in to GitHub.com in a browser and click the + in the upper right of the screen to make a new repository.

* Choose a name for your repository. This does not have to be the same name as your project folder.

* You will be presented with options, but you do not need to change any of the defaults. Scroll down and click the button to Create Repository.

* You will be presented with various setup next steps, but you won’t need to use any of them. Make a note of the URL of your repository. You can now exit this page without doing anything.

https://github.com/simorgh10/astro-tutorial

* Click the ••• “3 dots” menu above the commit message and choose Remote > Add Remote. Select Add remote from GitHub. If necessary, follow any authentication steps then return to VS Code and repeat this action. You should see a list of all your repositories on GitHub. Choose the one you created for this project. If you don’t see your project, paste in its GitHub URL directly. You may also be asked to give this repository a local name. You can select any name you like.

* At the top of the menu pane, there will be a place to enter a commit message (description of your file changes). Type in initial commit and press the Commit button to commit these changes.

* You may see a message telling you that you have no “staged” commits, and asking you if you want to stage them. Click Always and continue.

* Lastly, the list of changed files should be replaced with a Publish button. Click this to send your committed changes to GitHub.

* or 

> git remote add origin https://github.com/simorgh10/astro-tutorial.git

> git push --set-upstream origin master


# Deploy your site to the web

* https://app.netlify.com/teams/simorgh10/overview

* Click Add new site > Import an existing project.

* You will be asked to connect to a Git provider. Choose GitHub and follow the steps onscreen to authenticate your GitHub account. Then, choose your Astro project’s GitHub repository from the list provided.

* At the final step, Netlify will show you your app’s site settings. The defaults should be correct for your Astro project, so you can scroll down and click Deploy site.

* You can change your project name to something more memorable, and this will automatically update your URL.

https://golden-pie-2114d9.netlify.app/

* Domain management > Production domains > Options > Edit site name : https://astro-tutorial-2114d9.netlify.app/

# Create your first Astro page

* navigate to the folder src/pages/ where you will see the existing file index.astro, create a new file named about.astro.
* Copy, or retype the contents of index.astro into your new about.astro file.
* Under the File menu in VS Code, enable “Auto Save” and you should no longer need to save any files manually.
* Add /about to the end of your website preview’s URL in the address bar and check that you can see a page load there. (e.g. http://localhost:4321/about)

* To make it easier to preview all your pages, add HTML page navigation links before your <h1> at the top of both of your pages (index.astro and about.astro):

src/pages/about.astro

* Unlike many frameworks, Astro uses standard HTML <a> elements to navigate between pages (also called routes), with traditional page refreshes.

* Add a third page blog.astro

# Write your first Markdown blog post

* Create a new directory at src/pages/posts/.
* Add a new (empty) file post-1.md inside your new /posts/ folder.
* Look for this page in your browser preview by adding /posts/post-1 to the end of your existing preview URL. (e.g. http://localhost:4321/posts/post-1)
* Change the browser preview URL to view /posts/post-2 instead. (This is a page you have not yet created.)
* Note the different output when previewing an “empty” page, and one that doesn’t exist. This will help you troubleshoot in the future.

* Copy or type the following code into post-1.md https://docs.astro.build/en/tutorial/2-pages/2/

* Check your browser preview again at http://localhost:4321/posts/post-1. You should now see content on this page. It may not yet be properly formatted, but don’t worry, you will update this later in the tutorial!

* Use your browser’s Dev Tools to inspect this page. Notice that although you have not typed any HTML elements, your Markdown has been converted to HTML. You can see elements such as headings, paragraphs, and list items.

* The information at the top of the file, inside the code fences, is called frontmatter. This data—including tags and a post image—is information about your post that Astro can use. It does not appear on the page automatically, but you will access it later in the tutorial to enhance your site.

* Link to your first post with an anchor tag in src/pages/blog.astro 

* Now, add two more files in src/pages/posts/: post-2.md and post-3.md. Here is some sample code you can copy and paste into your files, or, you can create your own!

* Check your browser preview and make sure that: All your links for Post 1, Post 2, and Post 3 lead to a working page on your site. 

# Add dynamic content about you

* Define and use a variable. Add the following line of JavaScript in the frontmatter script in about.astro, between the code fences: https://docs.astro.build/en/tutorial/2-pages/3/

* Replace both the static “Astro” title and “About Me” heading in your HTML with the dynamic variable {pageTitle}.

* Add the following JavaScript to your frontmatter, between the code fences:https://docs.astro.build/en/tutorial/2-pages/3/

* Add the following lines to your frontmatter script to define variables: https://docs.astro.build/en/tutorial/2-pages/3/

* Astro’s templating syntax is similar to JSX syntax. If you’re ever wondering how to use your script in your HTML, then searching for how it is done in JSX is probably a good starting point!

# Style your About page

* Copy the following code and paste it into src/pages/about.astro https://docs.astro.build/en/tutorial/2-pages/4/
* Add the class name skill to the generated <li> elements on your About page, so you can style them. Your code should now look like this:

* The Astro <style> tag can also reference any variables from your frontmatter script using the define:vars={ {...} } directive. You can define variables within your code fence, then use them as CSS variables in your style tag.

* Define a skillColor variable by adding it to the frontmatter script of src/pages/about.astro

* Update your existing <style> tag below to first define, then use this skillColor variable inside double curly braces.

# Add site⁠-⁠wide styling

* Add a global stylesheet
* in this tutorial, you will create and import a global.css file into each of your pages.
* Create a new file at the location src/styles/global.css https://docs.astro.build/en/tutorial/2-pages/5/
* In about.astro, add the following import statement to your frontmatte
* When conflicting styles are defined both globally and in a page’s local <style> tag, the local styles should overwrite any global styles. (But, there can be other factors involved, so always visually inspect your site to make sure your styles are properly applied!)

# Make a reusable Navigation component
* To hold .astro files that will generate HTML but that will not become new pages on your website, you will need a new folder in your project:src/components/
* Create a new file: src/components/Navigation.astro https://docs.astro.build/en/tutorial/3-components/1/. Copy your links to navigate between pages from the top of any page and paste them into your new file, Navigation.astro
* If there is nothing in the frontmatter of your .astro file, you don’t have to write the code fences. You can always add them back in when you need them.

* Go back to index.astro and import your new component inside the code fence:

# Create a social media footer
* Create a new file at the location src/components/Footer.astro
* https://docs.astro.build/en/tutorial/3-components/2/

* Since you might have multiple online accounts you can link to, you can make a single, reusable component and display it multiple times. Each time, you will pass it different properties (props) to use: the online platform and your username there.

* Create a new file at the location src/components/Social.astro https://docs.astro.build/en/tutorial/3-components/2/
* Change the code in src/components/Footer.astro to import, then use this new component three times, passing different component attributes as props each time:


* Customize the appearance of your links by adding a <style> tag to src/components/Social.astro.

* Add a <style> tag to src/components/Footer.astro to improve the layout of its contents.

# Build it yourself ⁠-⁠ Header

* Create a new Header component. Import and use your existing Navigation.astro component inside a <nav> element which is inside a <header> element.

* On each page, replace your existing <Navigation/> component with your new header.

* Check your browser preview and verify that your header is displayed on every page. It won’t look different yet, but if you inspect your preview using dev tools, you will see that you now have elements like <header> and <nav> around your navigation links.

* Update Navigation.astro with the CSS class to control your navigation links. Wrap the existing navigation links in a <div> with the class nav-links.

* Copy the CSS styles below into global.css. These styles: https://docs.astro.build/en/tutorial/3-components/3/
  + Style and position the navigation links for mobile
  + Include an expanded class that can be toggled to display or hide the links on mobile
  + Use a @media query to define different styles for larger screen sizes

* MOBILE-FIRST DESIGN: Start by defining what should happen on small screen sizes first! Smaller screen sizes require simpler layouts. Then, adjust your styles to accommodate larger devices. If you design the complicated case first, then you have to work to try to make it simple again.

* CSS PS: https://developer.mozilla.org/en-US/docs/Web/CSS/unset The unset CSS keyword resets a property to its inherited value if the property naturally inherits from its parent, and to its initial value if not.

* Resize your window and look for different styles being applied at different screen widths. Your header is now responsive to screen size through the use of @media queries.

# Send your first script to the browser

* Let’s add a hamburger menu to open and close your links on mobile screen sizes, requiring some client-side interactivity!

* Create a file named Hamburger.astro in src/components/ https://docs.astro.build/en/tutorial/3-components/4/

* This will represent your 3-line “hamburger” menu to open and close your navigation links on mobile. (You will add the new CSS styles to global.css later.)

* Place this new <Hamburger /> component just before your <Navigation /> component in Header.astro.

* Add the following styles for your Hamburger component: https://docs.astro.build/en/tutorial/3-components/4/

* Your header is not yet interactive because it can’t respond to user input, like clicking on the hamburger menu to show or hide the navigation links.

* Add the following <script> tag to index.astro, just before the closing </body> tag.

* nstead of writing your JavaScript directly on each page, you can move the contents of your <script> tag into its own .js file in your project.

* Create src/scripts/menu.js

# Build your first layout

* Create a new file at the location src/layouts/BaseLayout.astro. (You will need to create a new layouts folder first.)

* Replace the code at src/pages/index.astro

* Add a <slot /> element to src/layouts/BaseLayout.astro just above the footer component, then check the browser preview of your Home page and notice what really did change this time!

* The <slot /> allows you to inject (or “slot in”) child content written between opening and closing <Component></Component> tags to any Component.astro file.

* Pass the page title to your layout component from index.astro using a component attribute:

* Change the script of your BaseLayout.astro layout component to receive a page title via Astro.props instead of defining it as a constant.

# Create and pass data to a custom blog layout

* When you include the layout frontmatter property in an .md file, all of your frontmatter YAML values are available to the layout file.

* Create a new file at src/layouts/MarkdownPostLayout.astro

* Add the following frontmatter property in post-1.md

* When using layouts, you now have the option of including elements, like a page title, in the Markdown content or in the layout. Remember to visually inspect your page preview and make any adjustments necessary to avoid duplicated elements.

# Combine layouts to get the best of both worlds

* In src/layouts/MarkdownPostLayout.astro, import BaseLayout.astro and use it to wrap the entire template content. Don’t forget to pass the pageTitle prop:

# Create a blog post archive

* Access data from all your posts at once using Astro.glob()
* Display a dynamically generated list of posts on your Blog page
* Refactor to use a <BlogPost /> component for each list item

* To generate the entire list of posts dynamically, using the post titles and URLs, replace your individual <li>
* Add a new blog post by creating a new post-4.md file in src/pages/posts/ and adding some Markdown content. Be sure to include at least the frontmatter properties used below.

* create BlogPost component

# Generate tag pages

* You can create entire sets of pages dynamically using .astro files that export a getStaticPaths() function.

* Create a new file at src/pages/tags/[tag].astro.

* The getStaticPaths function returns an array of page routes, and all of the pages at those routes will use the same template defined in the file.

* Make sure that every blog post contains at least one tag, written as an array, e.g. tags: ["blogging"].

* Add the following props to your getStaticPaths() function in order to make data from all your blog posts available to each page route.

* Filter your list of posts to only include posts that contain the page’s own tag.

* If you need information to construct the page routes, write it inside getStaticPaths().

* To receive information in the HTML template of a page route, write it outside getStaticPaths().

* Your tag pages are now defined statically in [tag].astro. If you add a new tag to a blog post, you will also have to revisit this page and update your page routes.

* The following example shows how to replace your code on this page with code that will automatically look for, and generate pages for, each tag used on your blog pages.

* Create an array of all your existing tags

* Replace the return value of the getStaticPaths function

# Build a tag index page

* Add a new page using the /pages/folder/index.astro routing pattern
* Display a list of all your unique tags, linking to each tag page
* Update your site with navigation links to this new Tags page

* Create a new file index.astro in the directory src/pages/tags/.
* Create a minimal page at src/pages/tags/index.astro that uses your layout. You have done this before!

* Create an array of tags
* In src/pages/tags/index.astro, add the line of code to the frontmatter script that will give your page access to the data from every .md blog post file.

* Add this page to your navigation

* But, you still need to make these pages discoverable from other pages on your website.

# Add an RSS feed

> npm install @astrojs/rss

* Create a new file in src/pages/ called rss.xml.js https://docs.astro.build/en/tutorial/5-astro-api/4/
* Add the site property to the Astro config with your site’s own unique Netlify URL. https://astro-tutorial-2114d9.netlify.app/
* This rss.xml document is only created when your site is built, so you won’t be able to see this page in your browser during development
* Quit the dev server and run the following commands to first, build your site locally and then, view a preview of your build:

> npm run build

> npm run preview

* Visit http://localhost:4321/rss.xml

* Download a feed reader, or sign up for an online feed reader service and subscribe to your site by adding your own Netlify URL. You can also share this link with others so they can subscribe to your posts, and be notified when a new one is published.

# Build your first Astro island

* Add Preact to your Astro project

> npx astro add preact

* Include Astro islands (Preact .jsx components) on your home page

* Use client: directives to make islands interactive

* Create a new file in src/components/ named Greeting.jsx

* Import and use this component on your Home page index.astro.

* Check the preview in your browser: you should see a random greeting, but the button won’t work!

* Add a second <Greeting /> component with the client:load directive.

* The second button works because the client:load directive tells Astro to send and rerun its JavaScript on the client when the page loads, making the component interactive. This is called a hydrated component.

* Once the difference is clear, remove the non-hydrated Greeting component.

* There are other client: directives to explore. Each sends the JavaScript to the client at a different time. client:visible, for example, will only send the component’s JavaScript when it is visible on the page.

https://docs.astro.build/en/tutorial/6-islands/1/

* The component with the client:load directive will rerender after the page is loaded, and any interactive elements that it has will work.

# Back on dry land. Take your blog from day to night, no island required!

* Let’s build a clickable icon to let your users toggle between light or dark mode using another <script> tag for interactivity… with no framework JavaScript sent to the browser.

* Build an interactive theme toggle with only JavaScript and CSS

* Send as little JavaScript to the browser as possible!

* Create a new file at src/components/ThemeIcon.astro https://docs.astro.build/en/tutorial/6-islands/2/

https://stackoverflow.com/questions/43613619/what-does-global-colon-global-do

* The :global operator is used in CSS Modules. Modular CSS uses a CSS Modules compiler to scope CSS styles within their respective modules (e.g., React component).

* :global switches to global scope for the current selector resp. identifier. :global(.xxx) resp. @keyframes :global(xxx) declares the stuff in parenthesis in the global scope.

* Add the icon to Header.astro so that it will be displayed on all pages. Don’t forget to import the component.

* o add interactivity to an Astro component, you can use a <script> tag. This script can check and set the current theme from localStorage and toggle the theme when the icon is clicked. Add the following <script> tag in src/components/ThemeIcon.astro after your <style> tag: https://docs.astro.build/en/tutorial/6-islands/2/

* You need to write the script inside <script is:inline></script> if you want to use things like window or document. This way Astro won't touch your JS and include it directly on the HTML.

