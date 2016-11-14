# Dotfiles

Forked from https://github.com/thoughtbot/dotfiles which explains the setup

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
