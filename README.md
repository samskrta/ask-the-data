# Ask the Data

Live demo page for the MSA 2026 class "AI That Actually Works" (Jack Miller, SCS Communications, and Todd Daganaar, Hometown Hero Appliance Repair).

- `index.html` loads `visits.csv` (31,088 anonymized Hometown Hero tech visits, Oct 2025 to Sep 2026) into an in-browser SQL engine (AlaSQL).
- Questions go to a Supabase Edge Function (`ask-the-data` in the skynet project), which adds the Anthropic API key and relays to Claude with a single `run_sql` tool. Every query runs in the browser and is shown on screen.
- The data has no names, phone numbers, addresses, ZIP codes, invoice numbers or notes. IDs are random codes.

Turn the demo off: set the Supabase secret `ASK_ENABLED` to `false`, or revoke the API key.
