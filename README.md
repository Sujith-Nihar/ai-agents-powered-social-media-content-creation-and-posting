# AI Agents for Social Media Content Generation and Posting

An end-to-end **agent-based AI system** that transforms a single user-provided idea into complete social media content — including captions, hashtags, images/videos — and automatically publishes it across multiple platforms using n8n workflows.

> 🚀 From idea → content → posting — fully automated.

---

## Overview

This project implements a fully automated, agent-based AI pipeline for social media content creation and publishing.

Users only need to provide a high-level **idea**, and the system handles the entire workflow end-to-end:

- Generates structured prompts using Gemini
- Creates captions and hashtags automatically
- Produces images or videos using generative AI models
- Publishes content across selected social media platforms
- Updates status in a centralized sheet

The system acts as a set of coordinated AI agents that convert ideas into fully ready-to-publish social media content without manual intervention.

---

## Key Capability

### Idea → Content → Posting (Fully Automated)

A single input idea is enough to trigger the complete pipeline:

- Content planning (AI-generated prompt)
- Caption generation
- Hashtag generation
- Media generation (image/video)
- Multi-platform publishing

No manual content creation or editing is required.

---

## Features

- Fully automated **idea-to-post pipeline**
- AI-generated **captions and hashtags**
- Image and video generation using generative AI models
- Multi-platform auto publishing:
  - Instagram
  - Facebook
  - X (Twitter)
  - YouTube
- Agent-based workflow orchestration using **n8n**
- Dynamic routing based on user preferences
- Automated status tracking using **Google Sheets**

---

## Workflow Architecture

The pipeline follows a structured multi-agent workflow:

1. **Schedule Trigger**
   - Runs the automation at defined intervals

2. **Read Input (Google Sheets)**
   - Fetches user-provided ideas and preferences

3. **Filter + Loop**
   - Processes only valid rows
   - Iterates through each idea

4. **AI Agent (Gemini)**
   - Converts idea into:
     - structured prompt
     - caption
     - hashtags

5. **Content Type Decision**
   - Determines whether to generate:
     - Image
     - Video

6. **Content Generation**
   - Image generation (GenAI models)
   - Video generation (GenAI models)

7. **File Upload**
   - Stores generated media for publishing

8. **Platform Routing**
   - Routes content based on selected platforms

9. **Auto Publishing**
   - Instagram
   - Facebook
   - X (Twitter)
   - YouTube

10. **Merge Results**
   - Collects responses from all platforms

11. **Update Status**
   - Updates Google Sheet with posting result

---

## Tech Stack

- **n8n** — workflow orchestration
- **Google Sheets** — input + tracking
- **Gemini (LLM)** — prompt, caption, hashtag generation
- **Generative AI models** — image and video creation
- **Social Media APIs** — automated posting
- **Cloud storage / upload nodes** — media handling

---

## Input Format

The workflow reads structured input from Google Sheets.

| idea | content_type | platforms | status |
|------|--------------|-----------|--------|
| Promote a healthy breakfast | image | Instagram, Facebook | pending |
| Startup motivation reel | video | X, YouTube | pending |

---

## How It Works

1. User provides a **simple idea**
2. AI generates:
   - prompt
   - caption
   - hashtags
3. AI creates:
   - image or video
4. Workflow automatically:
   - uploads media
   - posts to platforms
5. Sheet is updated with results

---

## Example Use Cases

- Automated brand marketing
- AI-driven social media management
- Content scaling for creators
- Campaign automation
- Multi-platform content distribution

---

## Benefits

- Eliminates manual content creation
- Scales social media operations
- Ensures consistent posting
- Reduces time from idea → publish
- Enables AI-driven marketing workflows

---

## Future Improvements

- Platform-specific caption optimization
- Hashtag performance tuning
- Approval workflow before posting
- Analytics & engagement tracking
- Add support for TikTok, LinkedIn
- Retry and failure handling
- Content calendar integration

---

## Screenshots

Add your workflow screenshot here:

```markdown
![Workflow](./assets/workflow.png)
