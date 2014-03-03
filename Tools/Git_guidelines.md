# Git guidelines

1. Every project *MUST* have its own repository

2. Every repository *MUST* have at least two branches
    1. `master` - the current stable version of the project
    2. `staging` - the current development version

3. Development *MUST* only happen in the `staging` branch

4. Release
    1. When the `staging` branch is considered stable and feature complete, it *MUST* get a new version number: Either by [PEP-386][pep386] or according to [semver][semver]. We *MAY* use [PEP-440][pep440] here, but this is still a draft and is therefore NOT *RECOMMENDED*.
    2. The `staging` branch *MUST* be merged into to the `master` branch.
    3. The `HEAD` commit in the `master` branch *MUST* get a tag named after the version preceded by a lowercase `v`. E.g. a version `1.2rc4` will have a tag `v1.2rc4`, a version `4.5.6` will have a tag `v4.5.6` and a version `1.2.3-beta.4` will have a tag `v1.2.3-beta.4`.

5. Bug-fixes related to an existing issue or more complicated features *SHOULD NOT* be pushed to the `staging` branch directly. One *SHOULD* create a [merge-request][merge-request] and at least two other developers *SHOULD* review the code. This prevents many bugs to be pushed to staging. Notwithstanding, minor fixes, such as spelling corrections or obvious few-line-changes, *MAY* be pushed to `staging` directly.

     1. If a merge request includes migrations, one *MUST* make sure that the migration ID does NOT exist for the respective Django application. If migration IDs are NOT unique, one *MUST* increment the IDs of the migrations that are part of the merge request, so that the IDs are both, *continual* AND *unique*: `0001_existing`, `0002_existing`, `0003_existing`, `0002_merge`, `0003_merge` *MUST* result in `0001_existing`, `0002_existing`, `0003_existing`, `0004_merge`, `0005_merge`.

## Git Commits and Issues
* If a commit fixes an issues, use ```Fixes #10``` where 10 is the number of the issue
* In the comments of the issue write **how** you fixed the issue and **add links** that helped you. If possible document the solution in the appropriate place (GitHub, GitLab, codepen.io, jsfiddle, etc).

## Open Source GitHub Repositories
* Every open source repository should has a minimum code quality.
* The minimum code quality should be decided on per project base.
* Until this quality is reached, we use our internal GitLab repository.

