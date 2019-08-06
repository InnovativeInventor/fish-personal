# [Oh My Fish][oh-my-fish] personal package repository
Personal package repository for the [Oh My Fish][oh-my-fish] [Fish shell][fish] framework.

Note: This is for my personal use only. There is a reason why these packages are not on [packages-main](https://github.com/oh-my-fish/packages-main).

## Repository format
Packages are referenced in the repository using property files located in the `packages/` directory. The actual code of each package is stored in separate, individual Git repositories maintaned by the package mantainer themselves. This keeps control of the package in the owner's hands, but still allows easy sharing of the package.

The name of each property file indicates the package name, and the various properties in the file describe the package and how it can be installed. These are the properties currently used:

- `type`: The type of package. Can be `plugin` or `theme`.
- `repository`: A cloneable Git URL to the package source repository.
- `maintainer`: The name and email of the maintainer of the package.
- `description`: A short description of the package.

## Submitting a package
Want to add your own package to the public repository? First, make a fork of this Git repository. Then create a package description file inside the `packages/` directory. The file name should be the name of your package without any file extensions, and should contain at least these properties:

```
type = plugin
repository = YOUR-PACKAGE-URL
maintainer = YOUR-NAME <YOUR-EMAIL>
description = YOUR-PACKAGE-DESCRIPTION
```

Be sure to use a cloneable Git URL for your package. If your package is a theme, use `type = theme` instead.

Once you've created and committed your package description file, [open a pull request][new-pr] with your change, and the repository maintainers will review your submission and merge it in to the main repo.

Once your pull request is merged, your package will be immediately available for all users to install!


[fish]: http://fishshell.com
[new-pr]: https://github.com/oh-my-fish/packages-main/pull/new/master
[oh-my-fish]: https://github.com/oh-my-fish/oh-my-fish
