# abandoned crates
If you have a crate at rust's [crates.io](https://crates.io/) that you can no longer
maintain (or if you no longer want to hold the name) you can abandon it here. A team
of people will make sure that if anyone wants to maintain or use your crate name,
they will be able to.

## Process for abandoning your crate
- transfer ownership to this group via the
    [cargo command](http://doc.crates.io/crates-io.html#cargo-owner)
    - `cargo owner --add github:rust-crates:reclaimers`
- Open a [ticket](https://github.com/rust-crates/abandoned/issues/new).
    In the ticket put the following:
    - whether you want to completely abandon the crate -- in which case all versions
        will be yanked and the name will be up for grabs.
    - whether you want a new maintainer -- in which case we will try our best to
        respect that wish.

## Process for claiming a crate
You can view all abandoned crates by looking at this repo's
[branches](https://github.com/rust-crates/abandoned/branches)

If you would like to be the new owner/maintainer of a crate, open a
[ticket](https://github.com/rust-crates/abandoned/issues/new). A volunteer will
work with you to get that to happen.
