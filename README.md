<!-- markdownlint-configure-file
{
  "no-empty-links": false
}
-->

# O'Reilly Awesome List

## Command Line

**[`^        back to top        ^`](#)**

### CLI Reference & Tips

### CLI Tools

- [gh](https://cli.github.com): GitHub CLI and API wrapper
- [Glow](https://github.com/charmbracelet/glow): Renders markdown
- [jq](https://stedolan.github.io/jq/): Formats and filters JSON data
- [Shellcheck](https://www.shellcheck.net/): Shell script linting

- Zsh Prompt/Config Managers:
  - [Oh My Zsh](https://ohmyz.sh): A framework for managing your Zsh configuration
  - [Powerlevel10k](https://github.com/romkatv/powerlevel10k): Performant and adaptable prompt generator
  - [Starship](https://starship.rs): Minimal and customizable prompt manager

### Dotfile Collections

- Brad: [vim](https://gist.github.com/bradleyfrank/2daa8dc057e58812643c9ec2f8d83156), [tmux](https://gist.github.com/bradleyfrank/575239da734aa7c8d9382a6afa576e4f), [zshrc](https://gist.github.com/bradleyfrank/8c2fc19c4d8b7a179c132ac937cc6728), [etc...](https://github.com/bradleyfrank/ansible)

## Git

**[`^        back to top        ^`](#)**

### Git Reference & Tips

- [ohshitgit](https://ohshitgit.com/): Plain english solutions to Git conflicts

### Git Tools

- [delta](https://github.com/dandavison/delta): GitHub style diffs

## Docker

**[`^        back to top        ^`](#)**

### Container Tools

- [dive](https://github.com/wagoodman/dive): Layer and filesystem explorer
- [Hadolint](https://github.com/hadolint/hadolint): Dockerfile linter for best practices

## Kubernetes

**[`^        back to top        ^`](#)**

### K8s Tools

- [Krew](https://krew.sigs.k8s.io): A `kubectl` plugin manager
- [Stern](https://github.com/wercker/stern): Easy pod and container log viewer

### K8s Reference & Tips

An alternative for `kubectl get all` that returns ***all*** resources. Warning: can be slow.

```sh
kubectl api-resources --verbs=list --namespaced --output name \
    | xargs -n 1 kubectl get --show-kind --ignore-not-found --namespace {{ namespace }} --selector {{ label }}
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