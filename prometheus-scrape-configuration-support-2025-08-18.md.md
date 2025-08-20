---
title: Prometheus Scrape Configuration Support
description: Added support for Prometheus scrape-based monitoring to accommodate clients that cannot use remote write approaches, now offering a lightweight local Prometheus instance with 1-day data retention for metric collection.
date: 2025-08-18
tags: [monitoring, prometheus, metrics, scraping]
---

## Prometheus Scrape Configuration Support

We've implemented a new monitoring approach for clients who cannot use Prometheus remote write capabilities. The system now supports running a lightweight local Prometheus instance that retains only 1 day of metrics data, specifically designed to be scraped by external Prometheus systems.

This configuration enables organizations with network restrictions or existing scrape-based monitoring infrastructure to integrate with BuildBuddy's metrics without requiring remote write access. The minimal data retention keeps the local instance resource-efficient while providing the necessary metrics exposure endpoint for external collection systems.