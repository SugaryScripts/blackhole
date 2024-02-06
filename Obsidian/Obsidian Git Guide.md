#literature 
at Medium by [Luca Franceschini](https://lucafrance.medium.com/?source=post_page-----f2b42d3b77b3--------------------------------)

An Obsidian vault can be versioned efficiently with git, as it consists mostly of markdown files. The right plugin automates committing and pushing to a remote. Here is how to do it with GitHub.

# Set up the GitHub repository

Create a new repository and set the visibility to private, unless you plan on sharing your obsidian vault with the internet.

![](https://miro.medium.com/v2/resize:fit:700/0*XCvRVM8CxiSd0d6L.png)

Commit a `.gitignore` file with the following lines. The `.gitignore` is set up to ignore the whole `.obsidian` folder by default and only include explicitly mentioned configuration files.

![](https://miro.medium.com/v2/resize:fit:700/0*nLrQfy7DUuqkum4C.png)

# Set up the Obsidian vault

Clone the repository you just created. If you want to use an existing vault, move all files to the cloned repository (including the `.obsidian` directory), then open the vault in the new folder with Obsidian. If not, start a new vault in the folder of the repository.

![](https://miro.medium.com/v2/resize:fit:700/0*REYukxddohqTMnFh.png)

# Configure the plugin

Go to _Options_ > _Community plugins_. If necessary, turn on the community plugins.

![](https://miro.medium.com/v2/resize:fit:700/0*pSVX7rzwfiNTNsYG.png)

Click _Browse_, then install and enable the [_Obsidian Git_](https://github.com/denolehov/obsidian-git) plugin by Denis Olehov.

![](https://miro.medium.com/v2/resize:fit:700/0*fTFjWGG0idF0Gsgo.png)

![](https://miro.medium.com/v2/resize:fit:700/0*FqSnBvWoI57ocfMw.png)

Enter a backup interval in the obsidian vault. The plugin will then regularly commit your changes and push them to GitHub. I also recommend disabling the notifications.

![](https://miro.medium.com/v2/resize:fit:700/0*Y1TXLV4e2ndTn8lL.png)

![](https://miro.medium.com/v2/resize:fit:700/0*Fn9rghWX2L_VbamV.png)

# Conclusion

Done! Your obsidian vault is now backed up to GitHub at regular intervals.

![](https://miro.medium.com/v2/resize:fit:700/0*Pyv1w7SMkZ1L14c5.png)

_This article has been updated since the first publication._ _Thank you_ [_BrandonTheTinkerer_](https://medium.com/@brandonthetinkerer) _for_ [_the suggestion_](https://medium.com/p/d739a6944583)_._

_Originally published at_ [_https://lucaf.eu_](https://lucaf.eu/2023/01/02/obsidian-git.html) _on January 2, 2023._

