# TTLCache - an in-memory cache with expiration

# Original Project

TTLCache was forked from [github.com/ReneKroon/ttlcache](https://github.com/ReneKroon/ttlcache)

## extra
1. provide feasibility between Get and LoaderFunction by providing KeyProvider interface
```go
type KeyProvider interface {
	GetKey() string
}

// examples...
localLoader := func(key KeyProvider) (data interface{}, ttl time.Duration, err error) {
return "local", 0, nil
}

key, _ := cache.Get(NewSimpleKey("test"))
```
2. fix metrics Retrievals and Hits
