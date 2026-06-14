<div align="center">
  <img width="80" alt="app-icon" src="https://github.com/user-attachments/assets/e7c70824-5448-4ac6-81ed-b53369576c32" />
  <h1 style="margin-top: 0px;">Synced</h1>
  <p>Plan and manage your Twitch stream schedule 📱</p>

[![GitHub Repo stars](https://img.shields.io/github/stars/ashuhlee/synced?style=for-the-badge&logo=starship&logoColor=%23D7E0ED&labelColor=%232F2D42&color=%23FFBDF2)](https://github.com/ashuhlee/synced/stargazers)
[![GitHub Issues or Pull Requests](https://img.shields.io/github/issues/ashuhlee/synced?style=for-the-badge&logo=gitbook&logoColor=%23D9E0EE&labelColor=%232F2D42&color=C1B5FF)](https://github.com/ashuhlee/synced/issues)
[![GitHub repo size](https://img.shields.io/github/repo-size/ashuhlee/synced?style=for-the-badge&logo=removedotbg&logoColor=%23D9E0EE&labelColor=%232F2D42&color=AEE5FF)](https://github.com/ashuhlee/synced)
![Static Badge](https://img.shields.io/badge/version-beta-A5A2B7?style=for-the-badge&logoColor=%23D9E0EE&labelColor=2F2D42)
</div>

## About the App

**Platforms:** iOS, Android <br>
**Status:** In Development - Beta

A Flutter app for planning and managing your Twitch stream schedule. Built as a personal learning project to practice MVVM architecture using the Stacked framework.

### Implementation
StreamSync pulls your channel's schedule from the Twitch API and displays it in a clean, mobile-friendly interface. The goal is to make it easy to view upcoming streams, draft new events, and push them to Twitch, all from one app.

### Planned Features
 
- View your Twitch stream schedule fetched via the Twitch Helix API
- Create and edit stream events (title, category, date/time, duration)
- Draft events locally before pushing them live to Twitch (locally stored, not on Twitch)
- Save stream presets (e.g. "Scary games with viewers" with title, category, and tags pre-filled)

## Architecture
### Project Structure
The project follows an MVVM structure, keeping UI, logic, and data in distinct layers:
 
```
lib/
  models/          # Data classes (StreamEvent, etc.)
  services/        # API calls and local storage logic
  ui/
    schedule_list/ # Main schedule view + viewmodel
    add_edit_event/ # Create/edit stream event view + viewmodel
```

### Tech Stack
 
- **Flutter** + **Dart**
- **Stacked** — MVVM architecture
- **Twitch Helix API** — schedule read/write
- **OAuth 2.0 or BetterAuth** — Twitch authentication (`channel:manage:schedule` scope)
