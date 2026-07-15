![image](https://misc-assets.raycast.com/releases/d6950772d00dc557f22bb22e3647bd05388e58a8e55e7b16fb394f4d2cb42291.png)

File Search can now help you find files by their text contents.

If you want to quickly find that essay, source file or text document that you know contains a word or phrase but can’t quite remember the file name, just type the text in Root Search or File Search.

**To enable Content Search toggle it on in Settings > File Search.** After this content-based results will appear after any name or path results in File Search.

This is the first step in making File Search even more powerful and we aim to bring further improvements specifically to Content Search in the future.

## ✨ New

-   **AI**: AI can ask you multiple choice questions through the Ask User Question tool when requiring extra information or when it’s not certain about something
-   **AI Chat**: Long user messages collapse to take less space away with ability to expand them when needed
-   **File Search**: You can now search contents of text documents from within File Search and Root Search
-   **File Search**: Settings now have a “Reset to Defaults” button to restore all default Search Scopes and ignore patterns
-   **File Search**: File Search now has a “Enforce Low Disk Space Block” to prevent File Search from indexing if you do not have enough disk space where Raycast is installed
-   **Hyper Key**: Added Secure Input Compatibility mode. When enabled, you can use Hyper Key even in the context of Secure Input (e.g. password fields). While on, right Control shortcuts are reserved for Hyper Key and only Hyper shortcuts (⌃⌥(⇧)⌘) from Raycast will trigger.

## 💎 Improvements

-   **AI**: Resetting AI content zoom to default is now aligned with current Interface Size
-   **File Search**: New File Search index backend which should improve indexing and search performance
-   **Interface Size**: Better aligned traffic light when using large/larger interface sizes
-   **Notes**: Resetting Notes content zoom to default is now aligned with current Interface Size
-   **UI**: Aligned date picker icon/indicator treatment with other selects
-   **Root Search**: Improved width handling of search arguments (inputs and select menus)
-   **System Actions**: The Bluetooth toggle now shows its on/off state in the HUD
-   **Uninstall Applications**: You’re now warned when uninstalling an application that is currently running

## 🐞 Fixes

-   **AI**: Fixed web search results being shown in 2 rows instead of 3 by accident
-   **AI**: Fixed an issue where AI mention icon would sometimes bust-out
-   **AI**: Fixed visual alignment of some tool calls
-   **AI**: Fixed Always on Top not being persisted when continuing a Quick AI chat in AI Chat
-   **Clipboard History**: Fixed an issue with entries created by Warp terminal after dropping an icon in it where we weren’t displaying the copied image correctly
-   **Clipboard History**: Fixed occasional hangs caused by pasteboard item capture
-   **Dictation Settings**: Fixed an issue that prevented scrolling the style dialog when over the textarea
-   **Extensions**: Fixed an issue where list detail content was sometimes cut-off at the bottom
-   **Extensions**: Fixed icon being too small in exception view
-   **HUD**: Fixed the HUD appearing on the wrong Space
-   **Input Sources**: Fixed a freeze when auto-switch input is enabled and IME is active
-   **Menu Bar**: Fixed a bootloop on macOS 27 related to menu bar extensions
-   **Quicklinks**: Fixed Quicklink arguments not being prompted when launched via hotkey
-   **Root Search**: Fixed an issue where in some cases descenders would appear clipped in text in the search field
-   **Root Search**: Fixed an issue where pressing down whilst on the last value of a select search argument would leak out and start navigating the main list
-   **Window Management**: Fixed instant Space switching on macOS 27

![image](https://misc-assets.raycast.com/releases/491a93c17bc7617b69093e3870167ea4daadcc5783ed3bfc8d8e38262ba6b36c.png)

This release introduces a new **Interface Size** setting which lets you scale Raycast interfaces so you can find a comfortable size on your display. Choose one of three sizes available:

-   **Default** — the standard size
-   **Large** — a bit bigger
-   **Larger** — the biggest option

When you change the size, every Raycast window resizes to match, and all Ul elements scale with it, including text, buttons, and fields.

_Note_: Interface Size can also affect the content zoom in Notes and Al Chat windows. If a window's content zoom is smaller than the new interface size, it grows to match. And if you scale Raycast back down while the two sizes are equal, they stay in sync. You can of course still customise those content zoom levels separately.

## ✨ New

-   **Settings**: Added a new I**nterface Size** setting

## 💎 Improvements

-   **AI**: Show richer error messages when completion fails in certain cases
-   **AI Chat**: Pressing Esc only closes history sidebar when in overlay mode
-   **Hyper Key**: Improved diagnostics when Hyper Key is not working because another process is keeping Secure Input active
-   **Raycast Focus**: Added missing _Import Focus Categories_ command and _Export Category_ action in _Search Focus Categories_
-   **UI**: Improved performance of hover state in list views
-   **Root Search**: Store and restore latest dropdown argument values
-   **MCP**: Add support for CIMD

## 🐞 Fixes

-   **AI:** Fix provider icons in the auto model popover wrapping when they shouldn’t
-   **Applications**: Fixed applications not always discovered in sub directories
-   **Dictation**: Fixed occasional crash in the equalizer
-   **Dictation**: Fix Styles hotkey not being cleaned up on deletion
-   **Dictionary**: Fixed blank window for some definitions
-   **Dictionary**: Fixed occasional crash when loading definitions
-   **File Search:** Better handling of mixed Latin and CJK filenames
-   **Raycast Focus**: Fixed “Restore Terminated Apps” not restoring apps after the session ends
-   **Root Search**: Fixed an issue where selection was wrongly preserved after a item stopped being suggested
-   **Snippets**: Fixed expansion mis deleting the keyword in some editors
-   **Snippets**: Fixed the _{cursor}_ placeholder landing in the wrong position in some editors
-   **Updater**: Added privileged daemon process to ease updates for non admin users. If you’re in that case, you’ll be prompted to authorize the daemon in System Settings > Login Items & Extensions > App Background Activity. Once authorized, you can update it manually without entering admin credentials anymore.

![image](https://misc-assets.raycast.com/releases/df278eef221eeef8a0ea07def6e9be619d4eec451902ac3a6edd6bbfc036e392.png)

Introducing in-place behavior for custom commands in Raycast. Choose whether to open and run a command in Raycast, or automatically replace selected text with the output. It’s a faster, more flexible workflow for translation and AI-powered commands, built to fit the way you work.

## ✨ New

-   **AI**: Custom AI commands now have an `Output Behavior` setting, so you can choose to open them in Raycast or replace selected text in place
-   **Translator**: Custom translate commands now have an `Output Behavior` setting, so you can choose to open them in Raycast or replace selected text in place
-   **Manual**: New Open Manual and Ask Manual commands
-   **Focus**: New `@raycast-focus` AI Extension to manage a focus session or explore past sessions activity

## 💎 Improvements

-   **AI**: Removed flashes of incorrectly parsed content during streaming
-   **AI**: All AI Modes now show their details in model switchers and models not available in the current subscription now lead to the subscription upgrade view
-   **AI**: Improved retry logic for failed requests
-   **AI**: Browser extension improvements for fetching the currently active tab
-   **AI Chat**: Added zoom support for AI content
-   **AI Chat**: Added rename chat action to action panel
-   **AI Chat**: Improved task-list rendering
-   **Dictation**: Using the “Copy to Clipboard” output mode no longer adds transcriptions to Clipboard History
-   **Dictation**: Allow pasting of comma separated items into vocabulary, accessible via the Vocabulary command or settings
-   **Focus**: Add support for Brave Origin browser
-   **Root Search**: Improved search latency when Contacts are included in root search
-   **Search Menu Bar Items**: Prioritized pinned menu bar items over other items when searching

## 🐞 Fixes

-   **AI Chat**: Prevented collapsing/expanding folder when renaming a chat inline
-   **AI Chat**: Fixed double-click on chat in sidebar not triggering chat rename
-   **Apple Shortcuts**: Fixed missing Apple Shortcuts and improve fallback when `Shortcuts Events` privacy permission is missing
-   **Clipboard History:** Fixed hangs when ingesting data from Universal Clipboard
-   **Core**: Ensured the Raycast window’s cached position remains within the screen bounds
-   **Core**: Fixed ⌘+Escape being swallowed by Raycast when ⌘+Tab window is frontmost
-   **Core:** Fixed hotkey reset after an app updates or is otherwise removed then re-added
-   **Dictionary**: Fixed regression showing a non-interactive button in the nav
-   **Dictionary**: Fixed an issue where certain definition results led to an empty detail view
-   **File Search:** Multiple queries are no longer emitted as you type
-   **File Search:** While a new search query fetches results, existing results are no longer cleared
-   **File Search:** “Recent Files” is now more accurate, fixed an issue with incorrect parsing of xattr dates
-   **Golden Gate**: Fixed corner radius of most windows
-   **Root Search:** File URLs now correctly resolve filesystem entries if they exist
-   **Snippets**: Fixed snippet not expanding for some users missing accessibility entitlement in subprocess
-   **Snippets**: Fixed snippet keyword not replaced in Terminal
-   **Snippets:** Fixed snippet timeout when the target application is slow to handle paste operation
-   **Theme Studio**: Fixed color editor UX (sliders not displaying correct colors)
-   **AI**: Fixed attachment error messages not being surfaced
-   **Window Management:** Layouts now work correctly with multiple displays
-   **Updates**: Fixed an issue where updates requiring elevated permissions could fail to install

![image](https://misc-assets.raycast.com/releases/9b8d056ba4ae8a054084e94785d3faf8b781c017fe317dde008846e29740c23d.png)

[Raycast Focus](https://raycast.com/focus) is back to help you achieve your goals without distractions. Simply use the “Start Focus Session” command to get started. Set a goal, define the duration you want to work on it, and select the apps and websites you want to block.

Learn how to get the most out of the feature with our [manual](https://manual.raycast.com/focus).

## ✨ New

-   **Focus:** Begin a session that shuts out distracting apps and websites with `Start Focus Session`.
-   **Focus:** `Edit Focus Session` adjusts the duration or blocked categories while a session is running.
-   **Focus:** Use `Pause Focus Session` , `Resume Focus Session` and `Complete Focus Session` to control current session.
-   **Focus:** `Toggle Focus Session` starts or stops focusing with a single command, useful for a hotkey.
-   **Focus:** Group the apps and sites that derail you into a reusable set using `Create Focus Category`, then review or change them with Search Focus Categories.

## 💎 Improvements

-   **AI**: Improved usability of Create AI Command view
-   **AI**: Markdown streaming is more stable with reduced flashes of incorrectly parsed content
-   **AI**: Tool call permission description is parsed as Markdown, allowing for richer content
-   **AI Chat**: Improved chat sidebar animation
-   **AI Chat**: Improved chat sidebar handling of collapsed state and navigation
-   **Clipboard History:** Better query matching for non-Latin alphabets (e.g. Cyrillic, CJK)
-   **Clipboard History**: Improved UX of "… and Keep Window Open" actions by delaying the state update so items aren't reordered yet
-   **File Search:** Paths ending with a slash in Browsing mode no longer display the folder as the top result
-   **Quicklinks**: Prefer Existing Tabs setting now supports more Chromium and WebKit browsers
-   **Search Menu Bar Items:** Grouped searched menu bar items into a single section
-   **Snippets:** Improved snippet expansion reliability and accuracy. Faster expansion when snippets are expanded within Raycast. More accurate {cursor} placeholder placement.
-   **System**: Add ability to skip confirmation for emptying the trash
-   **Core:** Improved hotkey conflict detection
-   **Core:** Hotkey conflict indicators appear in root search, _Shortcuts_ settings
-   **Core:** Command hotkeys are now unregistered when an extension is disabled
-   **Search Menu Items:** Added support for disabling specific applications
-   **Search Menu Items:** Search results are now displayed in a single group to improve discovery
-   **Root Search:** Contacts now have an _Open in Search Contacts_ primary action

## 🐞 Fixes

-   **AI Chat**: Removed flicker when searching through chats in sidebar
-   **AI Chat**: Made sidebar peek trigger more conservatively to prevent accidental activations
-   **AI Chat**: Fixed possibility to accidentally trigger sidebar peek while a menu is open
-   **Clipboard History**: Fixed copying large amount of text from a Raycast action (like Copy Chat) slowing down Clipboard History
-   **Core:** Fixed the main window appearing on the edge of another screen instead of the screen containing the mouse cursor
-   **Dictionary**: Fixed font rendering regression
-   **Extensions**: Fixed markdown in detail views not being selectable
-   **Extensions**: Fixed an issue where uninstalling an extension wouldn't instantly remove the commands in Root Search
-   **File Search:** Fixed issues with ignore files not being respected during incremental indexing
-   **File Search:** Fixed an issue preventing indexed files from being returned as part of the result set
-   **File Search**: Fixed an issue where we were attempting to preview database files which crashed File Search
-   **Root Search:** Fixed space key being swallowed during root search loading
-   **Script Commands:** Fixed AppleScript created with “Create Script Command” not being indexed
-   **Settings:** Fixed Escape closing the window instead of dismissing an opened alert
-   **Settings**: Fixed menus showing “Default” value accessory truncating their content
-   **Settings**: Removed duplicate settings for a few items (quitting apps, etc)
-   **Settings**: Added missing settings for resetting confirmation warnings (deleting chats, Quicklinks, Snippets, etc)
-   **UI**: Fixed an issue with open Select breaking some layouts
-   **Window Management:** Commands now work correctly when _Displays have separate Spaces_ is off
-   **Import:** Applications in `~/Applications` are now imported correctly from v1
-   **Import:** Added support for various Calendar settings previously missing from v1 import
-   **Import:** Added support for importing rich text from v1 snippets

![image](https://misc-assets.raycast.com/releases/2278ce96d04862055e323edfab35aa43a637df814f9de0c1967c3a7547e80fce.png)

Teams can now share AI Agents, AI Commands, and Dictation Styles across the organization, making it easier to give everyone access to the same setups and work more consistently.

## ✨ New

-   **Clipboard History**: Added new setting for “Prefer pasting as plain text”
-   **Clipboard History**: Copy text from QR code action for images
-   **Teams:** Share AI Agents across your organization
-   **Teams:** Share AI Commands with your whole team
-   **Teams:** Share Dictation Styles with everyone in your organization

## 💎 Improvements

-   **AI Chat**: Active chat is always preserved when closing AI Chat while streaming, irrespective of “start new chat” setting
-   **Dictation**: Improved the startup performance when using dictation, so your dictation responds even faster to pressing the hotkey
-   **Hotkeys:** Support for standalone navigation keys (Home, Insert, End, Page Up, Page Down)
-   **OCR:** Improved text recognition for small texts in Search Screenshots and Clipboard History
-   **Root Search**: Improved non-selected states of special items (calculator, color, etc)
-   **Root Search**: Improved ranking for previously used search terms

## 🐞 Fixes

-   **AI**: Fixed model resetting when changing reasoning effort in certain situations
-   **AI**: Fixed “Send text to AI” opening a new chat instead of using the currently active one
-   **AI Chat**: Fixed auto-loading of chats in the “Recent” section not working in some situations
-   **AI Chat**: Fixed content jumping at the end of AI generation
-   **AI Chat:** Auto-hide AI Chat toolbar in Full-Screen mode
-   **Clipboard History**: Fixed an issue where we unnecessarily showed the `Paste as…` action
-   **Clipboard History:** Fixed a race condition leading to entries not being recorded for some users
-   **Clipboard History:** Fixed stale file-based entries that were not removed when their associated file was deleted
-   **Contacts:** Added caching to improve load performance
-   **Core**: Fixed an issue where text would sometimes get selected when dragging a scrollbar
-   **Extensions**: Fixed an issue in required preferences view where app picker would jump when opened
-   **File Search:** Fixed an issue with infinitely recursive directory trees
-   **File Search:** We no longer index the contents of `.aplibrary`, `.band`, `.fcpbundle`, `.imovielibrary`, `.logicx`, `.migratedaperturelibrary`, `.postlabteam`, `.pvm`, `.sparsebundle` , `.theater`, `.turf` and `.tvlibrary` bundles
-   **Hyper Key:** Improved recovery from a stuck Secure Input state that prevents the app from remapping Caps Lock
-   **Import:** Fixed missing calendar settings when migrating or importing from v1
-   **Notes:** Fixed issue preventing users from creating a new note with the ⌘N shortcut
-   **Quick AI**: Fixed Quick AI not expanding the view in compact mode when logged out
-   **Root Search:** Fixed occasional delay leading to an aliased command no being open with `alias` + `␣` input
-   **Root Search:** Fixed missing Chinese localization in Apps and System Settings
-   **Root Search:** Improved ranking for localized apps and settings when using the non-localized name as the search term (e.g. “Journal” for “ジャーナル”)
-   **Search Screenshots:** Show preview for non downloaded cloud files
-   **Snippet Expansion:** Fixed snippets not expanding in Secure Inputs
-   **Translator:** Fixed translation not working in root search
-   **Typing Practice**: Fixed an issue where starting a new practice from the results view would restart the current one instead
-   **Typing Practice**: Fixed layout breaking with large scores

![image](https://misc-assets.raycast.com/releases/ad7ef5dbe8fee7541ab433a00eee2c9f57d7d0b06538f2d26841ae583e50dabb.png)

Color conversion is now in Raycast v2! Type any supported color value in root search to get an instant visual preview, and copy it in the format you need. Supports `hex`, `rgb`, `hsl`, `oklch`, and more.

## ✨ New

-   **Calculator:** Enable color conversion from Calculator settings to start surfacing color results in root search
-   **Calculator**: Type or paste any color value in root search to see an instant preview
-   **Calculator**: Copy a converted color in any format — hex, rgb, hsl, modern color spaces, plus NSColor/UIColor for Swift
-   **AI Settings**: Added ability to globally disable AI models to Settings > AI > Models
-   **AI Chat**: Added File Search extension for querying indexed files
-   **File Search**: Added “Open In Finder” command when entering a file path in the root search

## 💎 Improvements

-   **Dictation**: The hotkey for accepting/cancelling dictation can now be configured to require the primary modifier key
-   **Notes:** Add zoom support for Notes window
-   **Emoji Picker & Search Screenshots:** Add zoom support to customize grid size
-   **Calendar:** Add missing _Open Link_ action for events
-   **Calendar**: Parse “safe links” to get the meeting urls
-   **Quicklinks**: Improve support for quicklinks to Raycast deeplinks
-   **Store**: Added support for filtering by “Installed” extensions
-   **Search Screenshots:** Show preview for offline iCloud images
-   **Clipboard:** Remove stale clipboard entries

## 🐞 Fixes

-   **AI Chat**: Fixed the AI extension alignment
-   **Clipboard History:** Fix OCR processing for HEIC/HEIF screenshots
-   **Core:** Improve cold start for built-in commands such as Search Emojis & Symbols, Clipboard History…
-   **Core:** Recover stuck Secure Input after app switches
-   **Core:** Activate target application when using the Paste action
-   **Core:** Fix lag when searching if an extension refresh request times out
-   **Contacts:** Improve performance when loading large numbers of contacts
-   **Dictation**: Fix an issue with audio format conversion causing static for some users
-   **Dictation**: Fix the incorrect model naming convention and missing style application/website count in the Search Styles command
-   **Dictation**: Fix the context menu on the Dictation Pill not opening the correct screens
-   **Notes:** Fix key presses targeting previously focused application rather than the Notes window
-   **Hotkeys:** Fix Raycast hotkey not dismissing Raycast window
-   **Root Search:** Fix localization in some languages for applications and System Settings
-   **Settings:** Focus sidebar navigation when the window is opened
-   **Snippet Expansion:** Fix occasional crash on text field deletion
-   **Translator**: Show source text in the target panel when the source and target languages are the same
-   **Script Commands**: Handle ANSI output
-   **Core:** Avoid duplicate calendar events in root search
-   **Core:** Improve root search ranking
-   **API:** Fix `getWindowsOnActiveDesktop()`
-   **Window Management:** Fix move-to-previous/next space on macOS 26.5
-   **Snippets:** Improve expansion reliability in some circumstances

![image](https://misc-assets.raycast.com/releases/cd9d6becfb3c28cf56514b16dc6e9cb3147be2cb58964b7aa071379097ac8cc3.png)

Introducing the Quick Fix command. It takes your selected text, fixes spelling and grammar, and pastes back the corrected text. The first time you use the command, a little onboarding guide helps you set a hotkey. Our team likes to use the right Shift key for it.

## ✨ New

-   **AI**: New `Quick Fix` command to quickly fix spelling
-   **AI**: New settings to configure the default model for each AI feature

## 💎 Improvements

-   **AI Chat**: Improved startup and window reveal performance
-   **AI Chat**: Added line wrapping for code blocks
-   **AI Chat**: Added native full-screen support for the non-floating AI Chat window
-   **Core**: Improved text rendering
-   **Core**: Improved liquid glass controls when the window is blurred
-   **Dictation**: Added support for dictation in root search
-   **Dictation**: Improved cancellation behavior
-   **Dictation**: Added Dia, Helium, Zen, and Orion browser support for Styles
-   **Settings**: Improved Switch component states/interactions
-   **Script Commands**: Script command output is now selectable
-   **Store**: Improved stability of Store results while loading
-   **Translate**: Use Selected Text as Source now works via root search as well as via hotkey
-   **Window Management**: Add support for Quick Look panels
-   **General:** Reduced memory usage for app icons

## 🐞 Fixes

-   **AI Chat**: Fixed selecting reasoning effort resetting model
-   **AI Chat**: Fixed indented markdown rendering
-   **AI Chat**: Fixed new chats opening blank after triggering an AI Command
-   **AI Chat**: Fixed drafts not preserving newlines
-   **AI Chat**: Fixed scrolling to the wrong position after sending a message
-   **AI Chat**: Fixed tab order in the chat UI
-   **AI Chat**: Fixed pagination cursor overlap
-   **Applications:** Use alternate name for Creator Studio apps
-   **Calendar:** Google Meet meeting URLs now include the calendar account email
-   **Core**: Prevent default right-click menu inside popovers
-   **Core:** Allow running several instances of Raycast with different users in the context of Fast User Switching
-   **Clipboard History:** Fix missing _Open With_ and _Show in Finder_ actions for some images
-   **Clipboard History:** Improve reliability for restricted user accounts
-   **Dictionary**: Fixed duplicates in filter panel
-   **Dictation**: Fixed statistics display for large values
-   **Extensions**: Fixed menu bar items not using the system appearance
-   **File Search**: Improved search for files and directories using non-Latin alphabets
-   **File Search**: Fixed an issue which could cause searches to hang the Raycast UI
-   **General:** Fix issues using Raycast v2 in multi-user environments
-   **Hotkey Recorder**: Fixed **L⌥** + **R⌥** (or any other modifier) not triggering a double tap hotkey **⌥⌥**
-   **Hotkey Recorder**: Fixed **⌥⌥** hotkey triggered when pressing **⌥+Space** twice
-   **Hotkeys**: Fixed an issue which had hotkeys for disabled commands still respond
-   **Hotkeys**: Fixed hotkey registration when re-enabling a command
-   **Hyper Key:** Improve reliability after restoring from secure input or lock screen
-   **Import:** Improved reliability of Snippet keyword registration after import
-   **Import:** Fix missing open-with application after importing Quicklinks from v1
-   **Import:** Fix occasional hang when running the v1 migration
-   **Menu Bar:** Fix crash when toggling Menu Bar commands
-   **Onboarding**: Tweaked copy of transfer setup to show correct command name
-   **Permissions**: Improved handling of Calendar and Contacts permissions
-   **Permissions:** Fixed an issue where Raycast would not open System Settings when requesting access for a denied permission
-   **Root Search**: Fixed flickering empty state while typing
-   **Root Search**: Fixed duplicate script commands breaking root search list
-   **Root Search**: Renamed "Preferences" section to "System Settings"
-   **Root Search**: Fixed an issue where wrong command ids would show up in HUD after favoriting
-   **Settings**: Fixed double padding issue in Shortcuts settings view
-   **Settings**: Fixed scrollbar not updating when expanding/collapsing sections in Shortcuts settings view
-   **Settings**: Fixed Switch rendering on non-retina displays
-   **Updater:** Surface more detailed error when the updater fails
-   **Window Management:** Improved reliability and silenced some spurious warnings

![image](https://misc-assets.raycast.com/releases/072da6c924397ece2d4dfb7709abb6d0ad9393c4476e034d19505fe00574e6b0.png)

The next generation of Raycast is here 🎉 A new foundation, redesigned from the inside out. Today we are transitioning into public beta, and we are excited for everyone to [try it out.](http://raycast.com/new)

The new Raycast Beta installs next to your current Raycast because a few features are still being built. Use both until everything you need is in v2. During onboarding, you'll be able to import your existing Raycast setup so everything feels familiar to you.

Read the full announcement on our [blog](http://raycast.com/blog/the-new-raycast) and you can read about everything new in v2 in our [manual](https://manual.raycast.com/new-in-v2).

## 🐞 Fixes

-   **Applications:** Use alternate name for Creator Studio apps
-   **Calendar:** Google Meet meeting URLs now include the calendar account email
-   **Clipboard History:** Fix missing _Open With_ and _Show in Finder_ actions for some images
-   **Clipboard History:** Improve reliability for restricted user accounts
-   **General:** Fix issues using Raycast v2 in multi-user environments
-   **HyperKey:** Improve reliability after restoring from secure input or lock screen
-   **Import:** Improved reliability of Snippet keyword registration after import
-   **Import:** Fix missing open-with application after importing Quicklinks from v1
-   **Import:** Fix occasional hang when running the v1 migration
-   **Menu Bar:** Fix crash when toggling Menu Bar commands
-   **Permissions**: Improved handling of Calendar and Contacts permissions
-   **Permissions:** Fixed an issue where Raycast would not open System Settings when requesting access for a denied permission
-   **Updater:** Surface more detailed error when the updater fails
-   **Window Management:** Improved reliability and silenced some spurious warnings

![image](https://misc-assets.raycast.com/releases/84d8bfb4c82cbee0d1bb90ded3ff7b420464330efe183f1b0ae992c10bd7de34.png)

Finally, we built search for Raycast Settings. Quickly find extensions, commands and settings without having to remember where everything is 🎉.

## ✨ New

-   **Onboarding:** Experience a brand new onboarding flow as a first time Raycast user, or choose to migrate from the previous version of Raycast as an existing user with the migration flow.
-   **Settings Search:** Press `⌘F` and search for anything - this can be extension, commands, or settings and quickly navigate around to find what you’re looking for.
-   **Dictation**: Added Push to Talk support for Dictate to Note
-   **Dictation**: Added Push to Talk support for transcription styles
-   **AI Extensions**: Added Raycast Notes AI Extension

## 💎 Improvements

-   **AI**: Better error handling for remote tools
-   **AI Chat**: Improved startup performance of AI Chat window
-   **AI Settings**: Added a dedicated page for models with configurable defaults
-   **Dictation:** Added support for function keys
-   **Dictation**: Keyterms now load in AI Chat, Quick AI, and AI Command transcription
-   **Dictation**: Added an alert when canceling dictation after 15 seconds
-   **Dictation**: Added faster retry when a dictation failed
-   **Dictation**: Made cancelation behavior smoother
-   **Clipboard History:** Improved detection of excluded applications
-   **My Schedule:** Date formatting now respects the current locale
-   **Quicklinks:** Added _Paste Selected Text as Argument_ option to insert select text in an argument placeholder when the Quicklink is invoked by hotkey
-   **Root Search**: Number hotkeys (e.g. `⌘2`) are now supported in compact mode too
-   **Settings:** Quicklinks are now grouped by organization in settings
-   **Settings:** Menu bar commands are now clearly grouped in extension settings
-   **Settings:** Improved grouping of custom Window Management commands

## 🐞 Fixes

-   **AI Chat**: Fixed composer losing new lines when closing and re-opening AI Chat window
-   **AI Chat**: Fixed moving to incorrect scroll position sometimes when submitting a new message
-   **AI Chat and Quick AI**: Fixed an issue that made it difficult to select the first line of code in a multiline code block
-   **AI Chat**: Fixed an issue with AI Chat showing messages twice in rare scenarios
-   **Calendar:** improved handling of events from subscribed calendars
-   **Calendar:** Auto-join alert should not be presented when enabling the feature during an in-progress meeting
-   **Core**: Fixed a flickering issue of blurred state when first opening any window
-   **Core**: Fixed Raycast not being notified when upgrading to Pro or Advanced AI
-   **Emoji Picker**: Fixed `Paste and Keep Window Open` shortcut
-   **Export:** AI transcriptions and AI Chat folders added to exporter
-   **Import**: Fixed import of double-tap hotkeys from v1
-   **Import**: Improved handling of large `rayconfig` files when importing from v1
-   **Import:** Adding missing commands when importing from v1
-   **Import:** Fixed incorrect import of Script Command search directories from iCloud Drive
-   **Hyper Key: E**nsure Shift isn’t suppressed when Hyper Key is using another modifier key than Shift (e.g. Right Command)
-   **Snippets:** Fix inconsistencies between snippets expanded with keywords and snippets pasted from the Search Snippets
-   **Script Commands**: Fixed passing arguments to silent scripts
-   **Script Commands**: Fixed passing arguments via deeplinks
-   **Script Commands**: Immediately close the window when running a silent script
-   **Extensions**: Fixed an issue where consecutive hotkeys for extensions wouldn’t hide the window

![image](https://misc-assets.raycast.com/releases/e05605fe8a698a94eceb1b9b19a1411a58b4a01b85c4eb86b2d6b08a0c173dd8.png)

## 💎 Improvements

-   **Auto-Quit**: Simplified UX of Auto-Quit Applications in settings
-   **Clipboard History**: Improved color categorization when copying unqualified hex codes from design apps
-   **Clipboard History**: Improved rendering performance of long unbroken strings in text previews
-   **Clipboard History**: Improved image entries title generation by adding the image dimensions
-   **Dictation**: Added support for function keys and single-tap modifiers as hotkeys
-   **Root Search**: Simplified file browsing UX by automatically moving into File Search

## 🐞 Fixes

-   **Clipboard History**: Fixed an issue where some empty entries could be created
-   **Clipboard History**: Fixed an issue where copying a frame as PNG from Figma would not display the image entry correctly
-   **Clipboard History**: Fixed an issue where pasting an image into Claude Code in Ghostty only pasted “v”
-   **Clipboard History:** Fixed an issue where Automatic Text Recognition (OCR) failed on some images, preventing them from being found through their text content
-   **Core**: Fixed many internal extensions bypassing Raycast clipboard when copying to clipboard
-   **Menu Bar Extensions**: Fixed 100% CPU usage in some conditions where menu bar extensions are visible
-   **Notes**: Fixed a regression where the theme background was doubled, thus creating stronger coloring
-   **Window Capture**: Fixed Window Capture command capturing only the sheet instead of the full window when a sheet is open