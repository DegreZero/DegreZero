### Hi guys, here's a little secret for you to exploit 👋

```go
if nf, ok := output.(float64); ok {
    return nf, nil
} else if ni, ok := output.(int); ok {
    return float64(ni), nil
}
log.Errorw("invalid query execution: result should be number", "query", query, "result", output, "type", reflect.TypeOf(output))
return num, errors.New("invalid query execution result")
```
