### Blanket
---
.rb
https://github.com/inf0rmer/blanket

.js
https://github.com/alex-seville/blanket

```
gem 'blanket_wrapper'
bundle
gem install blanket_wrapper

```

```ruby
require 'blanket'
github = Blanket.wrap("https://api.github.com")
user = github.users('inf0mrmer').get
user.login
github.users('inf0rmer').repos.get

github = Blanket.wrap("https://api.github.com")
github.users('inf0rmer').repos.get

github = Blanket.wrap("https://api.github.com")
github.users
github.users('inf0rmer')
github.users('inf0rmer').repos

github.get('users/inf0rmer/repos')
github.send('users/inf0rmer').repos

user = githu.users('inf0rmer').get
user.login
user.url
repo = github.repos('inf0rmer').get('blanket')
repo.owner.login

repos = github.users('inf0rmer').repos.get
repos.map(&:name)

api.users(55).get(params: {foo: 'bar'})
# => "http://api.ex.org/users/55?foo=bar"

api = Blanket::wrap("http://api.ex.org", params: {access_token: 'my secret token'})

api = Blanket::wrap("http://api.ex.org", headers: {token: 'my secret token'})
api.users(55).get(headers: {foo: 'bar'})

api = Blanket::wrap("http://api.ex.org", extension: :json)
users_endpoint = api.users(55)
users_endpoint.extension = :xml

begin
  api.thingamajig.get
rescue Blanket::ResourceNotFound => e
  e.code
  e.message
  e.body
end

```
