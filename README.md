# C-Unplugged

C-Unplugged is a terminal-based music library and playlist manager written in C. It provides an interactive command-line interface to manage songs, organize them into albums, build playlists, and simulate music playback with a visual progress bar.

## Features

- **Music Library Management**: Add new songs with metadata (Title, Artist, Length, Year) to your library.
- **Albums & Playlists**: Create custom albums, add/remove songs, and manage the track order (swap, move). Queue songs and albums into your current playlist.
- **Playback Controls**: Simulate playback with play, pause, resume, fast forward, previous, repeat, and loop commands.
- **Interactive CLI**: A persistent prompt where you can execute commands using their names or numeric IDs.
- **Data Persistence**: Automatically saves and loads your library and albums to/from binary files across sessions.

## Command Line Interface

The application features a rich command menu. Upon running the program, you will be greeted with an interactive prompt (`>`).

- All available commands can be listed by using the `HELP` command (or just type `1`).
- To use any specific command, type it in its given syntax.
- You can use either the song (or album) name, or its serial number (as displayed when you list them). 
  - *Example*: `DELETE ALBUM "My Mix"` is the same as typing `12 1` (assuming "My Mix" is the 1st album and command 12 is DELETE ALBUM).

### Example Commands
- `LOAD` - Add a new song into the library.
- `LIST SONGS` / `LIST ALBUMS` - View your library.
- `CREATE <albumname>` - Create a new album.
- `MANAGE ADD <albumname> <song>` - Add a song to an album.
- `NEXT SONG <song>` - Add a song to the playback queue.
- `PAUSE` / `RESUME` / `FWD` / `PREV` - Playback controls.

## Build & Run

### Prerequisites
- GCC compiler
- `make`

*NOTE: This program relies on Unix-like process management (`fork`, `kill`, `waitpid`) and POSIX signals, so it might not work natively on Windows. Preferably use WSL, Linux, or macOS.*

### Instructions
1. **Build the project**: 
   ```bash
   make
   ```
2. **Run the application**: 
   ```bash
   make run
   ```
   *(Alternatively, execute `./c_unplugged` directly)*
3. **Clean build artifacts**: 
   ```bash
   make clean
   ```
