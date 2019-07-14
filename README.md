# all-in-one-build-image

[![Build Status](https://travis-ci.org/fabricepipart/all-in-one-build-image.svg?branch=master)](https://travis-ci.org/fabricepipart/all-in-one-build-image)
[![](https://images.microbadger.com/badges/image/fabricepipart/all-in-one-build-image.svg)](https://hub.docker.com/r/fabricepipart/all-in-one-build-image/tags "Get your own image badge on microbadger.com")

All my tools in one build image

## Setup of the Maven mirror
Please fill the variable MAVEN_MIRROR_URL

## To test locally

oc delete pod testit --ignore-not-found=true
oc run testit -it --image=docker-registry.default.svc:5000/ci/all-in-one:mvn36-jdk8-git-oc-py --image-pull-policy='Always' --restart=Never --command -- sh

## Inspiration

https://github.com/openshift/jenkins/blob/master/agent-maven-3.5/Dockerfile.localdev