task default: [ "build" ]

task build: [ "index.html", "style.css" ]


file "index.html" => "index.haml" do |t|
  `haml #{t.prerequisites[0]} #{t.name}`
end

file "style.css" => "style.scss" do |t|
  `sass #{t.prerequisites[0]} #{t.name}`
end
