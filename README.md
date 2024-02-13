# PROJ_KEY services

- nginx
    - ssl termination
    - custom error pages
    - router
- apache
    - backend that handles requests not for static objects

## Usage

```bash
# Git clone repo along with the submodules
git clone --recurse-submodules -j8 git-url
# see aliases.sh for short commands
```

## Deps as git submodules

See .gitmodules for dependencies

```yml
# code helpers
- .dev/certs
- .dev/helper-scripts
- .dev
    # mainly library references
    - refs 
        - h5bp
        - h5bp-apache
        - h5bp-nginx
    - jenkins_home
- _util/wptools
- laravel/blog # wordpress
- _jekyll
- _jenkins
```
