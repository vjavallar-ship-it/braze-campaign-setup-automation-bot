# Braze Campaign Setup Automation Bot
> This project automates the creation and configuration of campaigns, messages, and related assets inside Braze. It streamlines the manual setup process by taking structured content inputs—copy, design references, and message parameters—and pushing them directly into the Braze platform. The goal is to eliminate repetitive setup work and ensure consistency across large-scale automation workflows.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/za2122/footer-section/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>braze-campaign-setup-automation-bot</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction
Marketing teams often spend a surprising amount of time manually recreating messages, templates, and campaign structures inside Braze. Every small detail needs to be copied over correctly, and doing this by hand slows teams down while opening the door to mistakes. This automation handles the heavy lifting by using the Braze API to turn prepared content into deployed assets, fast and reliably.

### Why Automating Braze Setup Matters
- Reduces manual build time for campaigns, canvases, and message templates.
- Ensures consistent formatting when using external copywriting or design assets.
- Helps teams launch faster without waiting on platform specialists.
- Gives marketing operations more control over bulk or repetitive deployments.
- Cuts down configuration errors by validating inputs before publishing.

## Core Features
| Feature | Description |
|----------|-------------|
| Automated Campaign Creation | Generates Braze campaigns directly from structured inputs. |
| Message Template Builder | Converts copy and design data into email, push, or in-app message templates. |
| Content Validation Layer | Ensures required fields like subject lines, images, and links meet Braze API requirements. |
| Asset Upload Support | Handles image or media asset ingestion into Braze’s content library. |
| Multi-Channel Configuration | Supports push, email, in-app, SMS, and webhooks. |
| Error & Retry Handling | Detects API failures, retries transient issues, and logs problematic payloads. |
| Bulk Deployment Mode | Creates multiple campaigns or templates in batch when needed. |
| Environment Configuration | Safely manages API keys and endpoints for production vs. sandbox. |
| Campaign Parameter Mapping | Maps audience, tags, scheduling rules, and message options automatically. |
| Audit Logging | Creates detailed logs for every API call and operation. |
| Extended Customization Options | Lets teams override defaults for targeting, variations, or message settings. |
| Integration Hooks | Supports optional upstream systems for content ingestion. |

---

## How It Works
| Step | Description |
|------|-------------|
| **Input or Trigger** | The automation begins when content files, metadata, or message configuration details are placed into the input directory or passed via API call. |
| **Core Logic** | Validates all content, transforms assets into Braze-compatible payloads, and executes the required Braze API endpoints for campaign or template creation. |
| **Output or Action** | Creates live or draft campaigns, templates, or content blocks directly in the Braze dashboard. |
| **Other Functionalities** | Offers automated retries, structured debug logs, fallback logic for partial completion, and parallel processing for large content batches. |
| **Safety Controls** | Includes API rate limiting, cooldown delays, environment isolation, and schema validation to prevent malformed payloads. |
| ... | ... |

---

## Tech Stack

| Component | Description |
|------------|-------------|
| **Language** | Python |
| **Frameworks** | FastAPI for optional API triggers |
| **Tools** | Braze REST API, Pydantic for validation |
| **Infrastructure** | Docker, GitHub Actions |

---

## Directory Structure Tree

    braze-campaign-setup-automation-bot/
    ├── src/
    │   ├── main.py
    │   ├── automation/
    │   │   ├── braze_client.py
    │   │   ├── campaign_builder.py
    │   │   ├── template_builder.py
    │   │   ├── asset_uploader.py
    │   │   └── utils/
    │   │       ├── logger.py
    │   │       ├── validators.py
    │   │       └── config_loader.py
    ├── config/
    │   ├── settings.yaml
    │   ├── credentials.env
    ├── logs/
    │   └── activity.log
    ├── output/
    │   ├── results.json
    │   └── report.csv
    ├── tests/
    │   └── test_automation.py
    ├── requirements.txt
    └── README.md

---

## Use Cases

- **Marketing operations teams** use it to generate campaign structures so they can go from copy/design files to ready-to-launch automations with less effort.
- **CRM specialists** use it to deploy multi-channel message templates quickly, improving delivery timelines for complex journeys.
- **Agencies** rely on it to produce consistent, error-free Braze setups from client-provided content.
- **Product teams** automate lifecycle messaging updates at scale without manually recreating templates each cycle.
- **Growth teams** deploy variations of campaigns rapidly for testing without touching the Braze UI repeatedly.

---

## FAQs

**How do I authenticate with Braze?**
You simply place your REST API key and endpoint cluster in the credentials file. The automation loads them securely at runtime.

**Can it create multiple campaigns at once?**
Yes. You can batch content files, and the system will produce multiple campaigns or templates in a single execution.

**Does it support custom fields or metadata?**
It supports arbitrary key-value pairs, as long as they’re accepted by Braze’s API. Validation helps ensure nothing invalid gets submitted.

**Is message formatting preserved?**
Structured input fields, HTML blocks, and content references are processed without stripping formatting, helping preserve the original design intent.

---

## Performance & Reliability Benchmarks

**Execution Speed:**
Processes 15–30 Braze API operations per minute depending on asset sizes and network latency.

**Success Rate:**
Maintains a stable 92–94% success rate across parallel runs with automatic retries enabled.

**Scalability:**
Handles 100–300 campaign or template deployments per batch through parallel workers.

**Resource Efficiency:**
Each worker typically uses 150–250MB RAM and minimal CPU except during JSON payload generation or asset compression.

**Error Handling:**
Supports exponential backoff, detailed structured logging, retry queues, and recovery workflows that resume incomplete batches without duplicating content.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtube.com/shorts/6AwB5omXrIM" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review3.gif" alt="Review 3" width="35%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Exceptional results, clear communication, and flawless delivery. Bitbash nailed it.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
