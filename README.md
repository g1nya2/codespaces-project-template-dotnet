[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://github.com/codespaces/new?hide_repo_select=true&ref=main&repo=education/codespaces-project-template-dotnet) 

# .NET (Blazor) Portfolio Site with GitHub Codespaces

_Create, customize and deploy your own portfolio website in minutes._ ✨

In this template repository we have the development environment and base set and ready to go. So that you can immediately launch the Codespaces to customize with no setup.

- **Who is this for?** __Anyone__ looking to create a portfolio site, learn web development, or test out Codespaces.
- **How much experience do you need?** __Zero__. You decide how much you want to customize based on your experience, and time available.
- **Tools needed:** _None_. No need to install anything! All you need is a web browser.
- **Prerequisites:** _None_. This template includes your development environment and deployable web app for you to create your own site.

## About this portfolio template

In this "choose your own adventure" template portfolio, we have a [Blazor](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor?WT.mc_id=dotnet-82024-juyoo) based web application ready for you to easily customize and deploy using only your web browser.  

![Blazor WebAssembly profile web application](./images/blazorwasm-portfolio-site.gif "Blazor WebAssembly profile web application")

### Quick Start

1. Click the **Use this Template** button

   [![Use this Template](/images/template-button.svg)](https://github.com/education/codespaces-project-template-dotnet/generate)

1. Select the repository owner (e.g. your GitHub account)
1. Enter a unique name for your new repository
1. Click the **Code** button
1. Click **Create Codespace on main** button
1. [Customize your portfolio site](#-customize-your-site-in-4-steps)
1. [Deploy your site](#-deploy-your-web-application)

<details>
   <summary><b>🎥 To learn more about Codespaces, watch our video tutorial series</b></summary>

   [![Codespaces Tutorial](https://img.youtube.com/vi/ozuDPmcC1io/0.jpg)](https://aka.ms/CodespacesVideoTutorial "Codespaces Tutorial")
</details>

<br />

## 🗃️ .NET (Blazor) Portfolio template

This repo is a GitHub template to build a .NET personal portfolio frontend web application using the Blazor WebAssembly framework. The goal is to give you a template to you can immediately utilize to create your own website through Codespaces.

The repo contains the following:

- `/.devcontainer`
  - `.devcontainer/Dockerfile`: Configuration file used by Codespaces to determine operating system and other details.
  - `.devcontainer/devcontainer.json`: Configuration file used by Codespaces to configure Visual Studio Code settings, such as the enabling of additional extensions.
  - `.devcontainer/on-create.sh`: Configuration file used by Codespaces to install additional tools, such as PowerShell.
- `/src`: Blazor WebAssembly project to build your portfolio site.
- `.editorconfig`: Settings for [EditorConfig](https://editorconfig.org/) that helps maintain consistent coding styles in Codespaces.
- `global.json`: Settings for the Blazor WebAssembly app to avoid using pre-released .NET version.
- `swa-cli.config.json`: Settings for [Azure SWA CLI](https://azure.github.io/static-web-apps-cli/) to run the Blazor WebAssembly app on your Codespaces.
- `MyPortfolio.sln`: The solution file that contains the Blazor WebAssembly application project.

<br />

## 🚀 Getting started

This portfolio site project is filled with sample data so that you can immediately open Codespaces, see it running, and deploy at any point.

Your development environment is all set for you to start. Based on our [.NET Codespaces Template](https://github.com/education/codespaces-teaching-template-dotnet), here is what's already setup and ready for you to use:

- Simple [Blazor WebAssembly](https://dotnet.microsoft.com/apps/aspnet/web-apps/blazor?WT.mc_id=dotnet-82024-juyoo) application with components for each section of the portfolio site
- [SWA CLI](https://azure.github.io/static-web-apps-cli/) in place to build your site when deploying
- Code linting and formatting using [EditorConfig](https://editorconfig.org/) for code consistency.

### Create your portfolio

1. Create a repository from this template. Use this [create repo link](https://github.com/education/codespaces-teaching-template-dotnet/generate). Select the repository owner, provide a name, a description if you'd like and if you'd like the new repository to be public or private.
1. Navigate to the main page of the newly created repository.
1. Under the repository name, use the Code drop-down menu, and in the Codespaces tab, select "Create codespace on main".

    <img src="./images/new-codespace-button.png" alt="Create codespace" style="width:270px;"/>

1. Wait as GitHub initializes the Codespaces.

    <img src="./images/codespaces-initializing.png" alt="Codespaces initializing" style="width: 600px;"/>

1. When complete you will see your Codespaces load with a terminal section at the bottom. Here you will see `dotnet restore && dotnet build` executing. When complete you will return to the terminal prompt where you can run the web application by executing: `swa start`.

   When the web application is started you will see a prompt telling you it started successfully on port 4280, and you can open that site within your browser:

   <img src="./images/app-running-in-codespaces.png" alt="Web application started on port 4280" style="width: 340px;"/>

<br />

## ✨ 사이트를 4단계에 걸쳐 개인 맞춤 설정하기

이 프로젝트는 쉽게 개인 맞춤 설정할 수 있도록 제작되었습니다. 사이트의 각 부분은 별도의 컴포넌트이며, 당신의 정보는 한 곳에만 설정되어야 합니다. 이는 업데이트를 쉽게 하기 위한 것일 뿐만 아니라, 블레이저 컴포넌트에 값이 전달되는 방식을 확인할 수 있습니다.

각 단계별로 코드스페이스에서 프로젝트를 연 다음 코드스페이스 내에서 변경하고, 변경 사항을 커밋할 수 있습니다.

> 자세한 코드스페이스 소스 제어 방법은 [코드스페이스에서 소스 제어 사용](https://docs.github.com/codespaces/developing-in-codespaces/using-source-control-in-your-codespace) 을 참조하시면 됩니다.

### 1️⃣ 세부 정보 및 소셜 미디어 계정 추가하기

`/src/BlazorApp/wwwroot/sample-data/siteproperties.json`을 엽니다. 이는 이름, 제목, 이메일 및 소셜 미디어 계정을 개인 맞춤 설정하는데 필요한 키-값 쌍을 담고 있는 JSON 객체 입니다.

```jsonc
{
  "name": "Alexandrie Grenier",
  "title": "Web Designer & Content Creator",
  "email": "alex@example.com",
  "gitHub": "microsoft",
  "devDotTo": null,
  "instagram": "microsoft",
  "linkedIn": "satyanadella",
  "medium": "",
  "twitter": "microsoft",
  "youTube": "microsoft",
};
```

사이트 맨 위에 표시할 이름과 제목을 업데이트합니다.

_선택적인 값들_ 은 이메일 주소와 소셜 계정입니다. 이는 `Footer` 컴포넌트에 사용됩니다. 리스트에 어떤 항목도 포함하지 않거나 빈 문자열 ("")로 설정하면 아이콘과 링크가 표시되지 않습니다.

### 2️⃣ 이미지 업데이트하기

이 포트폴리오 사이트에는 3가지 이미지가 포함되어있습니다 : 상단 배경, "About me" 배경 및 포트폴리오 부분(책상그림) 등. These can be any **landscape** sized images of your choosing from your own collection, or found that have a license allowing you to use without attribution.

A couple possible sites to find photos are [Pixabay](https://pixabay.com/) and [Unsplash](https://unsplash.com). Photos, illustrations, vectors, your choice! When you find your images, save each one to `/src/BlazorApp/wwwroot/images` with a short, meaningful file name.

Open `/src/BlazorApp/wwwroot/sample-data/heroimages.json` and update images with your preferred ones, as well as the alt text for each image:

```jsonc
[
  {
    // Home component
    // section at top of the page, main image you will see when site loads (woman standing by server wall in sample)
    "name": "home",
    "src": "images/server-wall.jpg",
    "alt": "woman holding laptop standing by server room with glass wall"
  },
  {
    // About me component
    // background behind the detailed "about me" section (abstract mosaic in sample)
    "name": "about",
    "src": "images/mosaic.svg",
    "alt": "purple and blue abstract background"
  },
  {
    // Portfolio component
    // image highted in left hand side of section (design desk photo in sample)
    "name": "portfolio",
    "src": "images/design-desk.jpeg",
    "alt": "desktop with books and laptop"
  }
]
```

### 3️⃣ Add your "about me"

The about section helps to give people a bit more information about your skills and passions. Open `/src/BlazorApp/wwwroot/sample-data/aboutme.json` and update those 3 properties:

* `description`: short sentence or two describing yourself, career goal, and/or passions
* `skillsList`: an [array](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array) of your skills to list on the site, can be as many or little as you wish
* `detailOrQuote`: longer block for you to add more detail about yourself, or even a quote you like

### 4️⃣ Add items you've worked on and detail text

This section to update is portfolio, where you highlight items you've worked on. These would be articles, videos, logo designs, GitHub projects, anything that highlights you!

Open `/src/BlazorApp/wwwroot/sample-data/projects.json` that is a JSON array. Each item you want to highlight needs: title, description, and URL.

The sample design has 4, but the number you include is up to you.

```jsonc
[
  {
    "title": "10 Things To Know About Azure Static Web Apps 🎉",
    "description": "Collaboration to create a beginner friendly article to help explain Azure Static Web Apps and tooling to get started.",
    "url": "https://dev.to/azure/10-things-to-know-about-azure-static-web-apps-3n4i"
  },
  {
    "title": "Web Development for Beginners",
    "description": "Contributed sketch note imagery to accompany each lesson. These help provide visual representation of what is being taught.",
    "url": "https://github.com/microsoft/web-dev-for-beginners"
  },
  {
    "title": "My Resume Site",
    "description": "Created from Microsoft's resume workshop and deployed to GitHub pages. Includes my experience and design abilities.",
    "url": "https://github.com/microsoft/workshop-library/tree/main/full/build-resume-website"
  },
  {
    "title": "GitHub Codespaces and github.dev",
    "description": "Video interview to explain when to use GitHub.dev versus GitHub Codespaces, and how best to use each tool.",
    "url": "https://www.youtube.com/watch?v=c3hHhRME_XI"
  }
]
```

<br/>

## 🏃 Deploy your web application

Project includes the setup needed for you to deploy **free** to both [Azure Static Web Apps](https://azure.microsoft.com/products/app-service/static/?WT.mc_id=dotnet-82024-juyoo) and [GitHub Pages](https://pages.github.com/)</a>.

### Azure Static Web Apps

[Azure Static Web Apps](https://azure.microsoft.com/products/app-service/static/?WT.mc_id=dotnet-82024-juyoo) is Microsoft's hosting solution for static sites (or sites that are rendered in the user's browser, not on a server) through Azure. This service provides additional opportunities to expand your site through Azure Functions, authentication, staging versions and more.

You'll need both Azure and GitHub accounts to deploy your web application. If you don't yet have an Azure account you can create it from within during the deploy process, or from below links:

* [Create a (no Credit Card required) Azure For Students account](https://azure.microsoft.com/free/students/?WT.mc_id=dotnet-82024-juyoo)
* [Create a new Azure account](https://azure.microsoft.com/free/?WT.mc_id=dotnet-82024-juyoo)

With your project open in Codespaces:

1. Click Azure icon in the left sidebar. Log in if you are not already, and if new to Azure, follow the prompts to create your account.
1. From Azure menu click "➕" sign and then choose "Create Static Web App".

   <img src="./images/deploy-to-azure.png" alt="Create Static Web App" style="width: 300px;" />

1. If you are not logged into GitHub you will be prompted to log in. If you have any pending file changes you will then be prompted to commit those changes.
1. Set you application information when prompted:
    1. **Name for Static Web App**: enter the name for the Static Web App. Default to your GitHub repository name.
    1. **Region**: pick the one closest to your region
    1. **Project structure**: select "Blazor"
    1. **Location of application code**: enter `/src/BlazorApp`
    1. **Output location**: enter `wwwroot`
1. When complete you will see notification at the bottom of your screen, and a new GitHub Action workflow will be added to your project. If you click "Open Action in GitHub" you will see the action that was created for you, and it is currently running.

> 🤩 **Bonus**: [Setup a custom domain for your Azure Static Web App](https://learn.microsoft.com/shows/azure-tips-and-tricks-static-web-apps/how-to-set-up-a-custom-domain-name-in-azure-static-web-apps-10-of-16--azure-tips-and-tricks-static-w/?WT.mc_id=dotnet-82024-juyoo)

### GitHub Pages

[GitHub Pages](https://pages.github.com/) allows you to host websites directly from your GitHub repository. This project is already set up for you to get your portfolio deployed to GitHub pages with minimal steps.

On your GitHub repository:

1. Go to the "Settings" tab and navigate to the "Pages" menu.
1. Under the _Build and deployment_ section, select the source to **GitHub Actions**.

    <img src="./images/deploy-to-ghpages-01.png" alt="Choose GitHub Actions for deployment to GitHub Pages" style="width: 600px;" />

1. Ensure your GitHub Pages visibility to **Public**.
1. Run a GitHub Action workflow by pushing code or manually invoke it.

    <img src="./images/deploy-to-ghpages-02.png" alt="Invoke GitHub Actions" style="width: 600px;" />

1. Visit your GitHub Pages.

    <img src="./images/deploy-to-ghpages-03.png" alt="Visit GitHub Pages" style="width: 600px;" />

> 🤩 **Bonus**: [Setup a custom domain for your GitHub pages site](https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)

<br />

## 🏆 Challenges

Below are 4 additional ways you can continue to customize your portfolio site and learn some Codespaces, CSS, HTML and JavaScript along the way.

  1. [Customize your Codespaces](#1-customize-your-codespaces)
  1. [Update to smooth scroll to a section](#2-update-to-smooth-scroll-to-a-section)
  1. [Animate the desk photo](#3-animate-desk-photo)
  1. [Add a new section](#4-add-a-new-section)

### 1. Customize your Codespaces

Your environment comes with preinstalled extensions. You can change which extensions your Codespaces environment starts with, here's how:

1. Open file _.devcontainer/devcontainer.json_ and locate the following JSON element **extensions**

    ```jsonc
    "extensions": [
      "GitHub.copilot",
      "GitHub.copilot-chat",
      "ms-dotnettools.csdevkit",
      "ms-vscode.PowerShell",
      "ms-vscode.vscode-node-azure-pack",
      "VisualStudioExptTeam.vscodeintellicode"
    ]
    ```

1. Let's add the `indent-rainbow` extension. To do this, go to the **extensions** list and add:

    ```jsonc
    "oderwat.indent-rainbow"
    ```
  
   What you did above was to add the unique identifier of an extension of the [indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow&WT.mc_id=dotnet-82024-juyoo). This will let Codespaces know that this extension should be pre-installed upon startup.

To find the unique identifier of an extension:

* Navigate to the extension's web page, like so [https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow](https://marketplace.visualstudio.com/items?itemName=oderwat.indent-rainbow&WT.mc_id=dotnet-82024-juyoo)
* Locate the _Unique Identifier_ field under **More info** section on your right side.

> 💡 Learn more here, <https://docs.github.com/codespaces/customizing-your-codespace/personalizing-github-codespaces-for-your-account>

### 2. Update to smooth scroll to a section

In your site header you have links to each section below. Click one of these links and watch it scroll the page to that section. Not really a scroll, right?

Let's make this a better user experience by slowing that down so the user has a sense of what is happening, and where they are navigating to on the page. 

1. Open `/src/BlazorApp/wwwroot/css/app.css`, which is the stylesheet for your portfolio application. We need to add a style for `html`. If you look, you'll see right now `html` and `body` styles are being set together, so let's add the following css snippet to set the scrolling for the `html` element:

    ```css
    html {
      scroll-behavior: smooth;
    }
    ```

Your site should already be running in your Codespaces, and the change will reload onto the page automatically. Click a link in the top header to see the smooth scroll in action.

### 3. Animate desk photo

Animations are a way you can easily add some motion to elements on your page to increase user interactivity and highlight items you want to make sure they notice. Let's animate the desk photo in the portfolio section.

1. Open your site's stylesheet, `/src/BlazorApp/wwwroot/css/app.css` within your Codespaces. Add the animation sequence by adding a `@keyframes` definition to slide in from the left:

    ```css
    @keyframes slideInLeft {
      0% {
        transform: translateX(-100%);
      }
      100% {
        transform: translateX(0);
      }
    }
    ```

1. Now that we have defined our `slideInLeft` animation sequence we can tell our desk photo to animate itself with that sequence. Open `/src/BlazorApp/Components/Portfolio.razor` and locate the `img` tag. You will see it utilizes inline CSS to set it's styling. Within it's style definition add the following:

    ```css
    animation: 1s ease-out 0s 1 slideInLeft;
    ```

    Your image tag should look something like:

    ```html
    <img src="@(hero.Src)" style="height: 90%; width: 100%; object-fit: cover; animation: 1s ease-out 0s 1 slideInLeft;" alt="@(hero.Alt)" />
    ```

Your site should already be running in your Codespaces, and the change will reload onto the page automatically. Scroll up and down the page and watch your desk photo slide onto the page.

> 🤩 **Bonus**: Animate scroll down arrow

### 4. Add a new section

We started you off with a few basic sections for your portfolio site, but you have creative freedom to make it your own and add new sections relevant to what you want on your site.

For an example, let's add an education section to your portfolio site. 

1. Create a new component for the section within the `Components` folder. Add a new file called `Education.razor`.

1. In `Education.razor` add the component function, export and information you'd like to include:

    ```razor
    <section class="light" id="portfolio">
        <h2>Education</h2>
    </section>
    ```

1. In `Index.razor` add the `Education` component where you would like it to render within the page by inserting:

    ```razor
    <Education />
    ```

In your Codespaces, your portfolio application should be running and will reload your site with the changes.

<br />

## 📚 Resources

* [GitHub Codespaces docs overview](https://docs.github.com/codespaces/overview)
* [GitHub Codespaces guides](https://docs.github.com/codespaces/guides)
* [Use dev containers locally with VS Code and Docker](https://github.com/microsoft/vscode-remote-try-dotnet#vs-code-dev-containers)
* [Get started with Blazor](https://learn.microsoft.com/training/paths/build-web-apps-with-blazor/?WT.mc_id=dotnet-82024-juyoo)
* [Web Development for Beginners](https://github.com/microsoft/Web-Dev-For-Beginners)

> #### Codespaces Browser App
>
> If you are using Edge or Chrome you will see an option to install the Codespaces app when you launch your Codespaces. The Codespaces app lets you launch your Codespaces within the app so you can work outside of the browser.  Look for the app icon and install pop-up to try it out.
>
> <img src="./images/codespaces-app.png" alt="Codespaces browser app" style="width: 400px;"/>

<br />

## 🔎 Found an issue or have an idea for improvement?

Help us make this template repository better by [letting us know and opening an issue!](/../../issues/new).
