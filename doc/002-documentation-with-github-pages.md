# 2 - Documentation with GitHub Pages

Using GitHub Pages you can create Websites for your projects, for example to publish documentation.

The sites are direcly hosted from the GitHub repository.

Just edit, push, and your changes are live!

In this Lab you will add, and publish documentation to the repository you have created in the previous step.

----

### 1 - Create a `docs` folder and content

Go back to the main page of your repository.

Using a **new Codespaces**, or the editor create a new file with some markdown content.


- File: `/docs/index.md`

    ```md

    ## Documentation for my project

    This is an example of documentation

    ### Sample code

    - Sample code:

        ```js
            console.log("Simple code!");
        ```
    ```

- **Commit and push** the changes in `main` branch

---
### 2 - Enable GitHub Pages in your repository

- Go to the repository you have created, and click **Settings**
    
    Select the `main` branch, and the `docs` folder
    
    ![Settings](../images/img-009.png)

- If you scroll down on the settings page, you'll see the **GitHub Pages** section near the bottom. Click the **Choose a theme** button to start the process of creating your site.

    ![launch-theme-chooser](https://docs.github.com/assets/cb-62512/images/help/pages/choose-theme.png)

- Once you've clicked the button, you'll be directed to the Theme Chooser. You'll see several theme options in a carousel across the top of the page. Click on the images to preview the themes. Once you've selected one, click **Select theme** on the right to move on. It's easy to change your theme later, so if you're not sure, just choose one for now.

    ![theme-chooser](https://docs.github.com/assets/cb-180181/images/help/pages/select-theme.png)


- Click on the link at the top of the page to see your page

- You can change the Them and refresh your page, to see the changes (force refresh)

    When you change the theme a new file is added: `/docs/_config.yml`


---
### 3 Making changes

- Using Codespaces or other methods modify the `/docs/_config.yml` content

- You can also change the title and description, edit the `/docs/_config.yml` file with the following content:

    ```yml
    theme: jekyll-theme-minimal
    title: "<YOUR NNAME> - project homepage"
    description: "Great documentation about my project!"
    ```

- When you're done, click **Commit changes** and your updates will go live in just a few seconds!
    
    
## Conclusion Lab 2

In this lab you have learned, how to:

- 👏 Use Markdown to create content
- 👏 Create a site for your project using GitHub Pages
- 👏 Configure GitHub Pages


----

**Additional GitHub Content & Training:**

- [GitHub Pages](https://pages.github.com/)
- [GitHub Pages Documentation](https://docs.github.com/en/enterprise-cloud@latest/pages)
- [Personal Site with GitHub Pages](https://docs.github.com/en/enterprise-cloud@latest/pages/quickstart)
- [GitHub Pages](https://lab.github.com/githubtraining/github-pages)


----

Next : 
  - **[Create your community](003-create-community-with-github-discussion.md)**
