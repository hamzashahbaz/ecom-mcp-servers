# ecom-mcp-servers

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**The definitive directory of official MCP servers for eCommerce brands and agencies.**

The [Model Context Protocol (MCP)](https://modelcontextprotocol.io) gives AI assistants direct access to your tools, platforms, and data. For eCommerce teams, this means your AI can pull real-time orders from Shopify, check shipping status in ShipStation, analyze campaign performance in Google Ads, and manage invoices in QuickBooks — all without leaving the conversation. This directory catalogs every **official, first-party** MCP server relevant to running an eCommerce business.

> **31 official MCP servers across 14 categories** — built and maintained by the platform companies themselves

---

## Table of Contents

- [What is MCP?](#what-is-mcp)
- [Quick Start](#quick-start)
- [Storefronts & Platforms](#storefronts--platforms)
- [Advertising](#advertising)
- [Email & SMS Marketing](#email--sms-marketing)
- [Analytics](#analytics)
- [Customer Support](#customer-support)
- [Shipping & Fulfillment](#shipping--fulfillment)
- [Payments](#payments)
- [Inventory & ERP](#inventory--erp)
- [CRM](#crm)
- [SEO](#seo)
- [Project Management](#project-management)
- [Design](#design)
- [Content & CMS](#content--cms)
- [Infrastructure](#infrastructure)
- [Summary](#summary)
- [Contributing](#contributing)

---

## What is MCP?

The **Model Context Protocol (MCP)** is an open standard that lets AI assistants connect to external tools and data sources through a unified interface. Instead of copying data between tabs or writing one-off API scripts, MCP servers expose capabilities that your AI assistant can call directly.

Think of it as a universal adapter between AI and your tech stack. One protocol, every tool.

Learn more at [modelcontextprotocol.io](https://modelcontextprotocol.io).

---

## Quick Start

To connect an MCP server to Claude Desktop, add it to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "server-name": {
      "command": "npx",
      "args": ["-y", "@namespace/mcp-server-name"],
      "env": {
        "API_KEY": "your-api-key-here"
      }
    }
  }
}
```

Each server below includes its own setup instructions. Check the linked docs or repo for specifics.

---

## Storefronts & Platforms

### Shopify Dev MCP

> Search Shopify documentation, explore API schemas, and scaffold Shopify Functions from your AI assistant.

- **Built by:** Shopify
- **Links:** [Docs](https://shopify.dev/docs/apps/build/devmcp)
- **Auth:** None (runs locally)
- **Status:** Production

**Capabilities:**
- Search and retrieve Shopify developer documentation
- Explore GraphQL and REST API schemas
- Scaffold Shopify Functions and app extensions

---

### Shopify Storefront MCP

> Every Shopify store exposes `/api/mcp` — real-time access to product catalog, cart, checkout, and order tracking.

- **Built by:** Shopify
- **Links:** [Docs](https://shopify.dev/docs/apps/build/storefront-mcp)
- **Auth:** Built into every Shopify store
- **Status:** Production

**Capabilities:**
- Browse product catalog and collections in real time
- Manage cart and initiate checkout
- Track order status and fulfillment

---

### WooCommerce MCP

> Native MCP support in WooCommerce 10.3+ — manage orders, products, inventory, and analytics directly.

- **Built by:** Automattic
- **Links:** [GitHub](https://github.com/WordPress/mcp-adapter)
- **Auth:** JWT
- **Status:** Beta

**Capabilities:**
- Manage products, orders, and inventory
- Access store analytics and reporting
- Native integration with WordPress ecosystem

---

## Advertising

### Google Ads MCP

> Campaign data, performance analytics, keyword research, and ad management for Google Ads.

- **Built by:** Google
- **Links:** [GitHub](https://github.com/googleads/google-ads-mcp)
- **Auth:** OAuth2
- **Status:** Production

**Capabilities:**
- Retrieve campaign performance data and analytics
- Conduct keyword research and planning
- Manage ads, ad groups, and campaigns

---

### Amazon Ads MCP

> Campaign creation, performance reporting, account management, and billing for Amazon Advertising.

- **Built by:** Amazon
- **Links:** [Docs](https://advertising.amazon.com/API/docs/en-us/mcp/mcp-overview)
- **Auth:** Amazon Ads API credentials
- **Status:** Open Beta

**Capabilities:**
- Create and manage Sponsored Products, Brands, and Display campaigns
- Pull performance reports and analytics
- Account and billing management

---

## Email & SMS Marketing

### Klaviyo MCP

> Full Klaviyo platform access — profiles, lists, segments, campaigns, flows, events, metrics, and reporting.

- **Built by:** Klaviyo
- **Links:** [Docs](https://developers.klaviyo.com/en/docs/klaviyo_mcp_server)
- **Auth:** API Key (local) or OAuth (remote)
- **Status:** Production (GA since Aug 2025)

**Capabilities:**
- Manage profiles, lists, and segments
- Create and monitor campaigns and flows
- Track events, metrics, and reporting data

---

## Analytics

### Google Analytics MCP

> Property management, report generation, and audience analysis for Google Analytics 4.

- **Built by:** Google
- **Links:** [GitHub](https://github.com/googleanalytics/google-analytics-mcp)
- **Auth:** OAuth2
- **Status:** Production

**Capabilities:**
- Generate custom reports and data pulls
- Analyze audience demographics and behavior
- Manage GA4 properties and data streams

---

### Mixpanel MCP

> Event queries, funnel analysis, retention reports, and session replays from Mixpanel.

- **Built by:** Mixpanel
- **Links:** [Docs](https://docs.mixpanel.com/docs/features/mcp)
- **Auth:** Mixpanel credentials / OAuth
- **Status:** Production (hosted)

**Capabilities:**
- Query event data and run JQL queries
- Analyze funnels, retention, and user flows
- Access session replay data

---

### Triple Whale MCP

> eCommerce analytics — profit queries, revenue by country, and attribution data from Triple Whale.

- **Built by:** Triple Whale
- **Links:** [GitHub](https://github.com/Triple-Whale/mcp-server-triplewhale)
- **Auth:** API credentials
- **Status:** Production

**Capabilities:**
- Query profit and loss data
- Revenue breakdowns by country, channel, and product
- Attribution modeling and ROAS analysis

---

## Customer Support

### Intercom MCP

> Search conversations, retrieve contacts, and access metadata from Intercom.

- **Built by:** Intercom
- **Links:** [GitHub](https://github.com/intercom/intercom-mcp-server)
- **Auth:** OAuth or Bearer token
- **Status:** Production (US-hosted workspaces only)

**Capabilities:**
- Search and retrieve conversation history
- Access contact and company data
- Query metadata and custom attributes

---

## Shipping & Fulfillment

### ShipStation MCP

> Shipments, labels, rates, carriers, inventory, and warehouse management via ShipStation.

- **Built by:** ShipStation
- **Links:** [GitHub](https://github.com/shipstation/mcp-shipstation-api)
- **Auth:** API credentials
- **Status:** Production

**Capabilities:**
- Create shipments and purchase labels
- Compare carrier rates
- Manage inventory and warehouses

---

### ShipBob MCP

> Products, orders, inventory, fulfillment, returns, and reporting from ShipBob.

- **Built by:** ShipBob
- **Links:** [Docs](https://developer.shipbob.com/mcp-server)
- **Auth:** API credentials
- **Status:** Production

**Capabilities:**
- Manage products and inventory levels
- Track orders and fulfillment status
- Process returns and access reporting

---

### UPS MCP

> Rate quotes, label creation, package tracking, and freight management via UPS APIs.

- **Built by:** UPS
- **Links:** [GitHub](https://github.com/UPS-API/ups-mcp)
- **Auth:** API credentials
- **Status:** Production

**Capabilities:**
- Get real-time rate quotes and transit times
- Create shipping labels
- Track packages and manage freight shipments

---

## Payments

### Stripe MCP

> Customers, payments, refunds, and subscriptions — available as both remote (hosted) and local server.

- **Built by:** Stripe
- **Links:** [Docs](https://docs.stripe.com/mcp)
- **Auth:** OAuth (remote) or API Key (local)
- **Status:** Production

**Capabilities:**
- Manage customers, payments, and refunds
- Handle subscriptions and billing
- Access financial reports and payouts

---

### PayPal MCP

> Payment links, invoicing, and transaction management via PayPal.

- **Built by:** PayPal
- **Links:** [GitHub](https://github.com/paypal/paypal-mcp-server)
- **Auth:** PayPal login (remote) or API credentials (local)
- **Status:** Production

**Capabilities:**
- Create payment links and invoices
- Manage transactions and refunds
- Access account and balance data

---

### Square MCP

> Payments, catalog management, customers, and orders via Square.

- **Built by:** Square
- **Links:** [GitHub](https://github.com/square/square-mcp-server)
- **Auth:** OAuth
- **Status:** Production

**Capabilities:**
- Process payments and manage transactions
- Catalog and inventory management
- Customer and order management

---

## Inventory & ERP

### QuickBooks Online MCP

> Customers, estimates, bills, invoicing, and expense tracking for QuickBooks Online.

- **Built by:** Intuit
- **Links:** [GitHub](https://github.com/intuit/quickbooks-online-mcp-server)
- **Auth:** QuickBooks API credentials
- **Status:** Production

**Capabilities:**
- Manage customers, invoices, and estimates
- Track expenses and bills
- Access financial data and reports

---

### NetSuite MCP

> SuiteQL queries, inventory management, purchase orders, and sales data from Oracle NetSuite.

- **Built by:** Oracle
- **Links:** [Docs](https://www.netsuite.com/portal/products/artificial-intelligence-ai/mcp-server.shtml)
- **Auth:** OAuth 2.0 with PKCE
- **Status:** Production

**Capabilities:**
- Run SuiteQL queries against NetSuite data
- Manage inventory and purchase orders
- Access sales and financial data

---

## CRM

### HubSpot MCP

> Contacts, companies, deals, and engagement data from HubSpot CRM.

- **Built by:** HubSpot
- **Links:** [Docs](https://developers.hubspot.com/mcp)
- **Auth:** OAuth
- **Status:** Public Beta

**Capabilities:**
- Manage contacts, companies, and deals
- Access engagement and activity data
- CRM pipeline and reporting

---

### Salesforce MCP

> 60+ tools including Apex execution, SOQL queries, metadata management, code analysis, and org management.

- **Built by:** Salesforce
- **Links:** [GitHub](https://github.com/salesforcecli/mcp)
- **Auth:** Salesforce org credentials
- **Status:** Developer Preview

**Capabilities:**
- Execute Apex code and SOQL queries
- Manage metadata and org configuration
- Code analysis and deployment operations

---

## SEO

### Ahrefs MCP

> Backlink analysis, keyword research, site explorer, and competitive analysis from Ahrefs.

- **Built by:** Ahrefs
- **Links:** [Docs](https://docs.ahrefs.com/docs/mcp/reference/introduction)
- **Auth:** Ahrefs MCP key (remote preferred, local deprecated)
- **Status:** Production

**Capabilities:**
- Analyze backlink profiles and referring domains
- Keyword research and difficulty scoring
- Site explorer and competitive analysis

---

### Semrush MCP

> Domain analytics, keyword research, backlink analysis, and competitive intelligence from Semrush.

- **Built by:** Semrush
- **Links:** [Remote](https://mcp.semrush.com/v1/mcp)
- **Auth:** OAuth or API Key
- **Status:** Production

**Capabilities:**
- Domain analytics and traffic estimation
- Keyword research and gap analysis
- Backlink auditing and competitive intelligence

---

## Project Management

### Asana MCP

> Task management, project management, and workspace interaction for Asana.

- **Built by:** Asana
- **Links:** [Docs](https://developers.asana.com/docs/using-asanas-mcp-server)
- **Auth:** OAuth
- **Status:** Production

**Capabilities:**
- Create and manage tasks and subtasks
- Organize projects and sections
- Search and filter across workspaces

---

### Monday.com MCP

> Board management, item CRUD, and dynamic GraphQL API access for Monday.com.

- **Built by:** Monday.com
- **Links:** [GitHub](https://github.com/mondaycom/mcp)
- **Auth:** API token
- **Status:** Production

**Capabilities:**
- Manage boards, groups, and items
- Dynamic GraphQL query generation
- Column value management and updates

---

### Notion MCP

> Pages, databases, blocks, search, and comments for Notion workspaces.

- **Built by:** Notion
- **Links:** [GitHub](https://github.com/makenotion/notion-mcp-server)
- **Auth:** Integration token
- **Status:** Production

**Capabilities:**
- Create and manage pages and databases
- Block-level content operations
- Search across workspace and manage comments

---

## Design

### Figma MCP

> Design-to-code workflows, screenshots, metadata access, and Code Connect for Figma.

- **Built by:** Figma
- **Links:** [GitHub](https://github.com/figma/mcp-server-guide)
- **Auth:** Figma account
- **Status:** Production

**Capabilities:**
- Extract design data and screenshots for code generation
- Access component metadata and design tokens
- Code Connect for mapping components to codebase

---

### Canva MCP

> App development assistance and Connect API integration for the Canva platform.

- **Built by:** Canva
- **Links:** [Docs](https://www.canva.dev/docs/apps/mcp-server/)
- **Auth:** Canva developer account
- **Status:** Production

**Capabilities:**
- Canva app development guidance
- Connect API integration support
- Design asset and template access

---

## Content & CMS

### Contentful MCP

> Content CRUD, content type management, assets, publishing, and localization for Contentful.

- **Built by:** Contentful
- **Links:** [GitHub](https://github.com/contentful/contentful-mcp-server)
- **Auth:** Management API token
- **Status:** Production

**Capabilities:**
- Create, read, update, and publish content entries
- Manage content types and field schemas
- Asset management and multi-locale support

---

### Sanity MCP

> Schema-aware GROQ queries and document management for Sanity.

- **Built by:** Sanity
- **Links:** [Remote](https://mcp.sanity.io)
- **Auth:** Sanity project credentials
- **Status:** Production (remote hosted, local deprecated)

**Capabilities:**
- Schema-aware GROQ query generation
- Document CRUD operations
- Asset and reference management

---

### Prismic MCP

> Context-aware slice component guidance for Next.js, Nuxt, and SvelteKit projects using Prismic.

- **Built by:** Prismic
- **Links:** [GitHub](https://github.com/prismicio/prismic-mcp-server)
- **Auth:** Prismic project config
- **Status:** Production

**Capabilities:**
- Slice component development guidance
- Framework-specific code generation (Next.js, Nuxt, SvelteKit)
- Content modeling assistance

---

## Infrastructure

### AWS MCP

> Suite of specialized MCP servers for AWS services — compute, storage, databases, and more.

- **Built by:** AWS Labs
- **Links:** [GitHub](https://github.com/awslabs/mcp)
- **Auth:** AWS credentials
- **Status:** Production

**Capabilities:**
- Interact with AWS services (S3, Lambda, DynamoDB, etc.)
- Infrastructure management and querying
- CloudWatch logs and monitoring access

---

## Summary

| Metric | Count |
|--------|-------|
| **Total servers** | 31 |
| **Categories** | 14 |
| **All servers** | Official first-party only |

### Servers by Category

| Category | Count | Servers |
|----------|-------|---------|
| Storefronts & Platforms | 3 | Shopify Dev, Shopify Storefront, WooCommerce |
| Advertising | 2 | Google Ads, Amazon Ads |
| Email & SMS Marketing | 1 | Klaviyo |
| Analytics | 3 | Google Analytics, Mixpanel, Triple Whale |
| Customer Support | 1 | Intercom |
| Shipping & Fulfillment | 3 | ShipStation, ShipBob, UPS |
| Payments | 3 | Stripe, PayPal, Square |
| Inventory & ERP | 2 | QuickBooks Online, NetSuite |
| CRM | 2 | HubSpot, Salesforce |
| SEO | 2 | Ahrefs, Semrush |
| Project Management | 3 | Asana, Monday.com, Notion |
| Design | 2 | Figma, Canva |
| Content & CMS | 3 | Contentful, Sanity, Prismic |
| Infrastructure | 1 | AWS |

---

## Contributing

Know of an official MCP server we're missing? Spotted a broken link?

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines on submitting new entries. Only official, first-party MCP servers are included in this directory.

---

Maintained by **Hamza Shahbaz** / [Devturn](https://devturn.com)

If this directory saved you time, give it a star. It helps others find it.
