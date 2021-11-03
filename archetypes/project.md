---
title: "{{ replace .Name "-" " " | title }}"
date: {{ .Date }}
# weight: 1
# aliases: ["/first"]
# tags: ["first"]
author: {{ .Site.Params.Author }}
# author: ["Me", "You"] # multiple authors
draft: false
hidemeta: true
hideSummary: true
ShowReadingTime: false
ShowBreadCrumbs: true
ShowPostNavLinks: false
# cover:
#     hidden: false
#     image: "<image path/url>" # image path/url
#     alt: "<alt text>" # alt text
#     caption: "<text>" # display caption under cover
#     relative: false # when using page bundles set this to true
---
