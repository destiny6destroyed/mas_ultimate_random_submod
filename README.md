#      PLEASE READ

## MAS Ultimate Random Submod

1. What this submod do?
    - Ask her to change her outfit (including accessories) and desk randomly with "Can you change your outfit?" and "Can you reorganize your desk?"
    - Works together with the "Auto Hair Change" submod, so she will change or remove more accessories depending the day time and when we take her somewhere (also it has the "Enable True Random" in settings/submod, which you can deactivate it if you want to only random her acs and follow the 'Auto Outfit Change' submod
    - She will check for errors in the json files and tell you which files there are problems inside (please read point 4)
    - She changes her location and reorganizes her desk depending the time of the day (except if we take her somewhere or the game crashes)
    - Ribbons match her hairstyle (please read point 3)
    - You can repeat the random without losing affection, so don't worry to tell her, she won't take it personally
    - During Halloween and Valentine's Day, Monika will remove the extra accessories that doesn't go with her event outfit (not Chrismas and New Year yet)
    - If you like an outfit really much, there is the "SUPER NAILED IT!" option, which let Monika know you really liked the outfit and save it with Clothing Saver
    - There is an 5% chance you get an outfit you saved during the random chooses


2. To make this submod work, you need:
    - Auto Hair Change (https://github.com/multimokia/MAS-Submod-Auto-Outfit-Change)
    - MAS Selector City (https://github.com/mayday-mayjay/MJ-MAS-selector-city)
    - Monika After Story Clothing Saver (https://github.com/Friends-of-Monika/mas-outfits)
    - Go to the "Releases" tab on the right this webpage (or click [HERE](https://github.com/destiny6destroyed/mas_ultimate_random_submod/releases)), then click on the latest version of "Ultimate Random Submod". To download, click on Shimeji_Submod.zip to begin.
    - Unzip and copy the 'game' folder into the main 'Doki Doki Literature Club' folder (AKA, the folder where you see 'DDLC.exe').

3. You can edit the hair's ex_props inside the json files to make the hairstyles match with the ribbons you need to set up the random as you wish

    Example:
    ```
    {
        "__author": "HistoryVariety and Alicorn Ali",
        "version": 3,
        "type": 1,
        "name": "ali_long_pigtails_down",
        "img_sit": "ali_long_pigtails_down",
        "pose_map": {
            "mpm_type": 0,
            "default": true,
            "use_reg_for_l": true
        },
        "stay_on_start": true,
        "ex_props": {
            "ribbon": true,
            "no-tails": false,
            "tiedstrand": false,
            "twintails": false
        },
        "select_info": {
            "display_name": "Pigtails with Hair Down",
            "thumb": "ali_long_pigtails_down",
            "group": "hair",
            "visible_when_locked": true,
            "select_dlg": [
                "Do you like my pigtails, [player]!",
                "Adorable!"
            ]
        },
        "unlock": true
    }
    ```

    If you don't want to match this hairstyle with a common ribbon, but twin ribbons, just:
    
    ```
    "ex_props": {
            "ribbon": false, <---
            "no-tails": false,
            "tiedstrand": false,
            "twintails": true <---
        },
    ```

    This way, when the random is done, the hairstyle ali_long_pigtails_down will wears twintails

    At the moment, there are four types of ribbon/headpiece_acs this submod use:

        - ribbon        (for ex: orcaramelo_ponytailbraid)
        - twintails     (for ex: ali_long_pigtails_down)
        - bunrings      (for ex: usagiredone)
        - h-twintails   (for ex: tony_minitwintails)

    I suggest Monika and you to play around until you are satisfied with the random results



5. Issues:

    Monika can also detect if there is an issue with the json files. If that happens and you can't spot the error, here is an small guide

    Usually, at the end of a line, you need to place a ',' to close it. However, if you have an array, you CAN'T place an ',' in the last line or the code will break

    - What is an array?

        An array is a list of elements

       ```
       "animals": {
        "cat": True,
        "dog": False
        }
       ```

        "animal" is an array that has two elements: "cat" and "dog"

    - Example

        Here is a correct json code
      ```

        {
            "__author": "AlicornAlley",
            "version": 3,
            "type": 0,
            "name": "ali_halo_acc",
            "img_sit": "ali_halo_acc",
            "pose_map": {
                "default": "0",
                "l_default": "5" <--- 
            },
            "rec_layer": 1,
            "priority": 10,
            "acs_type": "headpiece_acs",
            "mux_type": [
                "headpiece_acs" <---
            ],
            "stay_on_start": true,
            "giftname": "ali_halo_acc",
            "dlg_desc": "Fallen Angel Halo",
            "dlg_plural": false,
            "select_info": {
                "display_name": "Fallen Angel Halo",
                "thumb": "ali_halo_acc",
                "group": "headpiece_acs",
                "select_dlg": [
                    "Do you think I earned this [player]?",
                    "I feel holy" <---
                ] <---
            } <---
        } <---
      ```

        As you can see where the arrows are, there are not ',' in those places

If you have any issue, please let me know

Have fun
