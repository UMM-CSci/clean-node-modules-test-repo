# clean-node-modules-test-repo
A repo used to test the `clean_node_modules` script.

There's probably no reason for humans to check this out unless it needs changes.
The intent is that the tests for
[clean_node_modules](https://github.com/UMM-CSci/clean_node_modules) will clone
this out in their `setup()` and use it to see if the `clean_node_modules` script
deletes the correct directories.

Cloning this will set the `atime` on all the files/directories to whatever time
the clone happened, so tests will have to use `touch -a` to set the access times
to points in the past for the two `old_...` directories.

I used [`decamelize`](https://github.com/sindresorhus/decamelize) as a nice,
simple NodeJS library that I could install quickly without creating a big
`node_modules` directory.
