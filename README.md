# Cyno - Yet an another firewall middleware for Gin

## Name: Inspired by Genshin Impact(Cyno is the General Mahamatra and he leads the Matra and strikes fear into the hearts of researchers of the Sumeru Akademiya.)

## Features:
1. Automatic Ban CC Attack
2. Record User Footstep by Clientid
3. etc

## How to use:

```shell
go get -u github.com/chi-net/cyno
```

```go
package main

import (
	"github.com/chi-net/cyno"
	"github.com/gin-gonic/gin"
)

func main() {
	r := gin.Default()

	r.Use(cyno.Default())

	r.get("/ping", func(c *gin.Context) {
		c.JSON(200, gin.H{
			"status": 200,
			"ping":   "pong",
		})
	})

	r.Run(":8080")
}
```

## License:

Under GPL-3.0 License.

## Used by:

[Nahida-web](https://openid.chinet.work/login)