desc "Deploy"
task :deploy do
	sh "git add --all"
  sh "git commit -am 'Updated blog content'"
  sh "git push origin master"
end

task :default => [:deploy]
