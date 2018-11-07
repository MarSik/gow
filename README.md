# Go workplace

This script makes it easy to switch Go workplaces.

Just create a .gopath file in the root directory
of what represents a GOPATH workplace and optionally
put a go version into that file.

Then execute the script from any subdirectory and it
will download golang of the right version and setup
all the necessary paths.

The tool expects https://github.com/travis-ci/gimme
is installed.

```
[msivak@msivak go10]$ echo 1.10.5 >.gopath
[msivak@msivak go10]$ gow

unset GOOS;
unset GOARCH;
export GOROOT='/home/msivak/.gimme/versions/go1.10.5.linux.amd64';
export PATH="/home/msivak/.gimme/versions/go1.10.5.linux.amd64/bin:${PATH}";
go version >&2;

export GIMME_ENV="/home/msivak/.gimme/envs/go1.10.5.env"
GOPATH=/home/msivak/go10
```

You can use `eval $(gow)` to automatically apply the change.

