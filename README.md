# pkgnotmatch-use

Test if package path last element not match package name

# Usage

Download or git clone this respo directly.

Run:

```sh
go run main.go
```

# Conclusion

Golang can use package which its name is not match its path.

The customer should use the package name instead of last element of its path.

- success: `abc.F01()`
- failed: `importnotmatchmod.F01()`

About import:

- can be: `import "github.com/vikyd/importnotmatchmod"`
  - used as: `abc.F01()`
- can also be: `import abc "github.com/vikyd/importnotmatchmod"`
  - used as: `abc.F01()`
- can also be: `import othername "github.com/vikyd/importnotmatchmod"`
  - used as: `othername.F01()`
