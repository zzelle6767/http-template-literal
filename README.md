# http-template-literal

Make HTTP requests the way TBL intended.

```javascript
var res = await http`
  GET https://httpbin.org/get
  Accept: application/json
`
console.log('Request one:', res.body)

var res = await http`
POST https://httpbin.org/post
Content-Type: application/json

${JSON.stringify({
  hello: 'world',
  awesome: true
})}
`
console.log('Request two:', res.body)
```

## FAQ

### Oh cool, should I use this?

No.