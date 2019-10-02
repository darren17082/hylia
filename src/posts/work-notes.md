---
title: My Work Notes
date: '2019-10-02'
tags:
  - demo-content
  - code
  - blog
---
# My Work Notes


## Mac Stadium

- MacStadium offers enterprise-scale Mac private clouds as well as individual dedicated Mac minis.
- Monday September 30 2019: Note from Joshua to Jonathan at Mac Stadium that he would like to make progress on the pricing discussion.
- Tuesday October 1 2019: reached out to Jonathan at ARM to schedule a call.


## ARM


- Arm research team has been using GitLab extensively for internal projects, please see couple of development scenarios in the attached slide. We plan to write a technical blog on this work which will be promoted during TechCon event.
- Arm is a big contributor/member of CNCF, the fluentd project from Arm Treasure Data. We partner strategically with Packet.com whose infrastructure is used for CNCF.CI projects which is based on GitLab.



From a product support standpoint, we are looking for three things (short-term to long-term):

- Official Arm 64-bit GitLab Runner (https://gitlab.com/gitlab-org/gitlab-runner/merge_requests/725).



## MR 725 Notes

- For MR 725 Thomas M. noted that there are 5 items needing to be resolved before the MR can be merged.
- This MR doesn't add building the Docker images for Runner.
- The arm/arm64 tags proposed in ci/release_docker_images are not consistent with the rest of tags that we're creating.
- Dockerfiles for arm are not consistent with x86_64 and arm64

### Work to be done

- We need to move up to Go 1.9+ 
- We need to update used Docker Machine version to something that is built with Go 1.9+ 
- We need to provide Git LFS and dumb-init binaries for both arm and arm64 architectures.
- We need to update ci/release_docker_images and the ubuntu/alpine Dockerfiles to make them consistent and to add the image buildings
- Since we recently added few changes in the Dockerfiles, the branch needs to be rebased on top of current
- "When we will upgrade from Go 1.8 and when we will provide missing binaries for Git LFS and dumb-init, changes from tm/feature/arm64-support-go1.9 should be enough to get this merged."


