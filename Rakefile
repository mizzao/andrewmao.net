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
    :allow_hash_href => true,       # don't break on <a href="#">
    :assume_extension => false,     # (true) for extensionless paths
    :http_status_ignore => [
      999, # LinkedIn throttling errors
      403, # Google scholar errors thrown from Travis (links here will be public anyway)
    ],
    :typhoeus => {
      :connecttimeout => 20,
      :timeout => 60,
      # avoid strange SSL errors: https://github.com/gjtorikian/html-proofer/issues/376
      :ssl_verifypeer => false,
      :ssl_verifyhost => 0
    }
  }
  HTMLProofer.check_directory("./_site", options).run
end

task :test do
  build_site
  doctor_site
  html_proofer
end

task :test_local do
  # Already built so don't build again
  doctor_site
  html_proofer
end

task :default => :test
