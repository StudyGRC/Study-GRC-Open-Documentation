# Contributing to Study GRC Documentation

Thank you for exploring how to contribute to Study GRC. Your unique perspectives and contributions make this a valuable resource for everyone.

💬 **Need help or want to discuss a policy idea?** Join the conversation in our [Study GRC Discord Server](https://discord.studygrc.org).

---

## Ways to Contribute

You do not need coding experience to contribute. Choose the method that works best for you:

- **Open an issue:** If you find a typo, notice an outdated policy, or want to suggest a new document, go to the **Issues** tab and open a ticket describing the need.
- **Join the discussion:** Share your expertise and help shape projects by commenting on existing GitHub Issues or joining our Discord.
- **Submit a change (Pull Request):** If you are ready to write or edit documentation, follow the pull request steps below.

## How to Submit Changes

We follow the standard GitHub workflow. Our `main` branch always represents our **Approved** and active documentation. 

If you are new to GitHub, here is a plain-language guide to help you submit your updates:

- **Fork the repository:** Click the "Fork" button at the top right of this page to create a personal workspace under your GitHub account.
- **Create a new branch:** Name your branch specifically for your task (for example, `draft-incident-response` or `fix-password-typo`).
- **Make your changes:** Add or edit Markdown files in the appropriate category folder (such as `/Policies` or `/Guidelines`). You can do this directly in your web browser or by cloning the repository to your computer.
- **Commit your changes:** Save your work with a clear, descriptive message explaining your updates (for example, "Added mobile device rules to BYOD policy").
- **Push the branch:** Send your saved changes from your computer to your GitHub account (skip this step if editing in the browser).
- **Open a Pull Request:** Return to the main Study GRC repository and click "New Pull Request" to ask the community to review and add your work.

---

## The Metadata Workflow

We organize files by category and track each document's lifecycle using a small block of data at the top of the Markdown file, known as YAML frontmatter.

### Writing a New Document

When drafting a new document, please copy this block, paste it at the top of your file, and fill in the brackets:

```yaml
***
title: [Document Title]
status: Draft
last_reviewed: YYYY-MM-DD
next_review_due: YYYY-MM-DD
owner: [Role or Team]
***
```
