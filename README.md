# hugo-starter

This repository contains a template that uses [Netlify](https://www.netlify.com/), [Hugo](https://gohugo.io/), and the [PaperMod](https://github.com/adityatelange/hugo-PaperMod) Hugo theme. Read the the `README.md` file below for step-by-step instructions to get a personal portfolio website up and running.

## Step 1: Deploy this template

To start using this template, deploy it to [Netlify](https://www.netlify.com/) with the button below.

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/allegheny-college-junior-innovators/hugo-starter)

You will need to create an account if you don't have one, and link your GitHub account.

This button will cause Netlify to authenticate with GitHub and create a new repository based off of this template, and then set up deployment through Netlify's hosting services.

## Step 2: Set your URL

Now that you have your website set up on Netlify, click on the "Deploys" tab and view the most recent deploy -- that is the template itself being built! To visit your new website, look under the "Deploys for ..." header for a link ending in `netlify.app`. You can visit that link and see the base template.

However, that link is not the most useful or memorable web address -- let's change it to something better! In Netlify, navigate to the "Site settings" tab (it is at the very end of the navigation bar at the top). Then, click the "Change site name" button and enter a better url for your site, like your name.

Once you have done that, you can navigate back to the Deploys tab or look at the top of the Site settings for the new link to your website; save that link as you'll want to enter it as the `baseURL` value in a later step, and share it with your network.

## Step 3: Customize your website

Navigate to the "Deploys" tab in Netlify again, and look for the GitHub link under the "Deploys for ..." header. Click that, and you'll be navigated to the repository that Netlify created for you! Now, edit the files in this repository to set the contents of your website. The following values and files should be configured or removed.

> If you're in a hurry, hit `.` when you're on the main repository page on GitHub and a web instance of VSCode will open. You can use this editor to edit files, make commits, and view the README, although you cannot run any terminal commands.

In `config.toml`:

- The `baseURL` key, to match what your chosen URL is on Netlify.
- The `title` key, to configure what your website is titled (and thus what the browser tab is named).
- Entries in the `[params]` table, to configure the `author`, `description`, `keywords`, and various other theme options.
- Entries in the `[params.label]` table, to configure the home label in the top-left corner.
- Entries in the `[params.profileMode]` table, to configure what you'd like to display on the main page.
- Entries in the `[params.profileMode.buttons]` array of tables, to configure what buttons you'd like on the main page. You can also remove the existing entries to have no buttons.
- Entries in the `[params.socialIcons]` array of tables, to configure what social icons and links are on the main page.
- Entries in the `[menu.main]` array of tables, to configure the top navigation links.

In `static/`:

- `profile.png`, to configure the image to show on the main page (or, if you'd like no image, remove the `image`-related keys in the `[params.profileMode]` table in `config.toml`)
- Any other static assets like images, fonts, or other static files and folders that you might want to link, reference, or use in your website. These will be available under the root directory of your website -- so, `profile.png` can be directly linked to with `/profile.png`.

In `contents/`:

- The contents (and existence) of the `blog/` folder, if you'd like to have blog posts on your website.
- The contents of the `projects/` folder -- either edit `_index.md` to show your project details all on one page, or create a project file for each ( use `hugo new --kind project projects/<name-of-project>`), which will be displayed as a card on the projects page.
- Any additional folders and/or files you'd like; each can be linked to by their file path, so `content/test-folder/my-page.md` would be accessed on your website as `/test-folder/my-page`, and you can add links to them in other pages or the top navigation menu.

Experimentation and creativity in organizing and creating content for your website is very important! If you are confused or would like to find out more about the possible configuration options of the PaperMod theme, visit the [demo website](https://adityatelange.github.io/hugo-PaperMod/posts/papermod/papermod-features/), which lists many of the available configuration options not used in this template.

## Alternatives

If the PaperMod theme isn't quite to your liking, you can easily remove it (use `git rm themes/PaperMod`) and use a different theme! There are many to choose from; [themes.gohugo.io](https://themes.gohugo.io/) contains hundreds of options. Below are a few options and the command you could use to add that theme (after removing PaperMod).

- [Gokarna](https://github.com/526avijitgupta/gokarna) - `git submodule add https://github.com/526avijitgupta/gokarna.git themes/gokarna` - [Setup Guide](https://gokarna-hugo.netlify.app/posts/theme-documentation-basics/)
- [Developer Portfolio](https://github.com/samrobbins85/hugo-developer-portfolio) - `git submodule add https://github.com/samrobbins85/hugo-developer-portfolio themes/hugo-developer-portfolio`
- [Highlights](https://github.com/schmanat/hugo-highlights-theme) - `git submodule add https://github.com/schmanat/hugo-highlights-theme.git themes/hugo-highlights-theme`
- [Osprey Delight](https://github.com/kdevo/osprey-delight) - `git submodule add https://github.com/kdevo/osprey-delight.git themes/osprey-delight`

Keep in mind that every theme is different, and you will need to read through the documentation to discover what entries you can add to `config.toml` and what content structure you should have in `content/`.
