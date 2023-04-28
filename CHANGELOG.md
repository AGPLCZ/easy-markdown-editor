# EasyMDE Changelog

All notable changes to EasyMDE will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com),
and this project adheres to [Semantic Versioning](https://semver.org).

## [Unreleased]

### BREAKING CHANGES

-   Complete rewrite of the editor. API has changed significantly, please see the [migration guide](TBD).

## [2.18.0] - 2022-09-20

### Added

-   `toolbarButtonClassPrefix` option to resolve conflicts with Bootstrap classes ([#493]).

## [2.17.0] - 2022-08-20

### Added

-   Improved CSRF support for uploading images (Thanks to [@ZsgsDesign], [#394]).
-   Option to register an image preview handler: `imagesPreviewHandler` (Thanks to [@diego-gw], [#411]).
-   Support for `.webp` image formats (Thanks to [@sghoweri], [#417]).
-   `toggleHeading` methods for headings 4, 5 and 6 (Thanks to [@vanillajonathan], [#449] and [#492]).
-   Support for `.gif`, `.avif` and `.apng` image formats (Thanks to [@vanillajonathan], [#450], [#458] and [#459]).
-   Keyboard shortcuts for `toggleHeading` methods (Thanks to [@vanillajonathan], [#451]).
-   `iconClassMap` option to specify icon class names for toolbar buttons (Thanks to [@vanillajonathan], [#454]).
-   `role="toolbar"` on the toolbar element (Thanks to [@vanillajonathan], [#455]).
-   Support for text buttons in the toolbar (Thanks to [@vanillajonathan], [#461]).
-   `aria-label` attribute for toolbar buttons (uses the `title` option) (Thanks to [@vanillajonathan], [#463]).
-   `role="application"` on the editor container element (Thanks to [@vanillajonathan], [#464]).
-   Option to not overwrite the preview HTML by returning `null` from `previewRender` (Thanks to [@LevitatingOrange], [#471]).

### Fixed

-   Hyperlink doubling (Thanks to [@danielok1993], [#95]).
-   URLs with certain characters entered through prompts causing invalid markdown (Thanks to [@Zignature], [#393]).
-   Autofocus option not working properly ([#399]).
-   Inconsistent border colour (Thanks to [@vanillajonathan], [#466]).
-   Invalid regex on Safari browsers ([#478])
-   `hideIcons` option type (Thanks to [@LoyalPotato], [#488]).

### Changed

-   Editor now uses responsive font sizes (Thanks to [@vanillajonathan], [#452]).

### Documentation

-   Added several improvements to README (Thanks to [@vanillajonathan], [#436], [#438], [#440], [#444]).
-   Fixed typo in README (Thanks to [@kicksent], [#484]).
-   Added missing icon for `upload-image` in README (Thanks to [@hlf20010508], [#486]).

## [2.16.1] - 2022-01-14

### Fixed

-   Incorrect initial line and column count in status bar.
-   Security issue in `marked` dependency.

## [2.16.0] - 2022-01-11

### Added

-   `direction` option to enable RTL mode (Thanks to [@souljuse], [#358]).
-   `attributes` option to add custom attributes to toolbar buttons (Thanks to [@Zignature], [#388]).
-   `unorderedListStyle` option to change the character used for unordered lists (Thanks to [@Zignature], [#389]).

### Fixed

-   Image extension detection when extension is uppercase (Thanks to [@ukjinjang], [#357]).
-   Submenu actions not working in Chromium Browsers (Thanks to [@Offerel], [@robjean9] and [@kelvinj], [#364]).
-   Incorrect line and column count in status bar (Thanks to [@Zignature], [#384]).

## [2.15.0] - 2021-04-22

### Added

-   `imagePathAbsolute` option to return the absolute path when uploading an image (Thanks to [@wwsalmon], [#313]).

### Fixed

-   `ToolbarIcon` typings, added `icon` (Thanks to [@ChronosMasterOfAllTime], [#308]).
-   Image link extension when it was not the last part of the URL (Thanks to [@deerboy], [#311]).
-   Preview mode did not stay enabled when toggling to fullscreen (Thanks to [@smundro], [#316]).
-   Required typings not being included in `dependencies` (Thanks to [@marekdedic], [#322]).

## [2.14.0] - 2021-02-14

### Added

-   The `scrollbarStyle` option to change the style of the scrollbar (Thanks to [@danice], [#250]).

### Fixed

-   Issues with images not displaying correctly in the preview screen (Thanks to [@ivictbor], [#253]).
-   An error when both `sideBySideFullscreen` and `status` were set to `false` (Thanks to [@joahim], [#272]).
-   Editor trying to display non-image files (Thanks to [@Juupaa], [#277])
-   Unneeded call to `window.removeEventListener` (Thanks to [@emirotin], [#280])
-   Spell checker (Thanks to [@Fanvadar], [#284]).
-   Focus issues with toolbar dropdown menus (Thanks to [@Situphen], [#285]).
-   Interaction between the `sideBySideFullscreen` and the preview state (Thanks to [@smundro], [#286])
-   Refactored strange method of padding the toolbar into regular padding (Thanks to [@sn3p], [#293]).
-   Security issue in `marked` dependency (Thanks to [@dependabot], [#298]).

## [2.13.0] - 2020-11-11

### Added

-   CodeMirror autorefresh plugin and autoRefresh option (Thanks to [@mbolli], [#249]).
-   `lineNumbers` option to display line numbers in the editor (Thanks to [@nhymxu], [#267]).

### Fixed

-   CSS scoping issues when the editor is used in combination with other CodeMirror instances ([#252]).

## [2.12.1] - 2020-10-06

### Changed

-   Set `previewImagesInEditor` option to `false` by default ([#251]).

## [2.12.0] - 2020-09-29

### Added

-   `this` context in imageUploadFunction (Thanks to [@JoshuaLicense], [#225]).
-   `previewImagesInEditor` option to display images in editor mode (Thanks to [@ivictbor], [#235]).
-   `overlayMode` options to supply an additional codemirror mode (Thanks to [@czynskee], [#244]).

### Fixed

-   Corrected default size units from `b,Kb,Mb` to ` B, KB, MB` ([#239]).
-   Max height less than min height (Thanks to [@nick-denry], [#222]).
-   toTextArea issue (Thanks to [@nick-denry], [#223]).
-   Error when updateStatusBar was called during image upload, but the status bar is disabled (Thanks to [@JoshuaLicense], [#224]).

## [2.11.0] - 2020-07-16

### Added

-   Support for Node.js 14.
-   Preview without fullscreen (Thanks to [@nick-denry], [#196]).

### Fixed

-   Fix cursor displayed position on activity (Thanks to [@firm1], [#184]).
-   Checkboxes always have bullets in front of them ([#136]).
-   Save the text only when modifying the content of the easymde instance (Thanks to [@firm1], [#181]).

## [2.10.1] - 2020-04-06

### Fixed

-   Typescript error when entering certain strings for toolbar buttons ([#178]).

## [2.10.0] - 2020-04-02

### Added

-   `inputStyle` and `nativeSpellcheck` options to manage the native language of the browser (Thanks to [@firm1], [#143]).
-   Group buttons in drop-down lists by adding a sub-option `children` for the items in the toolbar (Thanks to [@firm1], [#141]).
-   `sanitizerFunction` option to allow custom HTML sanitizing in the markdown preview (Thanks to [@adamb70], [#147]).
-   Time formatting and custom text options for the autosave message (Thanks to [@dima-bzz], [#170]).

### Changed

-   Delay before assuming that submit of the form as failed is `autosave.submit_delay` instead of `autosave.delay` (Thanks to [@Situphen], [#139]).
-   Add `watch` task for gulp (Thanks to [@A-312], [#150]).

### Fixed

-   Issue with Marked when using IE11 and webpack (Thanks to [@felipefdl], [#169]).
-   Updated codemirror to version 5.52.2 (Thanks to [@A-312], [#173]).
-   Editor displaying on top of other elements on a webpage (Thanks to [@StefKors], [#175]).

## [2.9.0] - 2020-01-13

### Added

-   Missing minHeight option in type definition (Thanks to [@t49tran], [#123]).
-   Other missing type definitions ([#126]).

### Changed

-   The editor will remove its saved contents when the editor is emptied, allowing to reload a default value (Thanks to [@Situphen], [#132]).

## [2.8.0] - 2019-08-20

### Added

-   Upload images functionality (Thanks to [@roipoussiere] and [@JeroenvO], [#71], [#101]).
-   Allow custom image upload function (Thanks to [@sperezp], [#106]).
-   More polish to the upload images functionality (Thanks to [@jfly], [#109]).
-   Improved React compatibility (Thanks to [@richtera], [#97]).

### Fixed

-   Missing link in dist file header.

## [2.7.0] - 2019-07-13

### Added

-   `previewClass` option for overwriting the preview screen class ([#99]).

### Fixed

-   Updated dependencies to resolve potential security issue.
-   Resolved small code style issues shown by new eslint rules.

## [2.6.1] - 2019-06-17

### Fixed

-   Error when toggling between ordered and unordered lists (Thanks to [@roryok], [#93]).
-   Keyboard shortcuts for custom actions not working (Thanks to [@ysykzheng], [#75]).

## [2.6.0] - 2019-04-15

### Added

-   Contributing guide (Thanks to [@roipoussiere], [#54]).
-   Issue templates.
-   Standardized changelog file.

### Changed

-   Finish rewrite of README (Thanks to [@roipoussiere], [#54]).
-   Image and link prompt fill with "https://" by default.
-   Link to markdown guide to <https://www.markdownguide.org/basic-syntax/>.

### Fixed

-   Backwards compatibility in the API with SimpleMDE 1.0.0 ([#41]).
-   Automatic publish of master branch to `@next`

### Removed

-   Distribution files from source-control.

## [2.5.1] - 2019-01-17

### Fixed

-   `role="button"` needed to be `type="button"` ([#45]).

## [2.5.0] - 2019-01-17

### Added

-   Typescript support (Thanks to [@FranklinWhale], [#44]).
-   `role="button"` to toolbar buttons ([#38]).

### Fixed

-   Eraser icon not working with FontAwesome 5.

## [2.4.2] - 2018-11-09

### Added

-   Node.js 11 support.

### Fixed

-   Header button icons not showing sub-icons with FontAwesome 5.
-   Inconsistent autosave behaviour when submitting a form (Thanks to [@Furgas] and [@adamb70], [#31]).

## [2.4.1] - 2018-10-15

### Added

-   `fa-redo` class to redo button for FA5 compatibility (Thanks to [@Summon528], [#27]).

## [2.4.0] - 2018-10-15

### Added

-   Theming support (Thanks to [@LeviticusMB], [#17]).
-   onToggleFullscreen event hook (Thanks to [@n-3-0], [#16]).

### Fixed

-   Fullscreen not working with `toolbar: false` (Thanks to [@aphitiel], [#19]).

## [2.2.2] - 2019-07-03

### Fixed

-   Automatic publish only publishing tags.

## [2.2.1] - 2019-06-29

### Changed

-   Attempt automatic publish `@next` version on npm.
-   Links in the preview window will open in a new tab by default.

### Fixed

-   Multi-text select issue by disabling multi-select in the editor ([#10]).
-   `main` file in package.json (Thanks to [@sne11ius], [#11]).

## [2.0.1] - 2018-05-13

### Changed

-   Rewrote part of the documentation for EasyMDE.
-   Updated gulp to version 4.0.0.

### Fixed

-   Icons for `heading-smaller`, `heading-bigger`, `heading-1`, `heading-2` and `heading-3` not showing ([#9]).

## [2.0.0] - 2018-04-23

Project forked from [SimpleMDE](https://github.com/sparksuite/simplemde-markdown-editor)

### BREAKING CHANGES

-   Dropped Bower support.
-   Dropped support for older Node.js versions.

### Added

-   FontAwesome 5 support.
-   Support for newer Node.js versions.

### Changed

-   Packages are now version-locked.
-   Simplified build script.
-   Markdown guide button is no longer disabled in preview mode.

### Fixed

-   Cursor not always showing in "text" mode over the edit field

<!-- Linked issues -->

[#493]: https://github.com/Ionaru/easy-markdown-editor/issues/493
[#478]: https://github.com/Ionaru/easy-markdown-editor/issues/478
[#399]: https://github.com/Ionaru/easy-markdown-editor/issues/399
[#252]: https://github.com/Ionaru/easy-markdown-editor/issues/252
[#251]: https://github.com/Ionaru/easy-markdown-editor/issues/251
[#239]: https://github.com/Ionaru/easy-markdown-editor/issues/239
[#178]: https://github.com/Ionaru/easy-markdown-editor/issues/178
[#136]: https://github.com/Ionaru/easy-markdown-editor/issues/136
[#126]: https://github.com/Ionaru/easy-markdown-editor/issues/126
[#99]: https://github.com/Ionaru/easy-markdown-editor/issues/99
[#45]: https://github.com/Ionaru/easy-markdown-editor/issues/45
[#44]: https://github.com/Ionaru/easy-markdown-editor/issues/44
[#41]: https://github.com/Ionaru/easy-markdown-editor/issues/41
[#38]: https://github.com/Ionaru/easy-markdown-editor/issues/38
[#17]: https://github.com/Ionaru/easy-markdown-editor/issues/17
[#16]: https://github.com/Ionaru/easy-markdown-editor/issues/16
[#11]: https://github.com/Ionaru/easy-markdown-editor/issues/11
[#10]: https://github.com/Ionaru/easy-markdown-editor/issues/10
[#9]: https://github.com/Ionaru/easy-markdown-editor/issues/9

<!-- Linked PRs -->

[#492]: https://github.com/Ionaru/easy-markdown-editor/pull/492
[#488]: https://github.com/Ionaru/easy-markdown-editor/pull/488
[#486]: https://github.com/Ionaru/easy-markdown-editor/pull/486
[#484]: https://github.com/Ionaru/easy-markdown-editor/pull/484
[#479]: https://github.com/Ionaru/easy-markdown-editor/pull/479
[#471]: https://github.com/Ionaru/easy-markdown-editor/pull/471
[#467]: https://github.com/Ionaru/easy-markdown-editor/pull/467
[#466]: https://github.com/Ionaru/easy-markdown-editor/pull/466
[#464]: https://github.com/Ionaru/easy-markdown-editor/pull/464
[#463]: https://github.com/Ionaru/easy-markdown-editor/pull/463
[#461]: https://github.com/Ionaru/easy-markdown-editor/pull/461
[#459]: https://github.com/Ionaru/easy-markdown-editor/pull/459
[#458]: https://github.com/Ionaru/easy-markdown-editor/pull/458
[#455]: https://github.com/Ionaru/easy-markdown-editor/pull/455
[#454]: https://github.com/Ionaru/easy-markdown-editor/pull/454
[#452]: https://github.com/Ionaru/easy-markdown-editor/pull/452
[#451]: https://github.com/Ionaru/easy-markdown-editor/pull/451
[#450]: https://github.com/Ionaru/easy-markdown-editor/pull/450
[#449]: https://github.com/Ionaru/easy-markdown-editor/pull/449
[#444]: https://github.com/Ionaru/easy-markdown-editor/pull/444
[#440]: https://github.com/Ionaru/easy-markdown-editor/pull/440
[#438]: https://github.com/Ionaru/easy-markdown-editor/pull/438
[#436]: https://github.com/Ionaru/easy-markdown-editor/pull/436
[#417]: https://github.com/Ionaru/easy-markdown-editor/pull/417
[#411]: https://github.com/Ionaru/easy-markdown-editor/pull/411
[#394]: https://github.com/Ionaru/easy-markdown-editor/pull/394
[#393]: https://github.com/Ionaru/easy-markdown-editor/pull/393
[#389]: https://github.com/Ionaru/easy-markdown-editor/pull/389
[#388]: https://github.com/Ionaru/easy-markdown-editor/pull/388
[#384]: https://github.com/Ionaru/easy-markdown-editor/pull/384
[#364]: https://github.com/Ionaru/easy-markdown-editor/pull/364
[#358]: https://github.com/Ionaru/easy-markdown-editor/pull/358
[#357]: https://github.com/Ionaru/easy-markdown-editor/pull/357
[#322]: https://github.com/Ionaru/easy-markdown-editor/pull/322
[#316]: https://github.com/Ionaru/easy-markdown-editor/pull/316
[#313]: https://github.com/Ionaru/easy-markdown-editor/pull/313
[#311]: https://github.com/Ionaru/easy-markdown-editor/pull/311
[#308]: https://github.com/Ionaru/easy-markdown-editor/pull/308
[#298]: https://github.com/Ionaru/easy-markdown-editor/pull/298
[#293]: https://github.com/Ionaru/easy-markdown-editor/pull/293
[#286]: https://github.com/Ionaru/easy-markdown-editor/pull/286
[#285]: https://github.com/Ionaru/easy-markdown-editor/pull/285
[#284]: https://github.com/Ionaru/easy-markdown-editor/pull/284
[#280]: https://github.com/Ionaru/easy-markdown-editor/pull/280
[#277]: https://github.com/Ionaru/easy-markdown-editor/pull/277
[#272]: https://github.com/Ionaru/easy-markdown-editor/pull/272
[#267]: https://github.com/Ionaru/easy-markdown-editor/pull/267
[#253]: https://github.com/Ionaru/easy-markdown-editor/pull/253
[#250]: https://github.com/Ionaru/easy-markdown-editor/pull/250
[#249]: https://github.com/Ionaru/easy-markdown-editor/pull/249
[#244]: https://github.com/Ionaru/easy-markdown-editor/pull/244
[#235]: https://github.com/Ionaru/easy-markdown-editor/pull/235
[#225]: https://github.com/Ionaru/easy-markdown-editor/pull/225
[#224]: https://github.com/Ionaru/easy-markdown-editor/pull/224
[#223]: https://github.com/Ionaru/easy-markdown-editor/pull/223
[#222]: https://github.com/Ionaru/easy-markdown-editor/pull/222
[#196]: https://github.com/Ionaru/easy-markdown-editor/pull/196
[#184]: https://github.com/Ionaru/easy-markdown-editor/pull/184
[#181]: https://github.com/Ionaru/easy-markdown-editor/pull/181
[#175]: https://github.com/Ionaru/easy-markdown-editor/pull/175
[#173]: https://github.com/Ionaru/easy-markdown-editor/pull/173
[#170]: https://github.com/Ionaru/easy-markdown-editor/pull/170
[#169]: https://github.com/Ionaru/easy-markdown-editor/pull/169
[#150]: https://github.com/Ionaru/easy-markdown-editor/pull/150
[#147]: https://github.com/Ionaru/easy-markdown-editor/pull/147
[#143]: https://github.com/Ionaru/easy-markdown-editor/pull/143
[#141]: https://github.com/Ionaru/easy-markdown-editor/pull/141
[#139]: https://github.com/Ionaru/easy-markdown-editor/pull/139
[#132]: https://github.com/Ionaru/easy-markdown-editor/pull/132
[#123]: https://github.com/Ionaru/easy-markdown-editor/pull/123
[#109]: https://github.com/Ionaru/easy-markdown-editor/pull/109
[#106]: https://github.com/Ionaru/easy-markdown-editor/pull/106
[#101]: https://github.com/Ionaru/easy-markdown-editor/pull/101
[#97]: https://github.com/Ionaru/easy-markdown-editor/pull/97
[#95]: https://github.com/Ionaru/easy-markdown-editor/pull/95
[#93]: https://github.com/Ionaru/easy-markdown-editor/pull/93
[#75]: https://github.com/Ionaru/easy-markdown-editor/pull/75
[#71]: https://github.com/Ionaru/easy-markdown-editor/pull/71
[#54]: https://github.com/Ionaru/easy-markdown-editor/pull/54
[#31]: https://github.com/Ionaru/easy-markdown-editor/pull/31
[#27]: https://github.com/Ionaru/easy-markdown-editor/pull/27
[#19]: https://github.com/Ionaru/easy-markdown-editor/pull/19

<!-- Linked users -->

[@dependabot]: https://github.com/dependabot
[@wwsalmon]: https://github.com/wwsalmon
[@ChronosMasterOfAllTime]: https://github.com/ChronosMasterOfAllTime
[@deerboy]: https://github.com/deerboy
[@marekdedic]: https://github.com/marekdedic
[@emirotin]: https://github.com/emirotin
[@smundro]: https://github.com/smundro
[@Juupaa]: https://github.com/Juupaa
[@Fanvadar]: https://github.com/Fanvadar
[@danice]: https://github.com/danice
[@joahim]: https://github.com/joahim
[@nhymxu]: https://github.com/nhymxu
[@mbolli]: https://github.com/mbolli
[@ivictbor]: https://github.com/ivictbor
[@JoshuaLicense]: https://github.com/JoshuaLicense
[@czynskee]: https://github.com/czynskee
[@nick-denry]: https://github.com/nick-denry
[@StefKors]: https://github.com/StefKors
[@felipefdl]: https://github.com/felipefdl
[@A-312]: https://github.com/A-312
[@dima-bzz]: https://github.com/dima-bzz
[@firm1]: https://github.com/firm1
[@Situphen]: https://github.com/Situphen
[@t49tran]: https://github.com/t49tran
[@richtera]: https://github.com/richtera
[@jfly]: https://github.com/jfly
[@sperezp]: https://github.com/sperezp
[@JeroenvO]: https://github.com/JeroenvO
[@sn3p]: https://github.com/sn3p
[@roryok]: https://github.com/roryok
[@ysykzheng]: https://github.com/ysykzheng
[@roipoussiere]: https://github.com/roipoussiere
[@FranklinWhale]: https://github.com/FranklinWhale
[@Furgas]: https://github.com/Furgas
[@adamb70]: https://github.com/adamb70
[@Summon528]: https://github.com/Summon528
[@LeviticusMB]: https://github.com/LeviticusMB
[@n-3-0]: https://github.com/n-3-0
[@aphitiel]: https://github.com/aphitiel
[@sne11ius]: https://github.com/sne11ius
[@souljuse]: https://github.com/souljuse
[@ukjinjang]: https://github.com/ukjinjang
[@robjean9]: https://github.com/robjean9
[@Offerel]: https://github.com/Offerel
[@Zignature]: https://github.com/Zignature
[@kelvinj]: https://github.com/kelvinj
[@diego-gw]: https://github.com/diego-gw
[@danielok1993]: https://github.com/danielok1993
[@vanillajonathan]: https://github.com/vanillajonathan
[@LevitatingOrange]: https://github.com/LevitatingOrange
[@LoyalPotato]: https://github.com/LoyalPotato
[@kicksent]: https://github.com/kicksent
[@hlf20010508]: https://github.com/hlf20010508
[@ZsgsDesign]: https://github.com/ZsgsDesign
[@sghoweri]: https://github.com/sghoweri

<!-- Linked versions -->

[Unreleased]: https://github.com/Ionaru/easy-markdown-editor/compare/2.18.0...HEAD
[2.18.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.17.0...2.18.0
[2.17.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.16.1...2.17.0
[2.16.1]: https://github.com/Ionaru/easy-markdown-editor/compare/2.16.0...2.16.1
[2.16.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.15.0...2.16.0
[2.15.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.14.0...2.15.0
[2.14.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.13.0...2.14.0
[2.13.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.12.1...2.13.0
[2.12.1]: https://github.com/Ionaru/easy-markdown-editor/compare/2.12.0...2.12.1
[2.12.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.11.0...2.12.0
[2.11.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.10.1...2.11.0
[2.10.1]: https://github.com/Ionaru/easy-markdown-editor/compare/2.10.0...2.10.1
[2.10.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.9.0...2.10.0
[2.9.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.8.0...2.9.0
[2.8.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.7.0...2.8.0
[2.7.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.6.1...2.7.0
[2.6.1]: https://github.com/Ionaru/easy-markdown-editor/compare/2.6.0...2.6.1
[2.6.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.5.1...2.6.0
[2.5.1]: https://github.com/Ionaru/easy-markdown-editor/compare/2.5.0...2.5.1
[2.5.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.4.2...2.5.0
[2.4.2]: https://github.com/Ionaru/easy-markdown-editor/compare/2.4.1...2.4.2
[2.4.1]: https://github.com/Ionaru/easy-markdown-editor/compare/2.4.0...2.4.1
[2.4.0]: https://github.com/Ionaru/easy-markdown-editor/compare/2.2.2...2.4.0
[2.2.2]: https://github.com/Ionaru/easy-markdown-editor/compare/2.2.1...2.2.2
[2.2.1]: https://github.com/Ionaru/easy-markdown-editor/compare/2.0.1...2.2.1
[2.0.1]: https://github.com/Ionaru/easy-markdown-editor/compare/2.0.0...2.0.1
[2.0.0]: https://github.com/Ionaru/easy-markdown-editor/compare/1.11.2...2.0.0
