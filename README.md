# Talos-Kubernetes on OpenStack with Octavia Loadbalancer

## Overview

I deployed a Talos Kubernetes cluster (2 control plane nodes, 3 worker nodes) on OpenStack. I attached them to Octavia Loadbalancer which lets other devices in my Home network open the Nginx Sample App.

<p align="center">
  <img width="80%" height="80%" src="https://github.com/famasboy888/Talos_K8s_OpenStack_Loadbalancer/assets/23441168/21fa47ed-0078-4993-bb77-05d795fcc704">
</p>

<hr>

# My OpenStack Setup

## Talos terminal and my OpenStack Dashboard
It took a looooong time to boot up a single Talos Instance.
- 2 Control Plane Nodes
- 3 Worker Nodes
- 1 Remote Instance

<p align="center">
  <img width="80%" height="80%" src="https://github.com/famasboy888/Talos_K8s_OpenStack_Loadbalancer/assets/23441168/21fa47ed-0078-4993-bb77-05d795fcc704">
</p>

## My Octavia Load Balancer using `ROUND ROBIN` algorithm

<p align="center">
  <img width="80%" height="80%" src="https://github.com/famasboy888/Talos_K8s_OpenStack_Loadbalancer/assets/23441168/21fa47ed-0078-4993-bb77-05d795fcc704">
</p>

## See Load Balancing in action with a simple NGINX
You are probably wondering: Why the contents of the page changing and what is going on?
Well, we are just testing to see if the Load Balancing is working. So, to see load balancing in action, I changed each content to say which worker node it is from.
Of course, in the real world scenario we won't be changing the contents. Each pod should be identical to each other. Otherwise, they would say our web app is odd.
Yes, I'm pressing `F5` really fast coz I didn't have a script to auto refresh the browser.
