begin
  require 'jeweler'
  Jeweler::Tasks.new do |s|
    s.name = "twitter-lists-cli"
    s.executables = ["twitter-auth", "twitter-follow", "twitter-following", "twitter-lists"]
    s.summary = "Command-line client for manipulating Twitter lists."
    s.email = "dlitz@dlitz.net"
    s.homepage = "http://github.com/dlitz/twitter-lists-cli"
    s.description = <<EOF
A command-line client for manipulating large Twitter lists in the shell, shell scripts, etc.

Currently supports
------------------
- OAuth authentication
- Showing a users's followers/following
- Following and unfollowing users
- Showing, adding, and removing a members from a list
EOF
    s.authors = ["Dwayne Litzenberger"]
    s.files = FileList["[A-Z]*", "bin/**/*"]
    s.add_dependency "twitter", "~> 0.9.5"    # John Nunemaker's twitter gem
  end
rescue LoadError
  puts "Jeweler, or one of its dependencies, is not available. Install it with: gem install jeweler"
end
