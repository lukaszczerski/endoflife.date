---
title: Amazon EKS
layout: post
category: service
sortReleasesBy: "releaseCycle"
changelogTemplate: "https://docs.aws.amazon.com/eks/latest/userguide/kubernetes-versions.html#kubernetes-__RELEASE_CYCLE__"

releases:
  - releaseCycle: "1.21"
    eol: 2022-09-01
    release: 2021-07-19
    latest: "1.21.2"
  - releaseCycle: "1.20"
    eol: 2022-06-01
    release: 2021-05-18
    latest: "1.20.7"
  - releaseCycle: "1.19"
    eol: 2022-04-01
    release: 2021-02-16
    latest: "1.19.8"
  - releaseCycle: "1.18"
    eol: 2022-02-18
    release: 2020-10-13
    latest: "1.18.16"
  - releaseCycle: "1.17"
    eol: 2021-11-02
    release: 2020-07-10
    latest: "1.17.17"
  - releaseCycle: "1.16"
    eol: 2021-09-27
    release: 2020-04-30
    latest: "1.16.15"

iconSlug: kubernetes

permalink: /amazon-eks
alternate_urls:
  - /eks
  - /amazon-eks
  - /amazon-elastic-kubernetes-service
link: https://docs.aws.amazon.com/eks/latest/userguide/kubernetes-versions.html
activeSupportColumn: false
releaseColumn: true
releaseDateColumn: true
eolColumn: End of Support
command: eksctl get cluster --name=cluster-name
---
> [Amazon Elastic Kubernetes Service (Amazon EKS)](http://aws.amazon.com/eks/) is a managed service that you can use to run Kubernetes on AWS without needing to install, operate, and maintain your own Kubernetes control plane or nodes. EKS runs upstream Kubernetes and is certified Kubernetes conformant for a predictable experience.

Amazon EKS guarantees support for at least four production-ready versions of Kubernetes at any given time. A Kubernetes version is fully supported on EKS for 14 months after first being available on Amazon EKS. This is true even if upstream Kubernetes is no longer supporting a version available on Amazon EKS.

You can subscribe to upgrade notices (sent approximately 12 months after the Kubernetes version was released on Amazon EKS) on your [Personal Health Dashboard](https://aws.amazon.com/premiumsupport/technology/personal-health-dashboard/). The notice includes the end of support date, which is at least 60 days from the date of the notice.

## Upgrading

Amazon EKS will automatically upgrade existing control planes (not nodes) to the oldest supported version through a gradual deployment process after the end of support date. After the automatic control plane update, you _must [manually update cluster add-ons and Amazon EC2 nodes][upgrade]_. Amazon EKS does not allow control planes to stay on a version that has reached end of support.

Because Amazon EKS runs a highly available control plane, you can update only [one minor version at a time][skew]. Therefore, if your current version is 1.19, and you want to update to 1.21, then you must first update your cluster to 1.20 and then update it from 1.20 to 1.21. Similarly, your node version can be at most 2 minor version behind the control plane version.

[upgrade]: https://docs.aws.amazon.com/eks/latest/userguide/update-cluster.html#update-existing-cluster
[skew]: https://kubernetes.io/docs/setup/version-skew-policy/#kube-apiserver
