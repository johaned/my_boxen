# This file manages Puppet module dependencies.
#
# It works a lot like Bundler. We provide some core modules by
# default. This ensures at least the ability to construct a basic
# environment.

# Shortcut for a module from GitHub's boxen organization
def github(name, *args)
  options ||= if args.last.is_a? Hash
    args.last
  else
    {}
  end

  if path = options.delete(:path)
    mod name, :path => path
  else
    version = args.first
    options[:repo] ||= "boxen/puppet-#{name}"
    mod name, version, :github_tarball => options[:repo]
  end
end

# Shortcut for a module under development
def dev(name, *args)
  mod name, :path => "#{ENV['HOME']}/src/boxen/puppet-#{name}"
end

# Includes many of our custom types and providers, as well as global
# config. Required.

github "boxen", "3.3.4"

# Core modules for a basic development environment. You can replace
# some/most of these if you want, but it's not recommended.

github "dnsmasq",    "1.0.0"
github "foreman",    "1.0.0"
github "gcc",        "2.0.1"
github "git",        "1.2.5"
github "go",         "1.0.0"
github "homebrew",   "1.5.1"
github "hub",        "1.0.3"
github "inifile",    "1.0.0", :repo => "puppetlabs/puppetlabs-inifile"
github "nginx",      "1.4.2"
github "nodejs",     "3.3.0"
github "openssl",    "1.0.0"
github "phantomjs",  "2.0.2"
github "pkgconfig",  "1.0.0"
github "repository", "2.2.0"
github "ruby",       "6.7.2"
github "stdlib",     "4.1.0", :repo => "puppetlabs/puppetlabs-stdlib"
github "sudo",       "1.0.0"
github "xquartz",    "1.1.0"

# Optional/custom modules. There are tons available at
# https://github.com/boxen.

#github "chrome", "1.1.2"
github "firefox", "1.1.7"
github "gimp", "1.0.0"
github "heroku", "2.1.1"
github "imagemagick", "1.2.1"
github "java", "1.2.0"
github "memcached", "1.4.0"
github "mongodb", "1.2.0"
github "mysql", "1.2.0"
github "openssl", "1.0.0"
github "osx", "2.2.2"
github "redis", "2.1.0"
github "rubymine", "1.1.0"
github "skype", "1.0.8"
github "wget", "1.0.0"
github "wkhtmltopdf", "1.2.1"
github "zsh", "1.0.0"
github "qt", "1.2.0"
github "sublime_text_2", "1.1.2"
github "vagrant", "3.0.3"
github "virtualbox", "1.0.10"
github "ohmyzsh", "1.0.0", :repo => "samjsharpe/puppet-ohmyzsh"
