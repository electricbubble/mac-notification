# Notifier
[![go doc](https://godoc.org/github.com/electricbubble/notifier?status.svg)](https://pkg.go.dev/github.com/electricbubble/notifier?tab=doc#pkg-index)
[![go report](https://goreportcard.com/badge/github.com/electricbubble/notifier)](https://goreportcard.com/report/github.com/electricbubble/notifier)
[![license](https://img.shields.io/github/license/electricbubble/notifier)](https://github.com/electricbubble/notifier/blob/master/LICENSE)

Display a notification (macOS)

![](https://cdn.jsdelivr.net/gh/electricbubble/ImageHosting/img/20201123160223.png)

## Installation

```shell script
go get github.com/electricbubble/notifier
```

## Usage

> The sound can be one of the files in `/System/Library/Sounds` or in `~/Library/Sounds`.

```go
package main

import (
	"github.com/electricbubble/notifier"
)

func main() {
	notifier := NewNotifier(WithText("Hi, there!"), WithSound("Submarine"))
	notifier.Push()
	notifier.Push(WithText("Hi again"))
}

```

## Thanks

Thank you [JetBrains](https://www.jetbrains.com/?from=gwda) for providing free open source licenses
