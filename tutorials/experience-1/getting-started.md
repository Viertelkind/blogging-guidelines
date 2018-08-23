# Getting Started

## GET STARTED WITH HIPPO CMS

This Get Started tutorial helps you to get up and running with your first Hippo CMS implementation project.

Before you start, check out the [prerequisites](https://www.onehippo.org/trails/getting-started/prerequisites.html).

We recommend you follow the full tutorial and start with [Create the Project](https://www.onehippo.org/trails/getting-started/creating-a-project.html).

Alternatively, take a shortcut and follow the abbreviated steps below.

[Step 1: Create a project using the Hippo CMS Maven archetype:](https://www.onehippo.org/trails/getting-started/creating-a-project.html)

| `mvn org.apache.maven.plugins:maven-archetype-plugin:2.4:generate \-DarchetypeRepository=https://maven.onehippo.com/maven2` `\-DarchetypeGroupId=org.onehippo.cms7 \-DarchetypeArtifactId=hippo-project-archetype \-DarchetypeVersion=12.4.0` |
| :--- |


For Windows use:

| `mvn org.apache.maven.plugins:maven-archetype-plugin:2.4:generate -DarchetypeRepository=https://maven.onehippo.com/maven2` `-DarchetypeGroupId=org.onehippo.cms7 -DarchetypeArtifactId=hippo-project-archetype -DarchetypeVersion=12.4.0` |
| :--- |


Do not use special characters such as dot or dash in the artifactId. Also, avoid using 'cms' or 'hippo' as artifactId because these are known to cause naming conflicts.

Type ‘n’ at the prompt if you want to customize your project name or other [parameters](https://www.onehippo.org/trails/getting-started/creating-a-project.html).

[Step 2: Build the project:](https://www.onehippo.org/trails/getting-started/building-a-project.html)

| `cd` `myhippoprojectmvn clean verify` |
| :--- |


[Step 3: Run Hippo CMS:](https://www.onehippo.org/trails/getting-started/running-a-project.html)

| `mvn -Pcargo.run -Drepo.path=storage` |
| :--- |


This starts a local Tomcat container and deploys the following web applications in it:

| **Hippo CMS UI** at [http://localhost:8080/cms](http://localhost:8080/cms)Use admin/admin or editor/editor or author/author as username/password combination. These users have admin, editor and author roles respectively. Browse the [End User Manual](https://www.onehippo.org/library/end-user-manual/end-user-manual-introduction.html) to learn about creating, editing and publishing content as well as user management. | ![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/trails/getting-started-trail-10.0/cms-10.0-login.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/trails/getting-started-trail-10.0/cms-10.0-login.png) |
| :--- | :--- |
| **Hippo CMS Console** at [http://localhost:8080/cms/console](http://localhost:8080/cms/console)The [Console](https://www.onehippo.org/library/concepts/content-repository/using-the-console.html) is a power tool for advanced repository operations for use by developers and administrators. | ![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/trails/getting-started-trail-10.0/console.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/trails/getting-started-trail-10.0/console.png) |
| **Essentials** at [http://localhost:8080/essentials](http://localhost:8080/essentials)The Essentials setup application provides a [Feature Library](https://vimeo.com/105642248) from which features can be added to your project.The first time you use the application it will show a setup screen. Read carefully and if needed, change the default parameters before clicking on _**Get Started**_.Choose from a variety of features in the [library](https://www.onehippo.org/trails/getting-started/adding-features-to-a-project.html) to customize content, layout, integrations, SEO and much more. Click 'Install Feature' to add it to your project. Once installed they appear in the installed features tab where you can [configure](https://www.onehippo.org/trails/getting-started/adding-features-to-a-project.html) them. | ![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/trails/getting-started-trail-10.0/essentials-introduction.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/trails/getting-started-trail-10.0/essentials-introduction.png)![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/trails/getting-started-trail-10.0/essentials-library.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/trails/getting-started-trail-10.0/essentials-library.png) |
| **Website** at [http://localhost:8080/site](http://localhost:8080/site)The website will initially be empty. Once you have added some features from the library to the site it will render them using a default [bootstrap](http://getbootstrap.com/) theme. | ![//onehippo-prod.global.ssl.fastly.net/binaries/ninecolumn/content/gallery/connect/trails/getting-started-trail-10.0/default-site.png](https://onehippo-prod.global.ssl.fastly.net/binaries/content/gallery/connect/trails/getting-started-trail-10.0/default-site.png) |

[Step 4: Build your website:](https://www.onehippo.org/trails/developer-trail/introduction.html) 

You can now customize your newly added features or create your own. Check out our [tutorial](https://www.onehippo.org/trails/developer-trail/introduction.html) on creating a working website with Hippo CMS or take a deeper dive with our [Hello world](https://www.onehippo.org/trails/deep-dive/hello-world.html) example.

If you get stuck, check out the [troubleshooting](https://www.onehippo.org/trails/developer-trail/troubleshooting.html) and [documentation](https://www.onehippo.org/library/about/introduction-hippo.html) pages or reach out to the community through the [forum](https://community.bloomreach.com/).

