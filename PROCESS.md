
> This process is still a work in progress and will
> mostly be automated in the future.

# Setting a crate to the abandoned status
When someone has abandoned a crate they will have already
- added this group as an owner on crates.io
- opened an issue requesting their crate to be abandoned

The process for abandoning the crate is:
- create and checkout a branch off of this repository
    which is the same name as the crate
    - `git checkout -b CRATE_NAME`
- edit `Cargo.toml` to be the correct name and a
    MINOR version bump, i.e. 0.2.3 -> 0.3.0
- commit your changes
    - `git commit -m CRATE_NAME: Closes ISSUE_NUMBER`
- push your changes to github
    - `git push origin CRATE_NAME`
- run `cargo publish`
- remove the user as owner
    - `cargo owner --remove OWNER`
    - you can use `cargo owner --list` to see all owners

That's it!

# Giving an abandoned crate to a new owner
When someone has requested access to a crate they will have:
- opened an issue to ask for ownership

The process for giving them the crate is:
- checkout the branch their crate exists
    - `git checkout CRATE_NAME`
- add them as owner
    - `cargo owner --add GIT_USER_NAME`
- create a pull request for the branch, make sure to specify
    "Closes ISSUE_NUMBER" in the text

That's it!
