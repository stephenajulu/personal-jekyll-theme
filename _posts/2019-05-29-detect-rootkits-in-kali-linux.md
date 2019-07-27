---
layout: post
title: Detect Rootkits In Kali Linux
date: 2019-05-29 22:22
author: ajulusthoughts
comments: true
categories: [Ajulu's Thoughts, chrootkit, kali, Kali linux, linux, mr. robot, rkhunter, rootkit, rootkits, TECH &amp; CYBERSECURITY, trojan, virus, viruses, worm, worms]
---
<!-- wp:heading -->
<h2>What is a Rootkit?</h2>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>A rootkit is a clandestine computer program designed to provide  continued privileged access to a computer while actively hiding its  presence. Rootkits are generally associated with malware – such as  Trojans, worms, viruses – that conceal their existence and actions from  users and other system processes.</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>You can see in this scene of Mr. Robot, that he tries to check for rootkits not knowing that it's his monitor being captured. (Don't Mind The Video's Title, Probably an average user who couldn't tell what was being done)</p>
<!-- /wp:paragraph -->

<!-- wp:core-embed/youtube {"url":"https://www.youtube.com/watch?v=Hvphe2QWraE","type":"rich","providerNameSlug":"","className":"wp-embed-aspect-16-9 wp-has-aspect-ratio"} -->
<figure class="wp-block-embed-youtube wp-block-embed is-type-rich wp-embed-aspect-16-9 wp-has-aspect-ratio"><div class="wp-block-embed__wrapper">
https://www.youtube.com/watch?v=Hvphe2QWraE
</div></figure>
<!-- /wp:core-embed/youtube -->

<!-- wp:heading {"level":3} -->
<h3>Rootkit Detection</h3>
<!-- /wp:heading -->

<!-- wp:heading {"level":4} -->
<h4><strong><span style="text-decoration:underline;">chkrootkit</span></strong></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Install : <strong>apt-get install chkrootkit</strong> (comes pre-installed)</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong><span style="text-decoration:underline;">Commands:</span></strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>chkrootkit -h</strong> : help menu</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>chkrootkit</strong> : starts the checking process</p>
<!-- /wp:paragraph -->

<!-- wp:heading {"level":4} -->
<h4><span style="text-decoration:underline;"><strong>rkhunter</strong></span></h4>
<!-- /wp:heading -->

<!-- wp:paragraph -->
<p>Install : <strong>apt-get install rkhunter</strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong><span style="text-decoration:underline;">Commands:</span></strong></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>rkhunter </strong>: help menu</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>rkhunter -c </strong>: checks local system</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p><strong>rkhunter –update</strong> : updates the rootkit database</p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p></p>
<!-- /wp:paragraph -->

<!-- wp:paragraph -->
<p>Source: <a href="https://hsploit.com/">Hackersploit</a></p>
<!-- /wp:paragraph -->
