---
title: Enhanced Prometheus Monitoring Integration for Enterprise Customers
description: Added flexible Prometheus scraping configuration to support enterprise monitoring setups that cannot use remote write approaches
date: 2025-08-18
tags: [monitoring, prometheus, enterprise, scraping]
---

# Enhanced Prometheus Monitoring Integration for Enterprise Customers

We've implemented a new Prometheus monitoring configuration specifically designed for enterprise customers who cannot utilize the standard remote write approach for metrics collection. This enhancement introduces support for a scraping-based architecture where BuildBuddy runs a lightweight Prometheus instance that retains metrics for a short duration (approximately 1 day) and exposes them for external scraping.

This configuration is particularly valuable for organizations with strict network policies or existing monitoring infrastructure that requires pull-based metrics collection rather than push-based remote write. The lightweight Prometheus instance acts as a bridge, collecting BuildBuddy metrics and making them available through standard Prometheus scraping endpoints without requiring long-term storage overhead on the BuildBuddy side.

The implementation enables enterprise customers to integrate BuildBuddy metrics into their existing Prometheus-based monitoring stack while maintaining their preferred data collection patterns and security requirements.