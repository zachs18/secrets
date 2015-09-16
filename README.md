secrets
=======

[![Build Status][badge-ci]][ci]
[![crates.io][badge-package]][package]
[![MIT][badge-license]][license]

A library to help safely hold cryptographic secrets in memory.

Buffers allocated through this library:

* restrict themselves from being read from and written to by default
* allow access to their contents in explicit, limited scopes
* are never included in core dumps
* are never swapped to permanent storage (using `mlock`)
* are protected from overflows and underflows by inaccessible guard pages (using `mprotect`)
* are protected from underflows by a random canary
* immediately zero out the contents of the memory used to initialize them
* immediately zero out the contents of their allocated memory when they leave scope

Example
-------

Coming soon. Library very much in flux.

Documentation
-------------

[API documentation][docs] for the latest `master` is autogenerated using rustdoc.

License
-------

`secrets` is distributed under the [MIT license](./LICENSE).

[ci]:      https://travis-ci.org/stouset/secrets
[docs]:    https://stouset.github.io/secrets
[license]: https://github.com/stouset/secrets/blob/master/LICENSE
[package]: https://crates.io/crates/secrets

[badge-ci]:      https://img.shields.io/travis/stouset/secrets.svg
[badge-license]: https://img.shields.io/crates/l/secrets.svg
[badge-package]: https://img.shields.io/crates/v/secrets.svg
