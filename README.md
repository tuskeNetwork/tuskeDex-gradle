# tuskeDex-gradle

TuskeDex v1 gradle build plugins

## tuskeDex.post-build plugin
Gradle plugin for copying a repo distribution's run script and lib dir to root project directory.

### Usage

#### Define git submodule 'tuskeDex-gradle' in your repo

```asciidoc
$ git submodule add https://github.com/tuskeNetwork/tuskeDex-gradle.git
```


#### Link submodule 'haveno-gradle' in your repo

```asciidoc
$ git add tuskeDex-gradle 
$ git commit -m "Add submodule tuskeDex-gradle" tuskeDex-gradle .gitmodules 
$ git push
```

#### Register and clone new submodule 'tuskeDex-gradle' in your repo

```asciidoc
$ git submodule init 
$ git submodule update
```

#### Alternatively clone your repo with --recursive option

```asciidoc
$ git clone --recursive your-repo.git   
```

#### Apply plugin `tuskeDex.post-assemble` to your Gradle application project's build:

```asciidoc
plugins {
    id 'application'
    id 'tuskeDex.post-build'
}
```

The `tuskeDex.post-build` plugin's `postBuild` will execute at the end of your project's build task `build`.

