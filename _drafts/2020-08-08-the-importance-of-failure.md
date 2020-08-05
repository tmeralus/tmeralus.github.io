---
layout: post
title: "The Importance of Failure"
date: 2020-08-08
excerpt: "CCDA Validator and interview tests"
tags:
---
## There are many lessons in defeat,
https://www.wanderlustworker.com/the-importance-of-failure-5-valuable-lessons-from-failing/

An important lesson in failing is knowledge. Knowledge of self, knowledge of the past, and knowledge of the present, is what shapes the future. This COVID-19 pandemic has shifted my life in more ways than one. Losing my job, family, and faith in myself has definitely shaken up this year like a hurricane. In the midst of job hunting I have come across what some people would call a catch 22 (a dilemma or difficult circumstance from which there is no escape because of mutually conflicting or dependent conditions). [My resume](https://www.linkedin.com/in/tmeralus/) can be previewed on my Linkedin profile. I have a variety of skills in tech and experience as a system administrator and Linux administrator. I have certifications, which for some have value and help bypass HR "firewalls" (as I like to call them) and enough experience on paper to prove my worth and my talent as a Linux administrator. Due to the effects of COVID the travel software company I was working for had to cut 90% of the staff, me included. With the world going remote there are plenty of tech related jobs right now looking for senior level administrators who can jump into a remote based position and do some heavy lifting.

If i'm being honest with myself I'm a strong administrator, skilled technician, passionate and adaptable worker, but a senior level admin, may not be a title I would want to stitch onto my career vest just yet. I only believe this to be true because when I think of senior level talent I think of IT directors, admins with gray beards that go down to their belly buttons, and people who can build and manage infrastructure from memory. That may sound far-fetched to some but that is a level i'm looking to get to. Am I good at what I do? Yes! Am I able to resolve issues quickly or draft up solutions for meetings quickly? Yes! Am I good at taking tests without sweating and dealing with test anxiety? Nope!

With that being said I have come across a vast amount of recruiters who love my resume and pass it to businesses and interviewers who love my attitude and push me to the next round. Each of them come back multiple times with "It was a hard decision between you and someone else, but they decided to go the other way" or "They really liked you but they are looking for someone with more experience", or "We think that your great but we are looking for someone who has more experience with X".

Getting back to back rejections can definitely humble you. The problem with these chinks in my armor is not related to a catch 22 however. I'm a firm believer that every moment in life is a learning experience so I treat this as such. With one of the jobs that passed on me they introduced me to a github project that they wanted me to setup within a specific time frame while they watched. I wasn't able to get the tomcat application up in time due to some tricky wording in the documentation, however, I did decided to take it upon myself to not only finish setting up the application but setup a jenkins build project to check and keep the application up to date. I figured this will showcase my skills in Linux, Jenkins freestyle projects, docker configurations, git, CI/CD, devops tools, and then some. That way, if I run into another interviewer who asks me more about my skills and my talents I have something to show and explain with documentation.

# CCDA Validator Challenge
The job rejection triggered the CCDA Validator docker file.

Description: CCDA provides capabilities to validate your CCDAapplicable standards-specifications.

Interview Skills Challenge: Build out the CCDA validator on a given web server
Interview Error: My goal in the challenge was to complete the task in teh quickest way possible. Not taking my time and giving myself less time than the allotted time given caused more stress for me which prevented me from


Solution: A jenkins build for a CCDA docker container
Link: https://github.com/onc-healthit/reference-ccda-validator

Dockerhub:
Pull Request:
Setup:


# Apache GeoIP Challenge 

Issue: An application monitor is needed to view apache web servers and check where connections are coming from.
Possible Solution: [Grafana NGINX GeoIP dashboard](https://grafana.com/grafana/dashboards/8342)
Problem: This dashboard works great with NGINX, but company A uses apache and needs something that works with apache.

Jenkins Build Setup:
