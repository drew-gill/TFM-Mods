# TFM_Penguins
 TFM Mods


## Notes

Edit Binaries with dnSpy

- Draw card modifier: TM_GameData.DrawActionCards()
    - TM_GameData contains other modifiers such as choosing Corporations, Preludes, Generation, Player Productions starts, Global Parameters
- Card cost modifier

- Productions and Resources
    - Production Data managed by TM_PlayerProductionResourceData
    - Resource Data managed by TM_PlayerResourceData


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