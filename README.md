# renovate-composer-error

These are a valid composer.json and composer.lock
Any error Renovate 35.72 accepted them just fine; Later Renovate-versions seem to cause various errors on them.

Execute renovate like so:
docker run --rm renovate/renovate arjenm/renovate-composer-error

And that should output an error like this, which effectively says that the type:package repository is not supported.
```
       "err": {
         "issues": [
           {
             "code": "invalid_union",
             "unionErrors": [
               {
                 "issues": [
                   {
                     "code": "invalid_union_discriminator",
                     "options": ["composer", "vcs", "git", "path"],
                     "path": ["type"],
                     "message": "Invalid discriminator value. Expected 'composer' | 'vcs' | 'git' | 'path'"
```
