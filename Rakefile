# -*- ruby -*-

require 'rubygems'
require 'hoe'

Hoe.add_include_dirs("../../RubyInline/dev/lib",
                     "../../ZenTest/dev/lib")

Hoe.plugin :seattlerb

h = Hoe.spec 'wilson' do
  developer 'Ryan Davis', 'ryand-ruby@zenspider.com'

  multiruby_skip << '1.9' << 'trunk' << "2."
end

namespace :test do
  desc "profiles your tests"
  task :prof do
    ruby "-S zenprofile #{h.make_test_cmd}"
  end
end

# vim: syntax=Ruby
