# logutil

> Utilities to init and set defaults for zerolog

# NOTE: deprecated, merged into https://github.com/avakarev/go-util
> Scheduled for deletion after 2023-09-01


## Install

```shell
go get github.com/avakarev/go-logutil
```

## Usage

Initialize `go-logutil` before any other packages in your app for consistent logging format.

```go
package main

import (
	"github.com/avakarev/go-logutil"
	"github.com/rs/zerolog/log"
)

func main() {
	logutil.MustInit()

	log.Debug().Msg("Hello World!")
}
```

It respects `LOG_LEVEL` environment variable and sets global level for [zerolog](https://github.com/rs/zerolog).
If not set, default log level is `info`.

See allowed logging levels in zerolog's documentation: https://github.com/rs/zerolog#leveled-logging.


## License

`go-logutil` is licensed under MIT license. (see [LICENSE](./LICENSE))
