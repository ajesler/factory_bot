# Global sequences

Unique values in a specific format (for example, e-mail addresses) can be
generated using sequences. Sequences are defined by calling `sequence` in a
definition block, and values in a sequence are generated by calling `generate`:

```ruby
# Defines a new sequence
FactoryBot.define do
  sequence :email do |n|
    "person#{n}@example.com"
  end
end

generate :email
# => "person1@example.com"

generate :email
# => "person2@example.com"
```