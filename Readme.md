# TTLCache - an in-memory cache with expiration

# Original Project

TTLCache was forked from [github.com/ReneKroon/ttlcache](https://github.com/ReneKroon/ttlcache)

## extra
1. provide feasibility between Get and LoaderFunction by providing KeyProvider interface
```go
type KeyProvider interface {
	GetKey() string
}
```
2. fix metrics Retrievals and Hits
