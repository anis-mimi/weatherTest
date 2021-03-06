---
title: Machine Learning Capabilities
date: 2018-9-24 17:00:00
category: Computer And Network
---

![](/images/4.jpg)


## Evaluate SDN and machine learning capabilities and trade-offs

SDN and equipment learning can combine to form knowledge-defined networking, which uses gathered data to manage network configuration. It's important, even so, to consider trade-offs.

In the study paper "Knowledge-Defined Networking," the authors describe three experiments that take telemetry...

<!-- more -->

info gathered from all of the nodes in a good network, process it working with machine learning, and utilize the resulting data to manage characteristics of network construction and forwarding via an SDN controller.

They call this technique of using elements of SDN and machine learning knowledge-defined networking.

On this page, let's consider the to begin these three experiments discussed in the study paper -- telemetry info gathered from network nodes -- in light of probable applications and issues in real-world systems. The experimental setup involves an underlay network with 19 underlay factors and 12 overlay nodes.

The figure below illustrates a simplified network similar to the one defined by the authors.

In this network, the machine described in the paper collects information at the C, D, K and N routers, including the delay across the underlay network of E, F, G and H. Neither the SDN controller (Q) nor the overlay network possesses any usage of the routing information or even the obtainable paths in the underlay network. Using the info gathered at the four overlay routers, nevertheless, the SDN controller uses equipment understanding how to infer the paths obtainable in the underlay network.

Using these details, the SDN controller can certainly try positioning different combinations of several flows on each offered path to determine which pieces of flows provide the best efficiency against a given set of factors. In the study paper, the shortest delay through the network is selected as the network optimization of fascination.

For example, if there are two flows from M toward B and one from P toward A, the controller will place both flows from M toward B on the two available links. The controller could work through the available paths at K, inserting the flows the following:

- the first flow on the road through H and the next flow on the road through G;
- the first flow on the path through G and the next flow on the road through H;
- both flows on the road through G; or
- both flows on the path through H.

In moving through the combinations, the SDN controller may use the instrumentation at the four overlay routers to determine which of the possible combinations offers a traffic pattern with the right delay through the network. This work provides what's perhaps one of the better available employ cases for SDN and equipment learning in network functions. The utilization case is definitely solvable at least in a trivial case, yet it is possible to picture a real-environment deployment of this sort of technology to solve specific problems.

No work of this kind, even so, is without its complications; if you haven't determined the tradeoff, then you haven't looked hard more than enough. It's important to look at the challenges this sort of work will probably face before it could be deployed in a meaningful method in large-scale fabrics.

## SDN and equipment learning tradeoffs

First, there can be an underlying assumption about the system's capability to measure at every edge of the overlay -- to take all of this data and derive meaning from it. But at scale, this is simply not as convenient a problem to solve as it might primarily seem. For instance, many hyperscale fabrics carry terabits of data each day. Collecting information upon this number of flows will be challenging. In fact, it's likely such something would need a high-speed control network just to carry the network telemetry. Processing this volume of details in near-real time so it pays to for adjusting the circulation of site visitors through the network will get difficult.

Second, lots of the flows found in a large-scale network will be mouse flows, or microflows. Various applications will create mouse and elephant flows with numerous attributes. Mouse flows are nearly always going to be also short-lived to usefully characterize on a per-request basis using any kind of machine learning. It really is tempting to classify all mouse flows as anything, but each application may do in a totally different approach and treat its mouse flows differently. This will probably be a difficult issue to solve.

Third, a large number of applications can run across an individual fabric, each with numerous requirements. These requirements should be expressed in ways the SDN controller will figure out. The process of collating and interpreting this information will be enormous in its right.

Fourth, the qualities of any request are likely to change as time passes. Machine learning must regularly be trained on new data pieces, but these data sets are altered by the use of older sets of guidelines. This interaction may create a condition where it is difficult to seriously understand the native movement of the site visitors through the network and hence to continue the training process.

Fifth, it really is difficult to see how network failures may easily be accounted for found in this sort of system.

Overall, that is interesting work, but SDN and equipment learning -- and artificial cleverness, generally speaking -- have many large hurdles to jump above before they'll be useful for solving wide problems in the network engineering environment.