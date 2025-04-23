---
title: "ScegliMeglio - A Polling System"
excerpt: "Online polling system for collecting voters' preferences developed in Python and Flask following SCRUM methodology."
collection: portfolio
---

## Overview

A web application is required that allows users to define multiple-choice polls and collect voters' preferences.

## Features

### User Management

- Users must be able to **register** and have a **personal space** to manage their polls.

### Poll Management

- Polls must be able to be:
  - **Created**
  - **Started**
  - **Closed**
  - **Deleted**
- Results must be **viewable** and **downloadable in CSV format**.

### User Interface

- The interface must be **responsive** (mobile and desktop-friendly).

### Voter Access

- Voters must be able to **express their preferences** by accessing the poll through a **link or code**.
- Voters must have access to a **private area** where they can view:
  - All polls they can participate in
  - All polls they have already participated in

## Types of Polls

Polls must support three types:

1. **Single-Choice Preference**
   - Voters choose only one option.
   - The final order of options is determined by the total number of individual preferences.

2. **Schulze Method**
   - Voters rank the options in order of preference.

3. **Majority Judgment Method**
   - Voters rate each option on a **5 or 7-point scale**, from *Excellent* to *Terrible*.

## Development Methodology

The system is to be developed following the principles of the **SCRUM methodology**.

