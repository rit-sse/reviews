task default: [ "build" ]

task build: [ "index.html", "style.css", "se350/index.html" ]


file "index.html" => "index.haml" do |t|
  `haml #{t.prerequisites[0]} #{t.name}`
end

file "style.css" => "style.scss" do |t|
  `sass #{t.prerequisites[0]} #{t.name}`
end

file "se350/index.html" => "se350/index.haml" do |t|
  `haml #{t.prerequisites[0]} #{t.name}`
end


task :clean do |t|
  rm %W( index.html style.css )
end
