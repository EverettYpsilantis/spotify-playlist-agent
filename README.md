# spotify-playlist-agent
Claude SDK-powered Spotify playlist generator with iterative refinement and Discogs integration.
# Spotify Playlist Agent

A production-style multi-tool Claude SDK agent that generates and iteratively 
refines Spotify playlists based on natural language inputs: venue, vibe, artist, 
BPM, energy, danceability, valence, and popularity range.

## Features
- Natural language playlist generation via Claude SDK agent loop
- Real-time Spotify API integration (search, recommendations, audio features)
- Discogs collection import, match your vinyl/CD collection to Spotify
- Iterative refinement through multi-turn conversation
- Audio feature targeting (BPM, energy, danceability, valence, acousticness)
- Event-specific segment organization (ceremony, cocktail hour, first dance, party)

## Architecture
- **SpotifyMCPClient** — Spotify REST API wrapped into 6 discrete MCP-style tools
- **IterativePlaylistAgent** — Agentic loop handling tool-use, execution, and conversation history
- **PlaylistSession** — Stateful dataclass maintaining context across multi-turn refinement
- **Discogs Workflow** — 4-step pipeline: collection fetch → track expansion → Spotify matching → agent load

## Setup
1. Get API keys:
   - Anthropic: https://console.anthropic.com
   - Spotify: https://developer.spotify.com/dashboard
   - Discogs (optional): https://www.discogs.com/settings/developers
2. Open the notebook and enter keys when prompted
3. Run cells top to bottom and start generating

## Tech Stack
Python, Anthropic SDK, Spotify Web API, Discogs API, ipywidgets, pandas, httpx
