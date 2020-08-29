---
layout: post
title:  Paper Reading: Decentralized Trust Management
date:   2020-08-20 00:00:00
categories: jekyll update
author: John Dellaverson
---


We recently read the Paper 'Decentralized Trust Management' by Matt Blaze, Joan Feigenbaum, and Jack Lacy. To begin with a (very abridged and approximate) summary of the paper itself: the paper  was written in 1996, and is primarily concerned with making the argument that not only were then-current trust management systems (PGP, X.509) insufficient/poorly matched to the task of managing trust, but also that a better option would be to have the trust management credential (e.g. the certificate) hold all the information about whether or not an action can be taken. This in turn leads directly to authorization (or lack thereof). To this end, the paper outlined the PolicyMaker system, which implements the aforementioned option. To applications, the system appears to be a query engine on top of a database. The queries are of the form key1, key2, ... keyn REQUESTS ActionString. If the ActionString matches some filter (which, to a good approximation, can be either regular expressions or AWK programs) that was set up in PolicyMaker. In this way, PolicyMaker can authenticate requests like 'Bill for < $500 from Janice'. 

The most interesting part of this paper for our group is the comparison between PolicyMaker and NDN Trust Management solutions -- more specifically, between PolicyMaker and NDN Trust Schemas. We concluded that, though Trust Schemas provide additional flexibility compared to, say, X.509, PolicyMaker provides some additional granularity. PolicyMaker has the additional capability of designating allowed actions. One additional question we weren't satisfied with is how many of these actions (or what kind, broadly speaking) can be converted to name-based access control. 

The slides for the presentation can be found ["here"][slides].

[slides]: https://docs.google.com/presentation/d/1gnhZO04jh1FCXdCkpI1IBCBOaYXIuApQv7lrn6_C5SA/edit?usp=sharing