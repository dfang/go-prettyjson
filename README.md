# prettyjson

JSON pretty print for Golang.

## Example

```go
import "github.com/hokaccha/go-prettyjson"

v := map[string]interface{}{
    "str": "foo",
    "num": 100,
    "bool": false,
    "null": nil,
    "array": []string{"foo", "bar", "baz"},
    "map": map[string]interface{}{
        "foo": "bar",
    },
}
s, _ := prettyjson.Marshal(v)
fmt.Println(string(s))
```

![Output](http://i.imgur.com/cUFj5os.png)

## Debugging Functions

For quick debugging, you can use the `Print` and `Printf` functions:

### Print
```go
// Simply print pretty JSON to stdout
data := map[string]interface{}{
    "name": "John",
    "age": 30,
}
prettyjson.Print(data)
```

### Printf
```go
// Print with custom formatting
prettyjson.Printf("User data: %s\n", data)
prettyjson.Printf("=== JSON ===\n%s\n=== END ===\n", data)
```

## License

MIT
