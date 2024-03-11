---
layout: post
title:  "Introduction to Microsoft systems administration"
date:   2023-12-15
featured_image: 2023-11-24-ccna/blog-thumbnail.png
tags: [Microsoft, Windows, Cloud]
---

The other day, while casually browsing Dealabs.com - a french website where you can find good deals on things posted by other users -, I came accross an offer for some free certifications.

*Free certifications ? I'm in.* Those were made by Microsoft in collaboration with LinkedIn Learning and covered multiple carreers path from administration to cybersecurity. First, I tried getting "Preparation for your sysadmin carreer".

<!--more-->

# The course

## Summary

This course was made by [Robert McMillen](https://www.linkedin.com/learning/instructos/robert-mcmillen), a contractor working for multiple clients including the American Government. He is a great teacher and make concepts easy to understand.

The course is made of multiple 3 to 7 minutes videos, adding up to almost 5h total. This might seem a lot but it is actually quite small considering you can start the course and get the final exam in the same afternoon (what I did). It is separated in multiple parts:

- 1. Install, Update & Maintain operating systems
- 2. Configure, manage, maintain & monitor servers
- 3. Focus on identity and authentication services
- 4. Initiation to networking
- 5. First steps with virtualization
- 6. Reviewing Cloud administration
- 7. Benefit from security and monitoring
- 8. Plan, monitor and secure backups
- 9. Starting out as a sysadmin

## What I learned

This course is almost exclusively focused on Microsoft ecosystem. Which is great, since I was very unfamiliar with it. I've only played around with Active Directory on premise, and I didn't go very far.

In order, I learned about:

> Active Directory & Azure Active Directory

The two ways of managing objects (users, devices, groups...) in a company made by Microsoft. They're actually quite similar, the only difference is that Active Directory is deployed on a server on premise, while Azure Active Directory is deployed in the Azure Cloud.

> Windows 10 & 11

We go through the process of installing Windows for the first time on a computer in some videos. Different parameters can be set at this stage, and it's important to know some of them to speed up deployement process.

> Endpoint Manager

Nowadays this tool is called Intune. It's a web panel were you can see and manage all devices, users, groups, in your AD Domain. For example, you can create a *Group Object Policy* and affect it to a group to force a certain parameter to each object of this group. This is very useful in a company for example, were you would want to give some access to certain departments, and restrecting others.

**But also:**

> vmWare, HyperV \ Windows Defender \ GPO \ MFA \ Shared Folders \ OSI \ IP Stack \ VLANs \ Azure & Cloud in general \ Backups solutions

Everything would be too long to go in detail, because this course is already really complete. In summary, it makes a great first approach to becoming a sysadmin. 

# The Exam

You have 90 minutes to complete a 30 questions exam. To pass, you have to get at least 70% right answers, but you also have 3 tries.

The exam is nothing more than a combination of all smaller tests you went trought during the course. There are questions about each and every module you saw, making it more or less global. 

# My thoughts

In conclusion, I really enjoyed taking this course. Robert is a great teacher and it is so complete that I really felt like we went over all Microsoft tools used by sysadmins. Even if I couldn't remember how to use everything, it is still a great improvement in my skills and learning path. For the awesome price of *0$*, I really think this was a great investment. And heck, it's certified by Microsoft, too ! 

Anyway I recommend everyone wanting to learn more about Microsoft & Microsoft system administration to take this course.

