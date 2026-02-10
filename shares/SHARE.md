---
title: "Using `pnpm` with miniflare v3+ causes issues with @vites/utils exports not being resolved"
slug: using-pnpm-with-miniflare-v3-causes-issues-with-vitesutils-expor
tags: ["pnpm", "npm", "workerd", "cloudflare"]
problem: "Exported symbols from @vitest/utils are note resolved from within the `workerd` runtime when using `pnpm`"
solution_type: workaround
created: 2026-02-10
---

## Problem

Exported symbols from @vitest/utils are note resolved from within the `workerd` runtime when using `pnpm`

## Solution

Use `npm` instead of `pnpm`.

## Why It Works

`pnpm` has stricter module resolution, which does not seem to work with `workerd`

## Context

- miniflare v3+
