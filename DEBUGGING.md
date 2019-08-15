Some debugging tools and tricks

## Useful Regex

Legacy codebases
* Search for empty test blocks
`ag 'do$[ \s]*end' spec/`
Matches
```ruby
it "does a thing" do
end

it "has a few lines in between" do

end
```

## Useful Linux
* See the process given a PID 1337
`ps -p 1337 -o comm=`
http://superuser.com/questions/632979/if-i-know-the-pid-number-of-a-process-how-can-i-get-its-name

* And then to kill the process `kill 1337`
Mysql acting up with:
Mysql2::Error: Can't connect to local MySQL server through socket
'/tmp/mysql.sock' (2)
from
/Users/acann/.rbenv/versions/2.3.1/lib/ruby/gems/2.3.0/gems/mysql2-0.3.20/lib/mysql2/client.rb:70:in
`connect'

# find replace
find app/models/ -type f -exec sed -i "" 's/old string/new string/g' {} \;
