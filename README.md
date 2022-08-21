# TFM_Penguins
 TFM Mods


## Notes

Edit Binaries with dnSpy (open Assembly-CSharp.dll, replace the one in gamedata once done)

- Draw card modifier: TM_GameData.DrawActionCards()
    - TM_GameData contains other modifiers such as choosing Corporations, Preludes, Generation, Player Productions starts, Global Parameters
    - Project cards == "Action Cards"
    - TM_GameData.SetActionCards() function loads in the acceptable Action Cards into the game.
        - CardDeck loads data from Dataset CardDataset singleton
        - Example in TESTCardLoader.Awake()
    - To always draw certain card, edit DrawActionCard with card IDs


- Game Initialized in TM_Game.Start()
    - "GameInfo" from AsmodeeService?
    - Cards for a game determined in TM_Game.CreateGameData()

- Card cost modifier
- Expansion == "Extension/GameExtension"


- Productions and Resources
    - Production Data managed by TM_PlayerProductionResourceData
    - Resource Data managed by TM_PlayerResourceData

- Specific Cards
    - TM_CardData


View Assets with AssetStudio

- Cards are composed of (Sprites):
    - Image
        - art_tex_card_image_<CARD ID>
        - SpriteAtlasTexture-CardImages
    - VP Icon
        - UI_ic_card_lrg_<ICON>
        - SpriteAtlasTexture-Icons
    - Resources (e.g. Microbes)
        - UI_ic_com_med_ResCard<RESOURCE> (science, MC, )
    - Back of Card
        - SpriteAtlasTexture-Cards
    
    

- Corporation cards have:
    - Icons (UI_ic_com_corp_<Corp Name>)
        -Assuming these are for game state things
    - Logos (UI_img_card_logo_<Corp Name>)
        - These go on the cards
        - SpriteAtlasTexture-CorpCards



Cards + IDs accessible by at this [website](https://ssimeonoff.github.io/cards-list)