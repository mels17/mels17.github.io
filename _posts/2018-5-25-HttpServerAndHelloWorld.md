---
layout: post
title: HTTP Server and Hello World Deployment
---

The focus of Hello World was to learn about Continuous Integration and Continuous Deployment, not the implementation. It was about building a simple RESTful API to display messages according to the client requests. There was lot of Amazon documentation I had to get around and CI/CD was new to me. So, this is the flow I understand, ```Make changes to code -> push to github -> Travis pulls the code -> runs tests on it -> uploads the solution to S3 bucket -> Code Deploy tranfers the code to the Amazon EC2 instance in the Tomcat webapps folder```. Tomcat then runs the application on the specified port.

When implementing this, I did not use build frameworks like Gradle or Maven, because it never crossed my mind. However, for the application to be build by Travis it need a build file. So, I did a quick-fix, I auto-generated a Ant build file, a feature that IntelliJ offers. Also, MYOB uses Buildkite instead of Travis, but at the time I was doing this, I did not have the permissions to use Buildkite, so I had to do with using Travis. But others who have used Buildkite, says it's much easier to use than Travis. I understood CI/CD is really useful, if you have tests on the pipeline, when you change a piece of your code, you just need to push the code to Github and the pipeline will do the rest.

HTTP server marks the end of the roadmap of the acceleration stage. You need to create a http server from scratch in Java using sockets, without using any outside frameworks. Truth be told, I didn't know how servers work. I always took advantage of the HTTP libraries and starting up a server was just a couple of lines and done!

I started implementing a multi-threaded server using sockets and a threadpool allowing upto 10 client threads at a time and a simple get request handler. Then I setup my server to be tested against the cob-spec tests; these are a list of tests that a basic http server should pass. So, implementing this server involved a TDD approach; red, green and refactor. But, I wanted to go out of the way and not refactor until the very end, so I could see how patterns develop. 

The hardest of the cob-spec tests, were getting the partial content - displaying a part of the file, and image content - sending an image as the response. Tried a lot of different ways until I cracked it! The cob-spec tests introduced concepts that I was not aware of before, but sometimes it was not clearly documented what was the expectation.
