---
title: "Lab 10 Problem 3"
date: 2024-12-05
draft: false
---

# How I Built This Page

## Building the Page

Using the default Vim text editor on my machine, I made this page as a **Markdown** (.md) file, which is what the **Hugo framework** uses as its default content format. The process of making a site using Hugo involves writing content in Markdown and using Hugo to process it.

1. **Installation**: I installed Hugo using the package manager for my system (e.g., `sudo apt install hugo` on Linux Mint/Ubuntu).
2. **Theme Setup**: Initially, I used the **Ananke** theme, but switched it later due to compatibility issues.
3. **Page Creation**: I created the page using `hugo new posts/lab10c.md` and Hugo processed it into a static HTML page.

---

## Challenges and Solutions

### 1. **Hugo Version and Theme Compatibility**

- **Challenge**: My first issue was with the **Hugo version** and **theme compatibility**. Initially, I opted to use the **Ananke** theme, which caused an error related to a missing function (`css`) when I attempted to run Hugo. This was the error: `add site dependencies: load resources: loading templates: "/home/aidan/Desktop/mysite/themes/ananke/layouts/partials/func/style/GetMainCSS.html:54:1": parse failed: template: partials/func/style/GetMainCSS.html:54: function "css" not defined`
  
- **Solution**: I actually couldn't figure out how to resolve that error, so I just switched to a different theme, **Hello Friend**, which was compatible with my Hugo version.

---

### 2. **TOML Configuration File Error**

- **Challenge**: After downloading the **Hello Friend** theme, Hugo could not process the `config.toml` file due to a duplicate `theme` key, leading to the error: `"unmarshal failed: toml: key theme is already defined"`

- **Solution**: The issue occurred because I ran a command that automatically added the `theme` key without checking if one already existed in the `config.toml` file. To fix this, I manually edited the file and removed the duplicate `theme` key, so that there was just one theme key for the new theme I decided to use.

---

## Uploading to GitHub and Netlify
Lastly, to deploy the site online, I used **Netlify**:
 - I initialized a Git repo in my project folder, and pushed to my GitHub.
 - Then, I connected the GitHub repository to **Netlify**, which automatically detected the Hugo framework and deployed the site to a live URL.

---
