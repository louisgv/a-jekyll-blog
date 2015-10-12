---
layout: post
title: "jabSquared the Team"
date: "2015-10-11 11:19"
---

# Introduction

<!-- Who are jabSquared and the context of this conversation -->

jabSquared is a group of young entrepreneurs with a mission to transcend technology across culture. On the June of 2015, the team attended the AngelHack Hackathon and submitted Appointly, a B2C real-time appointment managing system for small businesses. With Appointly, jabSquared won the IBM's Bluemix grand prize of $120.000 in cloud credit.

After the hackathon, the team was left with a question: What to do with this sudden wealth of resource? The answer: a project every week. The purpose is to learn the tool as well as to attract potential client business.

<!-- Elaborate on the story of the question: what are we going to do with the credit we won. Every month a project, to learn the tool as well as to attract potential business. -->

# Progress

Since June, jabSquared has been utilizing Bluemix in most of their projects. Appointly was renamed to Cita (Appointment in Spanish), and was tailored for a local barbershop. The application used four of Bluemix's service: Cloud Foundry for backend hosting, Cloudant for real-time database, Mobile Push and Twillio for real-time end-user notification.

On August

Meteorite, jabSquared's landing page (http://jabSquared.ninja), is also hosted on BlueMix with Cloud Foundry.

Used IBM Bluemix on all four projects:
  Cita (previously Appointly),
  Meteorite - jabSquared's landing page,
  Unifiesta, and
  9 Billion.

Helped us in implementing a scalable ecosystem for each of our applications.

Never Stop Grinding

# Upcoming

Using Watson for pattern recognition

# End Notes

Young with huge potential. With the upcoming 120k packages, we will make services that scale to use up the resources, and make money. We hope to earn our money to use the service after this period is finished.

Why should BlueMix be recommended | is a great tool for beginner as well as intermediate:
  + Straight forward setup
    + From raw source or a git repo, importing project to IBM Bluemix is done with three cloudfoundry commands: `api`, `login`, `push`
    + Scaling is just another command line away
    + Built-in real-time logging system
  + Supports a variety of backend stack, including nodejs, go, ruby, etc...
  + Great services
    + Cloud Foundry
      + Painless Migration
      + Easily scalable
    + Cloudant
      + The PAIN Stack: PouchDB, Angular, Ionic and Nodejs
        + PouchDB is used to interact with Cloudant's CouchDB.
          + Cita for real-time appointment database
          + Unifiesta for raffle database
          + 9 Billion to store usage data
    + Twillio
      + Cita for Customer messaging
    + RedisLab
      + 9 Billion for realtime scalable countdown
    + Watson smart analytic:
      + A Slackbot that aggregate conversation
    + Built-in SSL for every services allowing for out-of-the-box security and privacy protection.
