> [!NOTE]
> Further development of this template is done here: https://github.com/behrica/devcontainer-templates



A template project featuring a devcontainer setup for Datascience with Clojure using several libraries from [scicloj](https://scicloj.github.io/)

It sets up an dev container environment with several tool s and libaries for datascience in Clojure.

# Quickstart
1. Create a new GitHub repository based on this template
2. Clone and open repository with VSCode / devpod / Codespaces and trigger/wait for container build
3. "jack in" inside the devcontainer
4. Enjoy Clojure and R  + python from Clojure  (using ClojisR + libpython-clj)

## Customization

5. Customize libraries
    * deps.edn: add Clojure + Java libraries
    * pyproject.toml: add python libraries into poetry config file
    * devcontainer.json: add R libraries (see [r-packages](ghcr.io/rocker-org/devcontainer-features/r-packages)


6. (Install more features in devcontainer: https://containers.dev/features)
7. (Remove things you don't need)
   


## Installed inside devcontainer
The provided devcontainer.json installs in the devcontainer:

* Clojure (incl. clojisr and libpython-clj)
* Python (packages can be added vi calling "pip" in devcontainer.json)
* R (packages can be added in devcontainer.json)
   * rstudio-server

* deps.edn with Clojure libraries for Data science from scicloj
* noVNC + lite desktop incl port forwarding
* Emacs
* quarto cli
* docker-in-docker
* leiningen
* babashka
* lsp

### Graphical Emacs in web-noVNC
In the default settings, we will get a vanilla Emacs running in noVNC.
The Emacs setup can be configured via providing a specific script in a fixed location 
, which can be most easly done using the dotfile support of devcontainer.

See here: [dotfiles](https://code.visualstudio.com/docs/devcontainers/containers#_personalizing-with-dotfile-repositories)

If there is a file in `/home/vscode/.setup-ide/setup-ide.sh` it will be executed after container creation.
This can do "whatever" to configure Emacs from your own configuration.
(Baically the script can do everything on the build container.)

My `setup-ide.sh` configures Doom Emacs with my personal configuration.





