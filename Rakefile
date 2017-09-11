require 'html-proofer'

# See here for ideas: https://github.com/keegoid/keegoid.github.io/blob/master/Rakefile
def build_site
  sh "bundle exec jekyll build"
end

def doctor_site
  sh 'bundle exec jekyll doctor'
end

def html_proofer
  options = {
    :allow_hash_href => true,     # don't break on <a href="#">
    :assume_extension => false    # (true) for extensionless paths
  }
  HTMLProofer.check_directory("./_site", options).run
end

task :test do
  build_site
  doctor_site
  html_proofer
end

task :default => :test
