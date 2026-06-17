# ClassicSearchBar theme for Windows 11 Settings Styler

This theme replicates the old Settings app searchbox location on Windows 11 25H2+.

**Author**: [Tails](https://github.com/milestprower92)
#
**Screenshot**
[![Screenshot](screenshot.png)](screenshot.png)

## Theme selection

The theme is integrated into the mod and can be selected directly from the mod's
settings:

* Open the Windows 11 Settings Styler mod in Windhawk.
* Go to the "Settings" tab.
* Select the theme and save the settings.

## Manual installation

The theme styles can also be imported manually. To do that, follow these steps:

* Open the Windows 11 Settings Styler mod in Windhawk.
* Go to the "Settings" tab and select "Textual mode".
* Copy the content below to the text box and click "Save settings".

<details>
<summary>Content to import (click to expand)</summary>

```yaml
controlStyles:
  - target: Grid@DisplayModeStates > Grid#PaneRoot > Border > Grid#PaneContentGrid > Grid#ItemsContainerGrid
    styles:
      - Margin=0,52,0,0
      - Margin@OpenOverlayLeft=-11,-15,0,0
      - Margin@Closed=-11,-15,0,0
  - target: Grid#RootCommandSearchGrid
    styles:
      - Margin=15,133,0,0
      - HorizontalAlignment=0
      - Width=282
      - CornerRadius=0
  - target: SystemSettings.View.SettingsAutoSuggestCommandSearchBox#CommandSearchBox
    styles:
      - Width=282
      - CornerRadius=3
  - target: TextBox#CommandSearchTextBox
    styles:
      - CornerRadius=3
  - target: StackPanel#SettingsCommandSearchBoxBackground
    styles:
      - CornerRadius=3
  - target: TextBox#CommandSearchTextBox > Grid > ScrollViewer
    styles:
      - Margin=-325,0,0,0
      - Width=232
  - target: TextBox#CommandSearchTextBox > Grid > TextBlock#PlaceholderTextContentPresenter
    styles:
      - Margin=-325,0,0,0
      - Width=232
  - target: TextBox#CommandSearchTextBox > Grid > Button#DeleteButton > Grid
    styles:
      - Margin=-100,5,5,5
      - Width=25
      - CornerRadius=3
  - target: TextBox#CommandSearchTextBox > Grid > Button#QueryButton > ContentPresenter
    styles:
      - Margin=253,0,0,0
  - target: TextBox#CommandSearchTextBox > Grid > Button#QueryButton > ContentPresenter > FontIcon > Grid > TextBlock
    styles:
      - FontSize=12
      - Opacity=0.8
  - target: SystemSettings.View.SettingsAutoSuggestCommandSearchBox
    styles:
      - Width=282
  - target: Button#CommandSearchBoxFlyoutButton
    styles:
      - Margin=140,-125,0,0
```
</details>
