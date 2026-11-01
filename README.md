# StayNest – Hotel Booking MVP

StayNest is a hotel booking website (React + Vite + Supabase). The base project already existed; this assignment added booking validation, testing docs, a code-review skill and an AI-assisted Jira and GitHub workflow. It allows users to search for hotels, view detailed information, and book stays with real-time data persistence.

## Features
- **Hotel Search**: Find hotels by destination, dates, and number of guests.
- **Detailed Listings**: View hotel descriptions, facilities, and available room types.
- **Validated Booking**: A booking form with real-time validation for required fields and date logic.
- **Database Integration**: Real-time booking storage in Supabase using a secure Postgres function.
- **Confirmation Page**: Instant confirmation with a unique booking ID.
- **Responsive Design**: A clean, mobile-friendly layout.

## Tech Stack
- **Frontend**: React 18 + Vite
- **Styling**: Plain CSS
- **Backend/Database**: Supabase (PostgreSQL)
- **Deployment**: Netlify

## Setup
1. **Install Dependencies**:
   ```bash
   npm install
   ```
2. **Configure Environment**:
   - Copy `.env.example` to `.env`.
   - Add your own `VITE_SUPABASE_URL` and `VITE_SUPABASE_ANON_KEY` (found in your Supabase Project Settings → API).
3. **Initialize Database**:
   - Open the Supabase SQL Editor.
   - Run `supabase/schema.sql` to create tables and RLS policies.
   - Run `supabase/update_rooms_extras.sql` to populate sample hotels and pricing.
4. **Run Locally**:
   ```bash
   npm run dev
   ```

## Usage
- Use the homepage search box to filter hotels.
- Select a hotel to view details and choose a room type and extras.
- Complete the booking form to save your reservation to the database.

## Testing
For manual test cases and verification steps for booking validation, please refer to [docs/TESTING.md](docs/TESTING.md).

## AI-Assisted Workflow
This project utilizes an agentic development workflow:
- **Task Tracking**: Managed via Jira project **KAN**.
- **Version Control**: GitHub branches and pull requests are used for all features.
- **MCP Integration**: Atlassian MCP server is used for Jira synchronization.
  - Setup: `claude mcp add --transport http atlassian https://mcp.atlassian.com/v2/mcp`
  - Authentication: Run `/mcp` to authenticate.
- **Quality Assurance**: Custom `code-review` skill located in `.claude/skills/code-review` ensures consistency and security.
- **Security**: Never commit `.env` files or real API tokens to the repository.

## Limitations
- **Error Reporting**: Booking error messages currently display database error text directly to the user. In a production environment, these should be replaced with generic user-friendly messages while technical details are logged internally.

---
*Note: The base StayNest project already existed. This assignment added KAN-5 booking validation, comprehensive testing documentation, the `code-review` skill, and the integrated Jira/GitHub AI workflow.*
