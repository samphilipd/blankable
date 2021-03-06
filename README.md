# Blankable

Implementation of `blank?` in Elixir. Aims to work in a practically identical fashion to [ActiveSupport's #blank? method](http://api.rubyonrails.org/files/activesupport/lib/active_support/core_ext/object/blank_rb.html).

## Installation

Add `blankable` to your list of dependencies in `mix.exs`:

```elixir
def deps do
  [{:blankable, "~> 1.0.0"}]
end
```

## Usage

```
iex> Blankable.blank?(nil)
true
iex> Blankable.blank?("")
true
iex> Blankable.blank?([])
true
iex> Blankable.blank?("Hello")
false
```

You can also get behaviour similar to ActiveSupport's `present?` method like so:

```elixir
def present?(term) do
  !Blankable.blank?(term)
end
```
