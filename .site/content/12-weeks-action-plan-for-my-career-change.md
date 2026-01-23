+++
title = "12 Weeks Action Plan for my career change"
author = ["James"]
date = 2025-12-27T18:36:00+00:00
draft = false
+++

## Context {#context}

This plan is design with my current life circumstances in mind - working 20 hours and private life things. In addition to that, I have also taken into consideration related skills and experiences that I already process.

I will also be documenting my progress as well as what I learn throughout this project, if you're interested.

The progress and documentation is tracked in week numbers:

[Career change progress track](/career-change-progress-track/#week-4-and-going-forward)


## PHASE 1 - The Foundation and Certification {#phase-1-the-foundation-and-certification}

`WEEKS 1 - 5`


### Week 1: The Enterprise Linux Gap {#week-1-the-enterprise-linux-gap}

This is where I will be bridge the knowledge gap between personal Linux and enterprise Linux.

The goal is to have a local VM running a hardened web server ( SELinux Enforcing ).

-   [X] Install a RHEL-based distro ( Set up Rocky Linux or Fedora in a VM )
-   [ ] Master Package Management ( `dnf` or `rpm` instead of `pacman` )
-   [ ] Learn SELinux ( Learn how to check logs and `audit2allow` )
-   [ ] Learn `nmcli`
-   [ ] Firewall ( Learn `firewalld` )


### Week 2 - 4: Deep Dive ( SAA-C03 ) {#week-2-4-deep-dive--saa-c03}

-   [ ] CIDR Notation ( Subnet ranges )
-   [ ] DNS Debugging ( Master `dig` and `nslookup` )
-   [ ] HTTP Status Codes ( Memorise difference between 401/403 and 502/503 )
-   [ ] The Packet Journey ( Be able to explain what happens when you type an address into a browser, e.g. `growing.wiki` and `DNS` -&gt; `IP` -&gt; `TCP Handshake` -&gt; `TLS` -&gt; `HTTP` )
-   [ ] Content Consumption ( Adrian Cantrill's or Stephane Maarek's AWS SAA-C03 course. Focus on `VPC`, `S3`, `EC2` and `IAM` )
-   [ ] `VPC Networking` and `IAM` ( Most people struggle hardest with )


### Week 5:  AWS Certified Solutions Architect ( SAA-C03 ) {#week-5-aws-certified-solutions-architect--saa-c03}

-   [ ] Practice Exams ( TutorialsDojo practice exams )
-   [ ] Exam ( PASS IT )


## PHASE 2 - The "Literate DevOps" Portfolio {#phase-2-the-literate-devops-portfolio}

`WEEKS 6 - 9`

The goal here is to build two professional projects using org mode.


### Week 6: Tooling + "Skeleton" {#week-6-tooling-plus-skeleton}

-   [ ] Learn and set up LSP's ( `terraform-ls` and `docker-langserver` )
-   [ ] Set up Doom Emacs for writing code
-   [ ] Set up Terraform Remote State ( S3 bucket for state and DynamoDB for locking )


### Week 7: Project A ( Static Site Migration `ongoingarchive.com` ) {#week-7-project-a--static-site-migration-ongoingarchive-dot-com}

Don't just make it work, make it **secure**!

-   [ ] Architecture ( Migrate the site to `AWS S3` for storage and `CloudFront` for CDN )
-   [ ] Terraform ( Write a literate `org` file documenting both explanation and Terraform code, required resources: `aws_s3_bucket`, `aws_cloudfront_distribution`, `aws_route53_record` )
-   [ ] Security ( Implement Origin Access Control )


### Week 8: Project B ( Container Orchestration `growing.wiki` ) {#week-8-project-b--container-orchestration-growing-dot-wiki}

Build a secure **"Production"** environment.

-   [ ] Containerise ( Write a multi-stage `Dockerfile`, from build stage to runtime stage, to keep the image small using Alpine Linux )
-   [ ] Orchestrate ( Use Terraform to deploy this to `AWS ECS Fargate` )
    -   [ ] Create a `VPC` with Public/Private subnets
    -   [ ] Put the Application Load Balancer ( `ALB` ) in Public
    -   [ ] Put the Fargate Tasks ( Containers ) in Private
-   [ ] Outcome ( A URL that load balances traffic to the container )


### Week 9: CI/CD Automation {#week-9-ci-cd-automation}

Automate the deployment for Project A + B.

**This is where you transition from "someone who knows AWS" to "someone who works in DevOps".**

-   [ ] GitHub Actions ( Create a workflow for both projects )
    -   [ ] Project A: `git push -> sync to S3 -> invalidate CloudFront cache`
    -   [ ] Project B: `git push -> build Docker image -> push to AWS ECR -> force new ECS deployment`


## PHASE 3 - The Job Hunt {#phase-3-the-job-hunt}

`WEEKS 10 - 12`

Basically at this point, what's left will be to get interviews and land a role using my resume and portfolio.


### Week 9: Resume Engineering + Literate Documentation {#week-9-resume-engineering-plus-literate-documentation}

-   [ ] Retail Translation ( Rewrite retail experience to suit new career )
-   [ ] Tech Highlights ( Linux and Terraform skills )
-   [ ] Project Links ( Link my GitHub and projects )
-   [ ] Polish `.org` files ( Make READMEs look professional )


### Week 10: London Market Integration {#week-10-london-market-integration}

-   [ ] Agencies ( Register specifically with LinuxRecruit, Oho Group and Client Server, call and not just email )
-   [ ] Platforms ( Create profiles on Otta and Cord )
-   [ ] Meetups ( Attend London DevOps and/or Cloud Native London, socialise and network )


### Week 11-12: Interview Drill {#week-11-12-interview-drill}

-   [ ] Scenario Prep ( Practice answer question like "A server is high on CPU, how do you debug it?" `top`, `htop`, `pidstat`, check logs )
-   [ ] The "Arch" Question ( Be ready to answer questions like "Why Arch?" )
