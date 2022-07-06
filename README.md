# gobuildtooltest
This is to test the use go install build tool system, potentially with importing repos with go build tags.

## Instructions

To get build tags working, you need to run the install command like so.

```sh
go install -tags "extended" github.com/gohugoio/hugo
```

This will build with the proper [build tag constraint](https://pkg.go.dev/go/build/constraint)s respected.

## References

1. [official docs, but without clear examples or example that build constraint tag works](https://github.com/golang/go/wiki/Modules/6ae647c7e344bc643f9ab7478e9cdd77b8795f72#how-can-i-track-tool-dependencies-for-a-module)
1. [golang/go#25922 with proposed and accepted solution](https://github.com/golang/go/issues/25922#issuecomment-412992431)
1. [official code example cited by docs](https://github.com/go-modules-by-example/tools/commit/2b180f37cec267e315f0ea5eda249e5b8e789724)