<!-- markdownlint-configure-file
{
  "no-empty-links": false,
  "line-length": false
}
-->

# O'Reilly Awesome List

Read about [how to contribute](CONTRIBUTING.md) to this list!

- TOC
{:toc}

## Command Line

**[`^        back to top        ^`](#)**

### CLI Reference & Tips

1. Find your public IP address:

    ```sh
    dig +short myip.opendns.com @resolver1.opendns.com
    ```

2. Lookup command examples:

    ```sh
    curl -s cheat.sh/<command>
    ```

3. Zsh does not enable a builtin `help` command, instead it provides `run-help`. By default `run-help` is an alias to `man` and will only work on external commands. To use it for Zsh builtins and features, load and unalias the command in your `.zshrc`.

    ```sh
    autoload -Uz run-help
    unalias run-help
    alias help=run-help # for convenience
    ```

4. To remove duplicate lines from unsorted data:

    ```sh
    echo "Apple\nOrange\nOrange \nBanana\nApple\nPineapple" > file1
    awk '!a[$0]++' file1
    Apple
    Orange
    Banana
    Pineapple
    ```

5. To merge text files side-by-side:

    ```sh
    echo "HEADER1\nData-1\nData-2" > file1
    echo "HEADER2\nValue-1\nValue-2" > file1

    paste file1 file2
    HEADER1 HEADER2
    Data-1  Value-1
    Date-2  Value-2
    ```

### CLI Tools

- General Tools:
  - [btop](https://github.com/aristocratos/btop): A monitor of resources
  - [exa](https://the.exa.website): modern `ls` replacement
  - [trash-cli](https://github.com/sindresorhus/trash-cli): Move files and folders to the trash
  - [zoxide](https://github.com/ajeetdsouza/zoxide): A smarter cd command

- Searching & Manipulating Data:
  - [jq](https://stedolan.github.io/jq/): Formats and filters JSON data
  - [ripgrep (rg)](https://github.com/BurntSushi/ripgrep): Fast, `.gitignore`-aware search tool
  - [yq](https://github.com/kislyuk/yq): jq wrapper for YAML/XML/TOML documents

- Scripting:
  - [Shellcheck](https://www.shellcheck.net/): Shell script linting

- Network/Internet Tools:
  - [curlconverter](https://github.com/curlconverter/curlconverter): transpiles `curl` commands into programs in other programming languages
  - [Httpie](https://httpie.io/): Better cURL

- Text Presentation:
  - [bat](https://github.com/sharkdp/bat): a `cat` clone with wings
  - [Glow](https://github.com/charmbracelet/glow): Renders markdown
  - [slides](https://github.com/maaslalani/slides): Terminal based presentation tool

- Zsh Prompt/Config Managers:
  - [Oh My Zsh](https://ohmyz.sh): A framework for managing your Zsh configuration
  - [Powerlevel10k](https://github.com/romkatv/powerlevel10k): Performant and adaptable prompt generator
  - [Starship](https://starship.rs): Minimal and customizable prompt manager

- Zsh Plugins:
  - [zsh-syntax-highlighting](https://github.com/zsh-users/zsh-syntax-highlighting): syntax highlighting for Zsh
  - [zsh-autosuggestions](https://github.com/zsh-users/zsh-autosuggestions): autosuggestions for zsh

## Git

**[`^        back to top        ^`](#)**

### Git Reference & Tips

- [ohshitgit](https://ohshitgit.com/): Plain english solutions to Git conflicts

### Git Tools

- [delta](https://github.com/dandavison/delta): GitHub style diffs
- [forgit](https://github.com/wfxr/forgit): A utility tool powered by fzf for using git interactively
- [gh](https://cli.github.com): GitHub CLI and API wrapper

## Docker

**[`^        back to top        ^`](#)**

### Docker Reference & Tips

List container tags:

```sh
# from DockerHub:
wget -q https://registry.hub.docker.com/v1/repositories/<container>/tags -O - | jq -r '.[].name'

# from GCR:
gcloud container images list-tags gcr.io/<project>/<container>
```

### Container Tools

- [dive](https://github.com/wagoodman/dive): Layer and filesystem explorer
- [Hadolint](https://github.com/hadolint/hadolint): Dockerfile linter for best practices

## Kubernetes

**[`^        back to top        ^`](#)**

### K8s Tools

- [Krew](https://krew.sigs.k8s.io): A `kubectl` plugin manager
  - [cert-manager](https://cert-manager.io/docs/usage/kubectl-plugin/)
  - [config-cleanup](https://github.com/B23admin/kubectl-config-cleanup)
  - [deprecations](https://github.com/rikatz/kubepug)
  - [get-all](https://github.com/corneliusweig/ketall)
  - [ksniff](https://github.com/eldadru/ksniff)
- [Stern](https://github.com/wercker/stern): Easy pod and container log viewer

### K8s Reference & Tips

An alternative for `kubectl get all` that returns ***all*** resources. Warning: can be slow.

```sh
kubectl api-resources --verbs=list --namespaced --output name \
    | xargs -n 1 kubectl get --show-kind --ignore-not-found --namespace <namespace> --selector <label>
```

## Python

**[`^        back to top        ^`](#)**

### Modules

- [Click](https://pypi.org/project/click/): Powerful and flexible command line options/arguments
- [Logzero](https://pypi.org/project/logzero/): Easy and effective logging

## VSCode

**[`^        back to top        ^`](#)**

### VSCode Reference & Tips

Perform a diff between two files.

```sh
code --diff <file1> <file2>
```

### Extensions

- [markdownlinter](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint): Markdown/CommonMark linting and style checking
- [shellcheck](https://marketplace.visualstudio.com/items?itemName=timonwong.shellcheck): Bash/Shell script linter

## Newsletters & Blogs

**[`^        back to top        ^`](#)**

- [Julia Evans](https://jvns.ca/)
- [Console](https://console.substack.com/)
- [The ReadME Project](https://github.com/readme)
- [O'Reilly Newsletters](https://www.oreilly.com/emails/newsletters/)

## Awesome Lists

**[`^        back to top        ^`](#)**

- [Awesome CLI](https://github.com/agarrharr/awesome-cli-apps)
- [Awesome Docker](https://github.com/veggiemonk/awesome-docker)
- [Awesome Python](https://github.com/vinta/awesome-python)
- [F!%king Awesome Python](https://github.com/trananhkma/fucking-awesome-python)
- [Awesome Shell](https://github.com/alebcay/awesome-shell)
- [Awesome SysAdmin](https://github.com/kahun/awesome-sysadmin)
