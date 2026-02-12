---
title: Sample Project
description: This is a sample project to demonstrate the portfolio functionality
technologies:
  - Technology 1
  - Technology 2
github_url: https://github.com/rishabhd625/sample-project
---

## Overview

This is a sample project demonstrating how to add portfolio items to your Jekyll site.

## Features

- Feature 1
- Feature 2
- Feature 3

## Technologies Used

{% for tech in page.technologies %}
- {{ tech }}
{% endfor %}

## Links

{% if page.github_url %}
[View on GitHub]({{ page.github_url }})
{% endif %}
