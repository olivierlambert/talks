class: center, middle

# Xen and Docker

## Uniting best of both worlds

![](assets/homepage-docker-logo.png)
---

# Agenda

1. Introduction
1. Definitions
1. Xen Objectives
1. Docker Objectives

---

# Introduction

---

# Abstract

Containers and hypervisors are different technologies. And also they lead to different usage, sometimes contradictory: Xen is a powerful hypervisor, allowing SysAdmins to build strong IT infrastructures, with security, control, resources isolation and flexibility. Docker is a container project bringing simplicity and universality for developers to build, test and ship their applications without thinking of what’s behind it. That’s why if you let everyone create Docker containers on your whole infrastructure, it will surely wreak havoc: CPU, RAM, network or disk usage without limits could lead to very serious problems. This talk will cover how developers can benefit from the flexibility containers provide, while avoiding potential shortcomings. By uniting Linux container and hypervisor technology, developers can get the best of both worlds and answer today’s cloud computing challenges.

---

# Ideas

* history of Xen, context, purpose, ideas
* Docker tales : context, initial purpose, ideas

Clash? Devops

Intro : tout ce que tu dis sera soumis à validation par toi avant publication.


Questions :



* ptite histoire de comment t'es arrivé chez Docker ?

10/11 ans d'herbegement Xen + associé, pas rendu riche
VOIP, Web agency, etc.

Solmon Hykes rencontré pendant ces périgrinations

DotCloud : fourni des VM 2008 avec noyau custom pour eux
2010 : Californie, bosser sur DotCloud hosting et dev, automatisation

EC2, monitoring, capacity planning
2012 apogée DotCloud : dirige équipe Ops

Fin 2012 : refactoring DotCloud Début 2013

Pivot sur Docker

Début 2013 fin 2013 : fin dotcloud

Début 2014 : talk Docker

Mi 2014 : full time evengelist Docker


Études dev + taff dans l'ops
50% dev 50% ops


* profil sysadmin, comprendre pourquoi ça réagit sceptiquement à Docker
* quel contexte est né Docker ? petite histoire rapidement

automatisation DotCloud

Proto Docker 2008 basé sur OpenVZ
LXC super bas niveau, super ! Mais rien au dessus.

Haute densité, truc qui démarre vite, métriques, sécurité

Idée prendre des VM chez Jerome

* quel était l'objectif à l'origine ?

déployer vite dans l'hébergement
moins cher plus économe
client veut wordpress : paf en deux secs, provisionner vite

pour les devs : instance environnement de devs, sandbox

* objectif aujourd'hui ?

virtu : plus de problématique bas niveau
Docker : simplifier encore plus, découper les problemes, déployer du code

plus de question des logs,

Donner des moyens d'innovation aux devs

* avantages principaux today
* relation avec hyperviseurs ? comment perçu chez vous ?


Container ET VM
* présentation rapide de l'écosystème (très grandes lignes)
* features qui manquent vs XenServer ? migration à chaud sans stockage ? est-ce que ça a un sens ?
* intégration avec XO, Docker machine / Drivers ?

* Avenir de Docker ?


Docker experience dev = un peu nawak

1st phase : one app dev, docker+compose en LOCAL
2nd phase : horizontal + appli + workflow
3rd phase : integration continue

1 an -> devs

ops -> prise en main

OBJECTIF PRINCIPAL = pour les devs, la prod moins objectif

Slide docker pour les sysadmins

pas de mise en prod direct

Vision devs à l'arrach ou ops aveugle => jour au lendemain fait accompli


viz resources ressources et logs

vendre docker a des ops

containers metrics = sysdig http://www.sysdig.org/
faire ressortir metriques via API

carte infrastructure : tel conteneur sur tel hote, carte a plat
