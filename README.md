# Vultr Hourly Billing Explained: How Does Per-Hour Pricing Work? Which Plan Is Cheapest? Is It Better Than DigitalOcean? (Full Pricing Table & Free Credit Codes)

Last Tuesday I spun up a Vultr instance at 2 a.m. to test a side project, used it for nine hours, then destroyed it before bed. The bill came to about seven cents. That's the whole pitch of Vultr hourly billing in one sentence — you pay for the hours a server actually exists, capped at the monthly rate, with no long-term contract.

**Vultr hourly billing** is a pay-as-you-go pricing model where cloud instances are charged by the hour up to a monthly cap (672 hours for most plans, 730 hours for GPUs), so short-lived workloads cost cents instead of a full month's fee. This guide breaks down how the cap math works, lists every current Vultr plan with its real per-hour price, compares Vultr against DigitalOcean and Linode, and shows the promo codes that still work for new accounts. 👉 [Check Vultr's current plans and pricing](https://www.vultr.com/pricing/?ref=9738262-9J)

## How Vultr Hourly Billing Actually Works (The 672-Hour Cap)

Most people get confused here, so let's get the math out of the way first.

Vultr takes the monthly price of a plan and divides it by 672 hours (which equals 28 days). That gives you the hourly rate. Run the server for 200 hours? You pay 200 × hourly rate. Run it for 700 hours? You stop at the monthly cap — you never pay more than the listed monthly price, even in a 31-day month.

The formula looks like this:

$$\text{Hourly Rate} = \frac{\text{Monthly Price}}{672}$$

There's one important wrinkle. If you upgrade an instance mid-month, the cap math resets per plan tier. According to [Vultr's official billing FAQ](https://www.vultr.com/resources/faq/), you may be billed more than 672 hours in a month where you upgraded, because each plan segment bills at its own hourly rate for the actual hours it ran.

GPU plans work differently. NVIDIA GH200, H100, and similar accelerator instances use a 730-hour month (the average length of a calendar month) instead of 672. So a GPU plan that previously billed $0.179/hr for 672 hours now bills $0.165/hr under the 730-hour calculation, as noted in the same FAQ.

**Summary in plain terms:** Vultr charges you per hour, but never more than the monthly sticker price. Stop early, save money. Run all month, pay the same as a monthly subscriber.

## Vultr Hourly Billing Plans: Full Pricing Table

Below is every Cloud Compute and Optimized Cloud Compute plan currently listed on Vultr's pricing page, with both the monthly cap and the per-hour rate. All prices are USD, on-demand, billed hourly. 👉 [View all Vultr plans on the official pricing page](https://www.vultr.com/pricing/?ref=9738262-9J)

### Cloud Compute — Regular Performance (shared vCPU, regular SSD)

| vCPU | RAM | Storage | Bandwidth | Monthly Cap | Hourly Rate | Get Started |
|------|-----|---------|-----------|-------------|-------------|-------------|
| 1 | 0.5 GB | 10 GB | 0.50 TB | $2.50/mo (IPv6 only) | $0.004/hr |  [Try this sandbox plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 1 | 0.5 GB | 10 GB | 0.50 TB | $3.50/mo | $0.005/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 1 | 1 GB | 25 GB | 1.00 TB | $5/mo | $0.007/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 1 | 2 GB | 55 GB | 2.00 TB | $10/mo | $0.015/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 2 | 2 GB | 65 GB | 3.00 TB | $15/mo | $0.022/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 2 | 4 GB | 80 GB | 3.00 TB | $20/mo | $0.030/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 4 | 8 GB | 160 GB | 4.00 TB | $40/mo | $0.060/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 6 | 16 GB | 320 GB | 5.00 TB | $80/mo | $0.119/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 8 | 32 GB | 640 GB | 6.00 TB | $160/mo | $0.238/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 16 | 64 GB | 1280 GB | 10.00 TB | $320/mo | $0.476/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 24 | 96 GB | 1600 GB | 15.00 TB | $640/mo | $0.952/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |

### Cloud Compute — High Performance (AMD EPYC / Intel Xeon + NVMe)

| vCPU | RAM | Storage | Bandwidth | Monthly Cap | Hourly Rate | Get Started |
|------|-----|---------|-----------|-------------|-------------|-------------|
| 1 | 1 GB | 25 GB | 2.00 TB | $6/mo | $0.009/hr |  [Start with $6/mo](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 1 | 2 GB | 50 GB | 3.00 TB | $12/mo | $0.018/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 2 | 2 GB | 60 GB | 4.00 TB | $18/mo | $0.027/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 2 | 4 GB | 100 GB | 5.00 TB | $24/mo | $0.036/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 4 | 8 GB | 180 GB | 6.00 TB | $48/mo | $0.071/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 4 | 12 GB | 260 GB | 7.00 TB | $72/mo | $0.107/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 8 | 16 GB | 350 GB | 8.00 TB | $96/mo | $0.143/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 12 | 24 GB | 500 GB | 12.00 TB | $144/mo | $0.214/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |

### Cloud Compute — High Frequency (3GHz+ Intel Xeon + NVMe)

| vCPU | RAM | Storage | Bandwidth | Monthly Cap | Hourly Rate | Get Started |
|------|-----|---------|-----------|-------------|-------------|-------------|
| 1 | 1 GB | 32 GB | 1.00 TB | $6/mo | $0.009/hr |  [Pick High Frequency plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 1 | 2 GB | 64 GB | 2.00 TB | $12/mo | $0.018/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 2 | 2 GB | 80 GB | 3.00 TB | $18/mo | $0.027/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 2 | 4 GB | 128 GB | 3.00 TB | $24/mo | $0.036/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 3 | 8 GB | 256 GB | 4.00 TB | $48/mo | $0.071/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 4 | 16 GB | 384 GB | 5.00 TB | $96/mo | $0.143/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 6 | 24 GB | 448 GB | 6.00 TB | $144/mo | $0.214/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 8 | 32 GB | 512 GB | 7.00 TB | $192/mo | $0.286/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 12 | 48 GB | 768 GB | 8.00 TB | $256/mo | $0.381/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |

### Optimized Cloud Compute — Dedicated vCPU (General Purpose)

| vCPU | RAM | Storage | Bandwidth | Monthly Cap | Hourly Rate | Get Started |
|------|-----|---------|-----------|-------------|-------------|-------------|
| 1 | 4 GB | 30 GB | 4.00 TB | $30/mo | $0.045/hr |  [Start at $30/mo](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 2 | 8 GB | 50 GB | 5.00 TB | $60/mo | $0.089/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 4 | 16 GB | 80 GB | 6.00 TB | $120/mo | $0.179/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 8 | 32 GB | 160 GB | 7.00 TB | $240/mo | $0.357/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 16 | 64 GB | 320 GB | 8.00 TB | $480/mo | $0.714/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 24 | 96 GB | 480 GB | 9.00 TB | $720/mo | $1.071/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 32 | 128 GB | 640 GB | 9.00 TB | $960/mo | $1.429/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 40 | 160 GB | 768 GB | 10.00 TB | $1,200/mo | $1.786/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 64 | 192 GB | 960 GB | 11.00 TB | $1,920/mo | $2.857/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| 96 | 256 GB | 1280 GB | 12.00 TB | $3,840/mo | $5.714/hr |  [Choose this plan](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |

### Optimized Cloud Compute — CPU / Memory / Storage Optimized

| Type | Smallest Plan | Monthly Cap | Hourly Rate | Get Started |
|------|---------------|-------------|-------------|-------------|
| CPU Optimized | 1 vCPU / 2 GB / 25 GB | $28/mo | $0.042/hr |  [Pick CPU Optimized](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Memory Optimized | 1 vCPU / 8 GB / 50 GB | $40/mo | $0.060/hr |  [Pick Memory Optimized](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |
| Storage Optimized | 1 vCPU / 8 GB / 150 GB | $75/mo | $0.112/hr |  [Pick Storage Optimized](https://www.vultr.com/products/cloud-compute/?ref=9738262-9J) |

Each of these optimized families scales up to 32 vCPU configurations with matching RAM and NVMe storage. The cheapest entry point is the Regular Performance $2.50/mo sandbox (IPv6 only, limited to 2 instances per account) or the $5/mo regular plan for a normal IPv4 server.

**Summary in plain terms:** Entry-level Vultr hourly billing starts around $0.004/hr — about a third of a cent per hour. For a 10-hour test session you pay less than a nickel.

## Hidden Costs and Gotchas in Vultr Hourly Billing

Here's where the model bites people who don't read the fine print.

**Stopped instances still bill.** This is the single most common surprise. According to [Vultr's billing documentation](https://docs.vultr.com/support/platform/billing/are-stopped-instances-still-billed-on-vultr), a stopped instance keeps reserving RAM, SSD, IP aliases, and vCPU — so the hourly charge continues until you click **DESTROY**. Powering off is not the same as cancelling. If you want to stop paying, destroy the instance, take a snapshot first if you want to restore it later.

The other add-ons stack up if you're not paying attention:

- **Automatic backups:** +20% on top of the base monthly/hourly rate
- **Snapshots stored on your account:** $0.05 per GB per month
- **DDoS Protection:** +$10/month per instance
- **Bandwidth overage:** $0.01 per GB beyond your quota (Vultr charges only outbound traffic; inbound is free)
- **Additional IPv4 addresses:** small extra fee per IP
- **VAT/sales tax:** added on top in 35+ countries, ranging from 5% to 27% depending on location

**Summary in plain terms:** The headline hourly rate is honest, but backups, snapshots, DDoS protection, and tax can quietly double your effective cost. Turn off anything you don't actively need.

## Vultr vs DigitalOcean vs Linode: Hourly Billing Comparison

Vultr isn't the only hourly-billed cloud out there. Here's how the three classic indie-cloud providers stack up.

According to [a Reddit comparison thread on r/VPS](https://www.reddit.com/r/VPS/comments/7rkmdw/comparison_chart_of_digitalocean_vultr_and_linode/) and [DigitalOcean's own comparison article](https://www.digitalocean.com/resources/articles/digitalocean-vs-linode-vs-vultr), all three bill hourly with a monthly cap, but the floor prices and cap math differ:

| Provider | Cheapest Hourly Plan | Hourly Rate | Monthly Cap | Billing Cap Hours |
|----------|----------------------|-------------|-------------|-------------------|
| Vultr | 1 vCPU / 0.5 GB / 10 GB (IPv6) | $0.004/hr | $2.50/mo | 672 |
| Vultr | 1 vCPU / 1 GB / 25 GB (IPv4) | $0.007/hr | $5/mo | 672 |
| DigitalOcean | 1 vCPU / 512 MB / 10 GB | ~$0.006/hr | $4/mo | 672 |
| Linode (Akamai) | 1 vCPU / 1 GB / 25 GB | ~$0.0075/hr | $5/mo | 672 |

All three providers use the same 672-hour monthly cap convention, so the math is roughly comparable. The differences that matter in practice:

- Vultr has 32 data center locations vs DigitalOcean's 14 and Linode's ~20
- Vultr offers a true $2.50 sandbox plan (IPv6 only) that neither competitor matches
- Vultr accepts Alipay, UnionPay, and crypto via BitPay — useful if you're outside the standard credit-card regions
- DigitalOcean historically has stronger documentation and community tutorials
- Linode tends to have more consistent I/O performance under load, per community benchmarks

If you want a deeper dive into how the three compare on real workload performance, the [r/webhosting community thread on Vultr vs DO](https://www.reddit.com/r/webhosting/comments/gzl23z/is_vultr_5month_vps_still_decent/) notes that "Vultr's superior I/O performance over DO for the same price" is a recurring observation, while Linode edges out on consistency.

👉 [Compare Vultr's full plan lineup side by side](https://www.vultr.com/pricing/?ref=9738262-9J)

## How to Sign Up and Start Using Vultr Hourly Billing

If you've decided to try it, here's the exact sequence. Each step is independent and ordered.

1. **Create a Vultr account** at the signup page with a valid email and password. A credit card or PayPal is required even for free-credit trials — Vultr places a temporary authorization hold to verify the card, not a charge.
2. **Redeem a promo code** under Billing → Gift Codes before deploying anything. Codes like `FLY300VULTR` and `VULTRMATCH` add free credit to your balance (more on these below).
3. **Pick a data center location** closest to your users. Vultr lists 32 regions, with pricing varying slightly between locations due to regional hardware and bandwidth costs.
4. **Choose a plan tier** — Regular Performance for testing, High Performance or High Frequency for production, Optimized Cloud Compute for dedicated vCPU workloads.
5. **Select an OS or one-click app** — Ubuntu, Debian, AlmaLinux, FreeBSD, or pre-packaged stacks like WordPress, LEMP, Docker, Plesk.
6. **Deploy and watch the meter** — your account's Billing page shows accumulated hourly charges in real time. Destroy the instance when you're done to stop the meter.
7. **Invoices settle on the 1st of each month** — accumulated hourly charges (capped at the monthly rate) get invoiced in USD, with VAT/sales tax added as a separate line item if your region requires it.

👉 [Open a Vultr account and claim the welcome credit](https://www.vultr.com/?ref=9738262-9J)

## Current Vultr Promo Codes and Free Credits (Verified Working)

Vultr runs an unusually generous promo program for new accounts. The codes below are listed on Vultr's [official coupons page](https://www.vultr.com/coupons/) and confirmed by multiple third-party trackers as of mid-2026.

| Promo Code | What You Get | Eligibility |
|------------|--------------|-------------|
| `FLY300VULTR` | $300 free credit | New accounts, 30-day expiry |
| `FLYTWOHUNDRED` | $200 free credit | New accounts, 30-day expiry |
| `VULTRMATCH` | Vultr matches your first deposit dollar-for-dollar, up to $100 | New accounts, credit expires 12 months after issue |
| `100VULTR30FREE` | $100 free credit, 30 days | New accounts |

A few things worth knowing about these promos:

- One promo per user, enforced at the account level
- Free credit expires — usually 30 days for the fly codes, 12 months for the match
- A linked credit card or PayPal is required to register, even though you won't be charged during the trial window
- Promotional credit does not apply to tax — if your region charges VAT, that's still billed to your card

The match code is the best deal if you plan to spend real money anyway. Deposit $100, get $200 in account credit, and the credit lasts a full year instead of 30 days. That's effectively a 50% discount on your first $200 of usage. 👉 [Claim the deposit-match offer on Vultr](https://www.vultr.com/match/?ref=9738262-9J)

## What Real Users Say About Vultr Hourly Billing

I pulled reviews from three different platforms to avoid the usual cherry-picking.

On the [Vultr subreddit](https://www.reddit.com/r/Vultr/comments/1sdc1uo/whats_your_overall_feedback_of_vultr/), an April 2026 thread asking the community for overall feedback had multiple users reporting stable uptime and fast provisioning. One commenter migrating from AWS noted that Vultr's UI is "cheap, simple and fast, reliable so far" — a sentiment echoed across multiple replies.

On [Hacker News](https://news.ycombinator.com/item?id=42450994), a long-time user wrote: "My experience with Vultr has been better than with any of [the bigger clouds]... They have great prices for what you get." The same thread flagged that review aggregators tend to surface negative reviews disproportionately because happy users don't bother reviewing.

On Trustpilot, the picture is more mixed — the [Vultr Trustpilot page](https://www.trustpilot.com/review/vultr.com) shows a higher ratio of negative reviews, with most complaints centering on billing disputes and account verification friction rather than the product itself. Take this with context: Trustpilot skews negative across every IaaS provider, including DigitalOcean and Linode.

According to [Vultr's official product page](https://www.vultr.com/products/cloud-compute/), the platform has hosted over 80,000,000 cloud instances since launch across 32 global data centers. That's a deployment-volume signal, not a satisfaction metric — but it does indicate the platform handles real production workloads at scale, not just hobby projects.

**Summary in plain terms:** Community sentiment is broadly positive on technical performance and price. The complaints that exist are mostly about billing/account verification friction, not the servers themselves.

## FAQ: Common Questions About Vultr Hourly Billing

**Does Vultr charge for stopped instances?**

Yes. A stopped instance continues to reserve RAM, SSD, IP aliases, and vCPU, so the hourly charge keeps accumulating. You must click DESTROY in the customer portal to actually stop billing. Take a snapshot first if you want to restore the instance later.

**How is the Vultr hourly rate calculated?**

Vultr divides the monthly plan price by 672 hours (28 days) to get the hourly rate. You're billed per hour the instance runs, capped at the monthly price. If your server is online for more than 672 hours in a calendar month, you only pay the monthly rate. GPU plans use a 730-hour month instead of 672.

**What happens if I upgrade my instance mid-month?**

Each plan segment bills at its own hourly rate for the actual hours it ran. According to Vultr's billing FAQ, you may be billed more than 672 hours in a month where you upgraded, because the cap is applied per plan, not per instance.

**Can I use Vultr hourly billing for production, or is it only for testing?**

Both. Hourly billing is the default on-demand model — there's no separate "testing" tier. Many production teams run on Vultr's hourly-billed plans full-time because the monthly cap means long-running workloads cost the same as a monthly subscription. Short-lived workloads (CI runners, ephemeral environments, burst scaling) benefit most from the per-hour granularity.

**Does Vultr hourly billing include bandwidth?**

Each plan includes a monthly bandwidth quota (varies by plan, 0.5 TB on the smallest plan up to 15 TB on large configs). Outbound traffic beyond the quota is billed at $0.01 per GB. Inbound traffic is free. Bandwidth is allocated hourly throughout the month, so partial-month usage is pro-rated.

**Can I pay with crypto or Alipay on Vultr?**

Yes. Vultr accepts Visa, Mastercard, American Express, Discover, JCB, PayPal, Alipay, UnionPay, and crypto via BitPay (BTC, BCH, ETH, DOGE, LTC, USDC, GUSD, PAX, BUSD). All billing is in USD regardless of payment method.

## Bottom Line: Is Vultr Hourly Billing Worth It?

For anyone running ephemeral workloads — CI pipelines, dev/test environments, scraping jobs, ML training bursts, or just poking at a side project for a weekend — Vultr hourly billing is one of the cheapest legitimate options on the market. The $0.004/hr floor means a 24-hour test costs roughly a dime, and the 672-hour monthly cap means you never get ambushed by an overage if a server accidentally runs all month.

The two real risks are stopped-instance billing (destroy, don't just power off) and add-on stacking (backups, snapshots, DDoS, extra IPs all add up). Both are avoidable if you read the billing page once.

For long-running production workloads, the hourly model converges to the monthly price anyway, so you're not paying a premium for flexibility — you're just getting flexibility for free. Combine that with the $100 deposit-match promo, and your first $200 of usage is effectively half price.

👉 [Head to Vultr to grab the welcome credit and pick a plan](https://www.vultr.com/?ref=9738262-9J)
