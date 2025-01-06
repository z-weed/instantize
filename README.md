# instantize

Easily create instance variables from method arguments

### I'm sure many have ended up in situations like this:

```ruby
class TestKlass
  def some_method(some_arg, some_other_arg, some_stuff)
    @some_arg = some_arg
    @some_other_arg = some_other_arg
    @some_stuff = some_stuff
  end
end
```

#### With this gem we can do it like this:

```ruby
class TestKlass
  include Instantize::Argument
	
  def some_method(some_arg, some_other_arg, some_stuff)
    instantize local_context
  end
end
```
