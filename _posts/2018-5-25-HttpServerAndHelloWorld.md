---
layout: post
title: HTTP Server and Hello World Deployment
---

HTTP server marks the end of the roadmap of the acceleration stage. You need to create a http server from scratch in Java using sockets, without using any outside frameworks. Truth be told, I didn't know how servers work. I always took advantage of the HTTP libraries and starting up a server was just a couple of lines and done!

I started implementing a multi-threaded server using sockets and a threadpool allowing upto 10 client threads at a time and a simple get request handler. Then I setup my server to be tested against the cob-spec tests; these are a list of tests that a basic http server should pass. So, implementing this server involved a TDD approach; red, green and refactor. But, I wanted to go out of the way and not refactor until the very end, so I could see how patterns develop. 

The hardest of the cob-spec tests, were getting the partial content - displaying a part of the file, and image content - sending an image as the response. Tried a lot of different ways until I cracked it! The cob-spec tests introduced concepts that I was not aware of before, but sometimes it was not clearly documented what was the expectation.
