[![Build Status](https://travis-ci.org/rust-lang/rustup.svg?branch=master)](https://travis-ci.org/rust-lang/rustup)

The rustup.sh script installs Rust from the Rust release channels.

This script is most often run directly from the web.

```
curl -sf https://static.rust-lang.org/rustup.sh | sudo sh
```

Features:

* Install from stable, beta, or nightly channels.
* Install from the archives.
* Verifies hashes.
* Verifies signatures (if gpg is available).
* Resumes downloads.
* For Linux and OS X (Windows support someday).

## Examples

Download and install the default channel, currently beta.

```
rustup.sh
```

Install to a particular location.

```
rustup.sh --prefix=my/install/dir
```

Save downloads for faster re-installs.

```
rustup.sh --save
```

Install nightly.

```
rustup.sh --channel=nightly
```

Install nightly archives.

```
rustup.sh --channel=nightly --date=2015-04-09
```

Install explicit versions.

```
rustup.sh --revision=1.0.0-beta
```

## Future work

* GC old temp and cache files.
* Do cleanup of in-use temp files on trap.
* Don't clobber multirust if it is installed at the destination prefix.

# License

This software is distributed under the terms of both the MIT license
and/or the Apache License (Version 2.0), at your option.

See [LICENSE-APACHE](LICENSE-APACHE), [LICENSE-MIT](LICENSE-MIT) for details.
