# Kobe's Homelab Setup Guide
[CML, GCP] Kobe's guide for setting up a homelab in the cloud.

UPDATED: December 8, 2024

For disclosure, I'm no expert in cloud or virtualization. I wanted to share my experience for setting up a homelab (using my Cisco Modelling Lab Personal Plus) via Google Cloud Platform. The guide is created due to lack of updated guides for setting up CML using GCP. The reason why I wanted to setup my homelab in the cloud is that CCIE Service Provider routers will require large RAM capacities in order for them to run properly. To save up for my CCIE SP exam, instead of purchasing a server (which will cost a ton aside from electricity consumption), I can just utilize the free $300 credit for 90 days provided by GCP to its users. My apologies if any of my terms are unclear or if I’ve stumbled along the way. Feel free to share any helpful or constructive feedback. Hopefully, this will be useful to you!

I’ve been trying to get Cisco CML 2.8.0 running in the cloud and, after a lot of trial and error, I think I’ve cracked it. I did find a guide on GitHub about setting it up on AWS using bare-metal EC2 instances, but after testing various setups, the cost didn’t make sense to me. AWS seems to only support nested virtualization if you use their bare-metal instances with specific processors that support it.

To save time, I checked out Azure and GCloud since both supposedly support nested virtualization. After digging deeper, GCP seemed like the better choice because its documentation and guides were easier to follow. The main selling point was a detailed article from Google that lays everything out. In short, GCloud supports Type I and Type II hypervisors, but Type I hypervisors need to run on a Linux-based OS and require a specific processor, which rules out E2 and N2D instance types.
