# WindowGlass theme for Windows 11 Settings Styler

A theme that adds a modern, glassy aesthetic with a compact layout to the Windows 11 Settings App.

**Author**: [Nathaniel4JC](https://github.com/Nathaniel4JC)

![Screenshot](screenshot.png)

## Notes
- This theme works best on Windows 11 **25H2** and later.
- This theme currently works on displays with a resolution **of or above** 1366x768.
- This theme consists of **three** backgrounds:
    - Glass
    - Frosted
    - Acrylic
  - In order to switch between these backgrounds, replace the value for "Background" with "$Glass", "$Frosted" or "$Acrylic".
- To change the app's corner radius, install the 'Custom Window Corner Radius' Mod and use the paste the following in the 'Advanced' section:
  ```json
  {"radius":20,"smallRadius":6,"tooltipRadius":-1}
  ```

## Bonus
- This theme can style other UWP Applications as well. 
- To make it work, you'll need to:
  - Add any of the following UWP apps to the 'Custom process inclusion list' under 'Advanced settings' in the Windows 11 Settings Styler mod:
  CalculatorApp.exe
  GameBar.exe
  Microsoft.Media.Player.exe
  mspaint.exe
  Taskmgr.exe
  Time.exe
  Todo.exe
  SecHealthUI.exe
  SystemSettings.exe
  VoiceRecorder.exe
  Whatsapp.exe
  WindowsCamera.exe
  WinStore.App.exe
  WindowsBackupClient.exe
  WindowsTerminal.exe

## For a complete WindowGlass-themed UI, download the following mods and use the 'WindowGlass' theme:
- Windows 11 Taskbar Styler - for styling the taskbar.
- Windows 11 Notification Center Styler - for styling the Notification Center and Action Center.
- Windows 11 File Explorer Styler - for styling Windows Explorer windows.
- Windows 11 Start Menu Styler - for styling the Windows 11 Start Menu.

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
styleConstants:
  - Glass=<WindhawkBlur BlurAmount="3" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Frosted=<WindhawkBlur BlurAmount="20" TintColor="{ThemeResource SystemChromeMediumColor}" TintOpacity="0.7" />
  - Acrylic=<AcrylicBrush TintColor="{ThemeResource SystemChromeAltHighColor}" TintOpacity="0.3" FallbackColor="{ThemeResource SystemChromeAltHighColor}" />
  - BorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="0.0" /><GradientStop Color="#50404040" Offset="0.25" /><GradientStop Color="#50808080" Offset="1" /></LinearGradientBrush>
  - BorderBrush2=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="{ThemeResource SystemChromeHighColor}" Offset="0.0" /><GradientStop Color="{ThemeResource SystemChromeLowColor}" Offset="0.15" /><GradientStop Color="{ThemeResource SystemChromeHighColor}" Offset="0.95" /></LinearGradientBrush>
  - overlay=<SolidColorBrush Color="{ThemeResource SystemChromeAltHighColor}" Opacity="0.1" />
  - overlay2=<WindhawkBlur BlurAmount="20" TintColor="#60353535"/>
  - CornerRadius=30
  - CR2=14
  - CR3=12
  - BorderThickness=0.3,1,0.3,0.3
  - ElementBG=<SolidColorBrush Color="{ThemeResource SystemChromeAltHighColor}" Opacity="1" />
  - ElementBorderBrush=<LinearGradientBrush StartPoint="0,0" EndPoint="0,1"><GradientStop Color="#50808080" Offset="1" /><GradientStop Color="#50606060" Offset="0.15" /></LinearGradientBrush>
  - ElementCornerRadius=30
  - ElementBorderThickness=0.3,0.3,0.3,1
  - ElementSysColor=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight1}" Opacity="1" />
  - ElementSysColor2=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight2}" Opacity="1" />
  - ElementSysColor3=<SolidColorBrush Color="{ThemeResource SystemAccentColorLight3}" Opacity="1" />
  - ElementSysColor4=<SolidColorBrush Color="{ThemeResource SystemAccentColorDark1}" Opacity="1" />
  - Backdrop=<AcrylicBrush BackgroundSource="HostBackdrop" TintColor="{ThemeResource SystemChromeAltHighColor}" TintOpacity="0.3" FallbackColor="{ThemeResource SystemChromeAltHighColor}" />
controlStyles:
  - target: Windows.UI.Xaml.Controls.Grid#ContentRoot > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.Grid#ContentGrid
    styles:
      - Background:=$ElementBG
      - BorderBrush:=$ElementBorderBrush
      - CornerRadius=13
      - BorderThickness=$ElementBorderThickness
      - Margin=8,50,8,8
  - target: Windows.UI.Xaml.Controls.RelativePanel#PaneContentGrid > Windows.UI.Xaml.Controls.ContentPresenter
    styles:
      - Background:=$ElementBG
  - target: WinStore.UX.Controls.SearchAutoSuggestBox#SearchBox > Windows.UI.Xaml.Controls.AutoSuggestBox#SearchTextBox > Windows.UI.Xaml.Controls.Grid#LayoutRoot > Windows.UI.Xaml.Controls.TextBox#TextBox > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Border#BorderElement
    styles:
      - CornerRadius=20
  - target: Windows.UI.Xaml.Controls.Grid#ControlPanelGrid
    styles:
      - CornerRadius=$CornerRadius
      - BorderBrush:=$BorderBrush
      - Background:=$Glass
      - BorderThickness=$BorderThickness
      - Width=Auto
      - Margin=100,0,100,-150
      - Height=Auto
      - MaxWidth:=700
      - MinWidth:=15
      - MinHeight:=15
      - MaxHeight:=300
      - HorizontalAlignment=1
      - RenderTransform:=<TranslateTransform X="0" Y="-170"/>
  - target: Windows.UI.Xaml.Controls.Primitives.ToggleButton#mtcMediaInformationButton
    styles:
      - CornerRadius=$CornerRadius
      - Padding=10
      - Margin=20,0,0,0
  - target: Windows.UI.Xaml.Controls.Border#MediaTransportControls_Timeline_Border
    styles:
      - RenderTransform:=<TranslateTransform Y="25"/>
  - target: Windows.UI.Xaml.Controls.Primitives.ToggleButton#mtcMediaInformationButton > Windows.UI.Xaml.Controls.ContentPresenter#ContentPresenter
    styles:
      - RenderTransform:=<TranslateTransform Y="25"/>
  - target: Windows.UI.Xaml.Controls.StackPanel#MediaControlsCommandBar_Center_Container
    styles:
      - RenderTransform:=<TranslateTransform Y="25"/>
  - target: Windows.UI.Xaml.Controls.Border#MediaControlsCommandBar_Right
    styles:
      - RenderTransform:=<TranslateTransform Y="25"/>
      - Margin=0,0,20,0
  - target: Windows.UI.Xaml.Controls.Grid#ContentRoot > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Controls.Grid#ContentGrid
    styles:
      - Background:=$MainContentBG
      - CornerRadius=0
      - Margin=0
      - BorderBrush:=$ElementBorderBrush
  - target: Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:=$$Frosted
      - BorderBrush=$BorderBrush
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Shapes.Ellipse#SliderInnerThumb
    styles:
      - Visibility=1
  - target: Windows.UI.Xaml.Controls.Grid#SliderContainer > Windows.UI.Xaml.Controls.Grid#HorizontalTemplate > Windows.UI.Xaml.Controls.Primitives.Thumb#HorizontalThumb
    styles:
      - Height=20
      - Width=30
  - target: Windows.UI.Xaml.Controls.Primitives.Thumb#VerticalThumb > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:=$Frosted
      - BorderBrush=$BorderBrush
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.Primitives.Thumb#VerticalThumb > Windows.UI.Xaml.Controls.Border > Windows.UI.Xaml.Shapes.Ellipse#SliderInnerThumb
    styles:
      - Visibility=1
  - target: Windows.UI.Xaml.Controls.Grid#SliderContainer > Windows.UI.Xaml.Controls.Grid#VerticalTemplate > Windows.UI.Xaml.Controls.Primitives.Thumb#VerticalThumb
    styles:
      - Height=30
      - Width=20
  - target: Windows.UI.Xaml.Controls.Border#BackgroundElement
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
      - BorderThickness:=0
      - CornerRadius:=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Border#BackgroundElement > Windows.UI.Xaml.Controls.Grid#DialogSpace
    styles:
      - Background:=$Frosted
      - BorderBrush:=$BorderBrush
      - BorderThickness:=$BorderThickness
      - CornerRadius:=$CornerRadius
  - target: Windows.UI.Xaml.Controls.Border#BackgroundElement > Windows.UI.Xaml.Controls.Grid#DialogSpace > Windows.UI.Xaml.Controls.Grid#CommandSpace
    styles:
      - Background:=Transparent
      - BorderBrush:=Transparent
  - target: Windows.UI.Xaml.Controls.ToggleSwitch > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#OuterBorder
    styles:
      - Height=22
      - Width=50
      - RadiusX=10
      - RadiusY=10
      - Stroke:=$ElementSysColor2
  - target: Windows.UI.Xaml.Controls.ToggleSwitch > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Controls.Grid > Windows.UI.Xaml.Shapes.Rectangle#SwitchKnobBounds
    styles:
      - Height=22
      - Width=50
      - RadiusX=10
      - RadiusY=10
  - target: Windows.UI.Xaml.Controls.Grid#SwitchKnob
    styles:
      - Height=20
      - Width=32
  - target: Windows.UI.Xaml.Controls.Grid#SwitchKnob > Windows.UI.Xaml.Controls.Border#SwitchKnobOn
    styles:
      - Height=19
      - Width=26
      - CornerRadius=8
      - Background:=$ElementSysColor
  - target: Windows.UI.Xaml.Controls.Grid#SwitchKnob > Windows.UI.Xaml.Shapes.Rectangle#SwitchKnobOff
    styles:
      - Height=17
      - Width=25
      - RadiusX=8
      - RadiusY=8
      - Fill:=$ElementSysColor
  - target: Windows.UI.Xaml.Controls.FlyoutPresenter
    styles:
      - Background:=$Frosted
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.MenuFlyoutPresenter > Windows.UI.Xaml.Controls.Border
    styles:
      - Background:=$Frosted
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.ToolTip > Windows.UI.Xaml.Controls.ContentPresenter#LayoutRoot
    styles:
      - Background:=$Frosted
      - BorderBrush:=$BorderBrush
      - CornerRadius=$CornerRadius
      - BorderThickness=$BorderThickness
  - target: Windows.UI.Xaml.Controls.Canvas > Windows.UI.Xaml.Controls.Border#PopupBorder
    styles:
      - Background:=$Frosted
      - BorderBrush:=$BorderBrush
      - BorderThickness=$BorderThickness
      - CornerRadius=$CornerRadius
```
</details>
