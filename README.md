# goscripts
Useful shell scripts for go development

## gorun

Sane version of `go run`. It's basically the same as `go run *go` but
it ignores `_test` files.

Example:

    gorun

## gowatch

Runs a given command then if/when there are changes to files on disk
run the command again (and again). Useful for server development or
if you want to automatically run tests when you save a file.

Note: This script is generally useful, not just for go :)

Example:

    gowatch go test

If you need to run several commands in sequence then you can quote them
and pass them as a single argument to avoid the shell interpreting the
`;` character.

Example:

    gowatch 'goimports -w .;gorun'
