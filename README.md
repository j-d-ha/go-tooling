# go-tooling

## Introduction

These are go tools I like to use. Setup and usage instructions are provided along with configuration
where needed.

## [`golangci-lint`](https://golangci-lint.run/)

### Install

```sh
brew install golangci-lint
brew upgrade golangci-lint
```

### Setup

#### GoLand / IntelliJ

1. Install [plugin](https://plugins.jetbrains.com/plugin/12496-go-linter)
2. get path of executable using this command in the terminal

    ```sh
    where GoLandci-lint
    ```
3. take output of above command and add it to and set in settings for `gol linter` plugin
4. copy `.GoLandci.yaml`
   from [here](https://github.com/GoLandci/GoLandci-lint/blob/master/.GoLandci.yaml) and add to root
   of project

## [`gofumpt`](https://github.com/mvdan/gofumpt)

### Install

```sh
go install mvdan.cc/gofumpt@latest
```

### Setup

#### GoLand / IntelliJ

1. Search everywhere with `cmd + shift + a`, search for `File Watchers`, and click on it
2. Click on the + on the top left side to add a new file watcher
3. Choose Custom Template
4. File Types: Select all .go files
5. Scope: Project Files
6. Program: `gofumpt` executable from the bellow command:

    ```sh
    where gofumpt
    ```
7. Arguments: `-w FilePath$`
8. Output path to refresh: `$FilePath$`
9. Working directory: `$ProjectFileDir$`
10. Environment variables: `GOROOT=$GOROOT$;GOPATH=$GOPATH$;PATH=$GoBinDirs$`

## [`gci`](https://github.com/daixiang0/gci)

### Install

```sh
go install github.com/daixiang0/gci@latest
```

### Setup

#### GoLand / IntelliJ

1. Search everywhere with `cmd + shift + a`, search for `File Watchers`, and click on it
2. Click on the + on the top left side to add a new file watcher
3. Choose Custom Template
4. File Types: Select all .go files
5. Scope: Project Files
6. Program: `gci` executable from the bellow command:

    ```sh
    where gci
    ```
7. Arguments: `write -s standard -s default -s blank -s dot -s alias -s localmodule $FilePath$`
8. Output path to refresh: `$FilePath$`
9. Working directory: `$ProjectFileDir$`
10. Environment variables: `GOROOT=$GOROOT$;GOPATH=$GOPATH$;PATH=$GoBinDirs$`

## [`tagalign`](https://github.com/4meepo/tagalign)

### Install

```sh
go install github.com/4meepo/tagalign/cmd/tagalign@latest
```

### Setup

#### GoLand / IntelliJ

1. Search everywhere with `cmd + shift + a`, search for `File Watchers`, and click on it
2. Click on the + on the top left side to add a new file watcher
3. Choose Custom Template
4. File Types: Select all .go files
5. Scope: Project Files
6. Program: `tagalign` executable from the bellow command:

    ```sh
    where tagalign
    ```
7. Arguments: `-fix -sort -strict $FilePath$`
8. Output path to refresh: `$FilePath$`
9. Working directory: `$ProjectFileDir$`
10. Environment variables: `GOROOT=$GOROOT$;GOPATH=$GOPATH$;PATH=$GoBinDirs$`

## [`golines`](https://github.com/segmentio/golines)

> **Note**
> I don't recommend using this formater in most situations.

### Install

```sh
go install github.com/segmentio/golines@latest
```

### Setup

#### GoLand / IntelliJ

1. Search everywhere with `cmd + shift + a`, search for `File Watchers`, and click on it
2. Click on the + on the top left side to add a new file watcher
3. Choose Custom Template
4. File Types: Select all .go files
5. Scope: Project Files
6. Program: `golines` executable from the bellow command:

    ```sh
    where golines
    ```
7. Arguments: `$FilePath$ --write-output --max-len=100 --no-reformat-tags`
8. Output path to refresh: `$FilePath$`
9. Working directory: `$ProjectFileDir$`
10. Environment variables: `GOROOT=$GOROOT$;GOPATH=$GOPATH$;PATH=$GoBinDirs$`