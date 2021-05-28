# actions-testing-repo

Just testing the `[skip ci]` functinoality here.
This addition shouldn't trigger CI if I do rebase merge on the PR?

## Tested

* `[skip ci]` on [direct commit to master](https://github.com/koivunej/actions-testing-repo/commit/2c2825a094e729c104ca536425be6d5775b9fd44)
* `[skip ci]` on [rebase merge"](https://github.com/koivunej/actions-testing-repo/pull/1)
    * did not run on PR nor the "rebase merge"
* `[skip ci]` on [normal merge'd PR](https://github.com/koivunej/actions-testing-repo/pull/2)
    * did not run on PR
    * did run on merge commit because it did not contain `[skip ci]`
* `[skip ci]` added on [the merge commit](https://github.com/koivunej/actions-testing-repo/pull/3)
    * expectation: run on PR
    * don't run on merge commit with `[skip ci]`
