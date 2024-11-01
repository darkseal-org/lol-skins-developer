# League of Legends Skins for Developer Repository

This repository aims to provide a centralized and easily accessible location for all in-game skins available for League of Legends. The purpose of this project is not to undermine the custom skin scene within League of Legends. Instead, we aim to provide a solution for players who have been unable to afford skins since the introduction of Vanguard. Previously, these players relied on tools like LolSkin or R3nzSkin, which are no longer viable.

Using custom skins does not confer any competitive advantage, as they are only visible to the player utilizing them. 

The creator of this repository believes that with the implementation of predatory practices in skin sales — exemplified by exclusive skins like the Faker skin, which cost as much as three months' wages in some regions — Riot has restricted access to certain content for a significant portion of its player base. 

> We hold that gaming culture should be inclusive and accessible, not just a privilege for those who can afford it.

## Repository Structure

The repository is organized as follows:

```
/
├── 1/  # Annie
│   ├── 0.fantome  # Default skin
│   ├── 1.fantome 
│   ├── 2.fantome
│   └── ...
├── 2/  # Olaf
│   ├── 0.fantome # Default skin
│   ├── 1.fantome
│   └── ...
└── README.md
```


Key points to remember:

1. The .fantome file is a renamed ZIP archive with a specific internal structure.
2. It must contain the standard folders: RAW (for legacy content), WAD (for main mod files), and META (for metadata).
3. The WAD folder should mirror League of Legends' file structure precisely for proper mod installation.
4. The META folder must include an info.json file with basic mod information such as name, author, and version.
5. Modern mods should primarily use the WAD folder structure for optimal performance and file size.
6. The RAW folder is mainly for backwards compatibility and should be avoided for new mods unless absolutely necessary.


## API Endpoints

To get champion and skin names, you can use the following Data Dragon API endpoints:

1. Champion Data:
   ```
   https://raw.communitydragon.org/latest/plugins/rcp-be-lol-game-data/global/default/v1/champion-summary.json
   ```

2. Skins and chromas ID for a Specific Champion:
   ```
   "https://raw.communitydragon.org/latest/plugins/rcp-be-lol-game-data/global/default/v1/champions/{champion_id}.json"
   ```
  

## How to Use

1. Identify the champion key you're interested in using the champion data endpoint.
2. Navigate to the corresponding folder in this repository (e.g., `/1/` for Annie).
3. Download the desired skin file (e.g., `1.fantome` for the first skin).
4. Use the skin data endpoint to find the corresponding skin name if needed.
5. Apply the skin using a compatible tool such as:
   - [Fantome](https://github.com/LeagueToolkit/fantome)
   - [CSLOL](https://github.com/LeagueToolkit/cslol-manager)

Follow the installation instructions provided with these tools to implement the skins successfully.

## Wanna contribute?

You can simply contribute by ⭐ starring this repository. 

But, if you want to go a little further, you can:

1. Fork this repository.
2. Add or update the Fantome files in the appropriate champion folder.
3. Ensure the file naming convention (using sequential numbers) is followed.
4. Submit a pull request with a clear description of your changes.

For more details, check our [CONTRIBUTING.md](CONTRIBUTING.md) file.

## Disclaimer

This project is not endorsed by Riot Games and does not reflect the views or opinions of Riot Games or any of its affiliates. League of Legends and all related properties are trademarks or registered trademarks of Riot Games, Inc.

The use of these assets for skin hack development may violate Riot Games' terms of service. Use at your own risk.

This repository is not affiliated with the moderators of r/LoLCustom.


Consider developing or using a tool that:
1. Reads the .fantome files from this repository
2. Makes minor, non-functional alterations to the file content (e.g., adding benign metadata or comments)
3. Generates a new file with a different hash but identical functionality

By implementing such a system, you can help protect users of your development from potential bans or other consequences, should Riot Games decide to take action against the use of these specific file hashes. Remember, the goal is to preserve functionality while avoiding direct matches to the files in this public repository.

Please note that while this method may reduce the risk of detection via hash matching, it does not guarantee protection against all forms of detection or potential consequences of using custom skins. Always inform your users about the risks involved in using custom skins or any modifications to the game client.

## Donation

If you find this project helpful, consider supporting the maintainers:

- Pix: b2763e55-ac97-4963-83e9-d9827caed2de
- Ko-Fi: https://ko-fi.com/koobzaar
