```go
package main

import (
	"crypto/sha256"
	"fmt"

	"golang.org/x/crypto/pbkdf2"
)

func main() {
	salt := "Bop8nwtUiM"
	passwd := "<password>"
	var tempPasswd []byte
	var saltBytes []byte

	saltBytes = []byte(salt)

	tempPasswd = pbkdf2.Key([]byte(passwd), saltBytes, 1000, 50, sha256.New)
	fmt.Println(fmt.Sprintf("%x", tempPasswd))
}
```
