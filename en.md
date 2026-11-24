---
title: Kage Arena privacy policy
---

# Kage Arena privacy policy

[Versão em português](./)

**Last updated:** November 24, 2026

The Portuguese version is the reference text; this is a translation.

## Summary

- Kage Arena **does not collect** your name, email, Steam account or IP address.
- When the game hits an error or crashes, it sends an **error report** so the problem can be fixed, both in the downloadable version and in the browser version. At the end of each online match, it also sends a summary of the connection quality, numbers only. You can turn this off in **Options > Game > Error reports**.
- After each **online** round on one of the game's stages, it sends **how long the round lasted and how many were playing**, and, if you vote during the round replay, **whether you liked the stage**. It goes with a random number for your installation, with nothing that identifies you. You can turn this off in **Options > Game > Stage votes and stats**.
- In **online play**, the computers in a room connect directly, so players in a room see each other's IP address. The game does not keep anything about them.

## Who is responsible

Kage Arena is developed by **Lucas Humberto**, an individual, who is the controller of the data described here (Brazilian General Data Protection Law, Law 13.709/2018, and, for players in the European Union, the General Data Protection Regulation).

**Contact for questions and requests:** lukas489@gmail.com

## 1. What the game does not collect

The game has no sign-up and does not collect your name, email, Steam account or username, IP address, location, contacts, screen recordings, or anything you type outside the game. The only exceptions are the IP address that online play needs to connect (section 3) and the one the votes service sees when it receives data (section 4), which the game does not keep. There are no ads, no advertising tracking and no sale of data.

## 2. Error reports

**When:** in the downloadable version (Windows, through Steam or itch.io) and in the browser version (itch.io), when the game hits an error, crashes, or has a problem in online play (lost sync, a room that drops, failing to join a room, a match that fails to start, a long wait for another player). Also, at the end of each online match, a summary of the connection quality: ping, network corrections, waits, packet size, number of bots and rounds, and how the match ended. Other than that, the game sends nothing when it starts or while everything works.

**What a report contains:**

| Data | Why |
| --- | --- |
| The error message and the place in the code where it happened | Find and fix the bug |
| The game version | Know which version has the problem |
| What was happening in the game (screen or mode, online steps before the error, ping and whether the connection is direct or relayed) | Reproduce the problem |
| Operating system, processor, graphics card, memory, screen resolution, language and time zone (in the browser version, the browser and operating system, from the identification every browser sends) | Problems that only happen on some computers |
| For severe crashes of the program (downloadable version only), a copy of part of the game's memory at the moment of the crash | Understand crashes that leave no error message |

**What it does not contain:** name, email, Steam account, IP address, location, computer name, system user name (it is cut from folder paths before sending), the page the game was opened from.

**Legal basis:** legitimate interest in keeping the game working and fixing bugs (LGPD, art. 7, IX; GDPR, art. 6(1)(f)). Only the minimum data for that is used, and you can opt out at any time.

**Who receives it:** reports are processed by the **Sentry** service (Functional Software, Inc.), in the **United States**, acting as processor under a data processing agreement (DPA) that covers international transfers through the Data Privacy Framework and, where it does not apply, standard contractual clauses. Sentry is configured not to store IP addresses.

**How long:** up to 90 days. After that, reports are deleted.

**How to turn it off:** in **Options > Game > Error reports**. When off, the game stops sending immediately. The choice is saved on your computer (in the browser version, in the browser's storage).

## 3. Online play

Online play connects the computers in a room directly to each other (WebRTC technology), with no game server in the middle. To do this:

- **The other players in the room receive your computer's IP address**, as in almost every online game without a central server. This is how the computers find each other and exchange the match inputs.
- To find a room by its code, the game uses the public **PeerJS** signaling server, which receives the room code and the IP address of whoever creates or joins it. To find the direct path, it uses **Google's STUN** servers, which also see the IP address.
- When a direct connection is not possible, the match goes through a **Cloudflare** relay (TURN), which sees the IP address and the match traffic (only the game inputs, encrypted by WebRTC itself).
- **Room list:** whoever creates a room can keep it in the public list (on by default; turn it off with "In the room list" inside the room). While the room is waiting for players (or, during a match, while it has a bot whose place someone can take), a game service on **Cloudflare** shows people looking for rooms the creator's nickname, the mode, how many slots are taken, the room code, whether it has a password (only that: the password never leaves the room creator's machine) and the approximate continent. The continent and an approximate position (city) come from the connection itself, worked out by Cloudflare; the position is only used to estimate the ping and is never shown to anyone. The service does not store the IP address: it keeps only a digest of it (hash) to limit how many rooms each connection creates. Everything stays in memory only and is gone within 45 seconds after the room leaves the list, the match starts or the room closes. People who only look for rooms send just the game version.
- **Looking at a room before joining:** when you pick a room from the list, the game connects directly to the room creator's computer, without taking a slot, and shows what it sends: the nicknames of the people in the room, each one's ping to the creator, the mode, the rounds, the biome, the variants and whether the match has started. As with every online connection in the game, both computers see each other's IP address. None of this is kept, and the connection ends when you leave that screen.
- In a room, whoever created it is shown by the room code and the others by a random nickname. The game does not use any Steam name or account for online play.
- Kage Arena does not keep any of this data. Each service follows its own privacy policy.

## 4. Stage votes and stats

**When:** only in online play, at the end of each round played on one of the game's own stages (not maps you make in the editor); and when you vote during the round replay (↑ liked it, ↓ did not). The data is sent together when the round changes.

**What is sent:**

| Data | Why |
| --- | --- |
| The stage name and a summary (hash) of its layout, to tell versions apart when the stage is edited | Know which stage and which version it is |
| How long the round lasted, how many were playing, how many people (not counting bots) and whether it was online | See which stages work: rounds too short, too long, stages nobody plays |
| Your vote on that stage version (one only; voting again replaces it) | Know whether the stage is liked |
| The game version | Compare before and after a change |
| A random number created the first time (the installation identifier), with a signature from the service | Count one vote per installation and make fake votes harder |

**What is not sent:** name, nickname, email, Steam account, nothing about your computer.

**IP address:** the service sees the connection's IP address, like any website. It does not keep it: when the installation asks for its number, only a summary of the IP made with a secret that changes every day is kept, to limit how many new installations each connection creates, and that summary is deleted the next day.

**Legal basis:** legitimate interest in improving the game's stages (LGPD, art. 7, IX; GDPR, art. 6(1)(f)). The data identifies no one and you can refuse at any time.

**Who receives it:** a game service on **Cloudflare** (Workers and the D1 database), acting as processor. Only the developer reads the numbers.

**How long:** while the game is in development, to compare stage versions. You can ask for your installation's data to be deleted at the email above.

**How to turn it off:** in **Options > Game > Stage votes and stats**. When off, the game stops sending right away.

## 5. Data that stays on your computer

Settings (language, volume, controls), editor maps, the votes you cast and your error report choice are saved on your computer and are not sent anywhere.

## 6. Children and teenagers

The game does not collect data that identifies players of any age. Error reports contain no personal information.

## 7. Your rights

You can request confirmation of processing, access, correction, deletion, information about sharing and review of decisions, and you can object to processing (LGPD, art. 18; GDPR, arts. 15 to 21), using the email above. Because reports have no name or account, finding a report of yours may require the approximate date and time and the game version. You can also complain to Brazil's National Data Protection Authority (ANPD) or to the data protection authority of your country.

## 8. Security

Reports travel encrypted (HTTPS) and only the developer has access to the account where they are kept.

## 9. Changes to this policy

When this policy changes, the date at the top changes too. The version history is kept in this repository.
