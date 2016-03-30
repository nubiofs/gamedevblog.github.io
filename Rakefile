desc "Deploy"
task :deploy do
	sh "curl http://127.0.0.1:2368/rss/ > feed/index.xml"
	sh "curl http://127.0.0.1:2368/rss/ > rss/index.xml"
	sh "curl http://127.0.0.1:2368/rss/ > rss.xml"
	sh "git add --all"
	sh "git commit -am 'Updated blog content'"
	sh "git push origin master"
end

task :default => [:deploy]
