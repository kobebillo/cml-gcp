# Kobe's Homelab Setup Guide
[CML, GCP] Kobe's guide for setting up a homelab in the cloud.

UPDATED: December 8, 2024

For disclosure, I'm no expert in cloud or virtualization. I wanted to share my experience for setting up a homelab (using my Cisco Modelling Lab Personal Plus) via Google Cloud Platform. I created this guide because there’s a lack of updated resources for setting up CML on GCP. The reason I chose to set up my homelab in the cloud is that CCIE Service Provider routers require large amounts of RAM to run properly. To save money for my CCIE SP exam, instead of purchasing a server (which would be expensive and add significant electricity costs), I decided to take advantage of GCP’s free $300 credit for 90 days.

Apologies if any of my terms are unclear or if I’ve made mistakes along the way. I welcome any helpful or constructive feedback. Hopefully, this will be useful to you!

I’ve been trying to get Cisco CML 2.8.0 running in the cloud and, after a lot of trial and error, I think I’ve cracked it. I did find a guide on GitHub about setting it up on AWS using bare-metal EC2 instances, but after testing various setups, the cost didn’t make sense to me. AWS seems to only support nested virtualization if you use their bare-metal instances with specific processors that support it.

To save time, I checked out Azure and GCloud since both supposedly support nested virtualization. After digging deeper, GCP seemed like the better choice because its documentation and guides were easier to follow. The main selling point was a detailed article from Google that lays everything out. In short, GCloud supports Type I and Type II hypervisors, but Type I hypervisors need to run on a Linux-based OS and require a specific processor, which rules out E2 and N2D instance types.

Visit this link for installing for installing [Free/Purchased] Cisco Modelling Lab: [link]
