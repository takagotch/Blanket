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


```
