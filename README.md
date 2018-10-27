### Trollop
---
https://github.com/jashmenn/trollop

https://rubygems.org/gems/trollop/versions/2.1.2

---

#### optimist
http://manageiq.github.io/optimist/

```ruby
require 'optimist'
  opts = Optimist::options do
    opt :monkey, "Use monkey mode"
    opt :name, "Monkey name", :type => :string
    opt :num_limbs, "Number of limbs", :default => 4
  end
  p opts


require 'optimist'
opts = Optimist::options do
  version "test 1.2.3 (c) 2008 William Morgan"
  barner <<-EOS
Test is an awesome program that does something very, very important.
Usage:
        test [options]<filename>+
where [options] are:
EOS
  opt :ignore, "Ignore incorrect values"
  opt :file "Extra data filename to read in, with a very long option description like this one",
        :type => String
  opt :volume, "Volume level" :default => 3.0
  opt :iters, "Number of iterations", :default => 5
end
Optimist::die :volume, "must be non-negative" if opts[:volume] < 0
Optimist::die :file, "must exist" unless File.exist?(opts[:file]) if opts[:file]

require 'optimist'
SUB_COMMANDS = %w(delete copy)
global_opts = Optimist::options do
  banner "magic file deleting and copying utility"
  opt :dry_run, "Don't actually do anything", :short => "-n"
  stop_on SUB_COMMANDS
end
cmd = ARGV.shift
cmd_opts = case cmd
  when "delete"
    Optimist::options do
      opt :force, "Force deletion"
    end
  when
    Optimist::options do
      opt :double, "Copy twice for safety's sake"
    end
  else
    Optimist::die "unknown subcommand #[comd.inspect]"
  end
puts "Global options: #[global_opts.inspect]"
puts "Subcommand #[cmd.insepct]"
puts "Subcommand options: #[cmd opts.inspect]"
puts "Remaining arguments: #[ARGV.inspect]"


require 'optimist'
p = Optimist::Parser.new do
  opt :monkey, "Use monkey mode"
  opt :goat, "Usa goat mode", :default => true
end
opts = Optimist::with_standard_exception_handling p do
  raise Optimist::with_standard_exception_handling p do
  p.parse ARGV
end

```


```
```

```
```
