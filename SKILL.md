---
name: lindo-ai
description: Create and manage websites, pages, and blog posts using the Lindo AI platform. Manage clients, assign websites, generate magic links, and allocate credits.
---

# Lindo AI

You have access to the Lindo AI platform through the MCP server `@lindoai/mcp-server`. Use it to help users manage their website builder workspace.

## Setup

The Lindo MCP server should be configured. If not, add it:

```bash
claude mcp add lindo -- npx -y @lindoai/mcp-server
```

Or for Cursor/VS Code, add to your MCP config:

```json
{
  "mcpServers": {
    "lindo": {
      "command": "npx",
      "args": ["-y", "@lindoai/mcp-server"]
    }
  }
}
```

## Capabilities

### Websites
- **Create Website**: Generate a full website from a text prompt using AI (`create_website`)
- **List Websites**: View all websites in the workspace (`list_websites`)
- **Get Website Details**: View details of a specific website (`get_website`)
- **Update/Delete Website**: Modify or remove websites

### Pages
- **Create Page (AI)**: Generate a page from a prompt (`create_page`)
- **Publish Page**: Publish static HTML content (`publish_page`)
- **List/Get/Delete Pages**: Manage existing pages

### Blog Posts
- **Create Blog (AI)**: Generate a blog post from a prompt (`create_blog`)
- **Publish Blog**: Publish a static markdown blog post (`publish_blog`)
- **List/Get/Delete Blogs**: Manage existing blog posts

### Clients
- **Create/List/Delete Clients**: Manage workspace clients
- **Assign Website**: Assign a website to a client (`assign_website`)
- **Generate Magic Link**: Create a login link for a client (`generate_magic_link`)

### Credits
- **Get Credits**: Check workspace credit balance (`get_credits`)
- **Allocate Credits**: Assign credits to a client (`allocate_credits`)

### Workspace
- **Get/Update Workspace**: View and modify workspace settings
- **Analytics**: View workspace and website analytics

## Guidelines

- When creating websites, pages, or blogs with AI, provide detailed prompts for better results
- AI creation is asynchronous — workflows take 1-2 minutes to complete
- Always confirm destructive actions (delete, unpublish) before executing
- Website IDs look like `webXXXXXX`, page/blog IDs like `assXXXXXX`, client IDs like `teamXXXXXX`
- If the user doesn't specify a website ID, list websites first and ask which one to use
- For blog publishing, accept markdown content — the API converts it to HTML automatically
- Requires a Business or Whitelabel plan for API access
