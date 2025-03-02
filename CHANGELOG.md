# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## Unreleased

## [v3.4.0] - 2022-10-03

### Added

- [crunzphp#31] Add format option to `schedule:list`

## [v3.3.0] - 2022-06-19

### Deprecated

- [crunzphp#24] Deprecate non string parameters

## [v3.2.2] - 2022-05-28

### Fixed

- [crunzphp#5] Fix Symfony 6.1 deprecations

## [v3.2.1] - 2022-01-09

### Fixed

- [#401] Fix version number

## [v3.2.0] - 2022-01-09

### Added

- [#398] Add hourlyAt()
- [#390] Symfony 6 Support, thanks to [@bashgeek]

### Changed

- [#396] Remove `opis/closure` and use `laravel/serializable-closure` instead

### Removed

- [#393] Drop Symfony 5.2 support
- [#394] Drop Symfony 5.3 support

## [v3.1.0] - 2021-11-24

### Changed

- [#385] Replace `Swiftmailer` with `symfony/mailer`

## [v3.0.1] - 2021-05-25

### Fixed

- [#361] Log to specific event log file, thanks to [@drjayvee]

## [v2.3.1] - 2021-05-25

### Fixed

- [#361] Log to specific event log file, thanks to [@drjayvee]

## [v3.0.0] - 2021-04-25

### Changed

- [#349] Require at least PHP v7.4
- [#356] Require package "dragonmantank/cron-expression" at least "v3.1"

### Removed

- [#351] Drop Symfony v3.4 support
- [#352] Drop Symfony v5.1 support
- [#354] Remove most "Crunz\Event::every*" methods

## [v2.3.0] - 2021-03-14

### Deprecated

- [#344] Deprecate most "Event::every*" methods

### Removed

- [#323] Drop Symfony 4.3 support
- [#324] Drop Symfony 5.0 support

## [v2.2.4] - 2020-12-18

### Fixed

- [#333] Include symlinks in Finder, thanks to [@iluuu1994]

## [v2.2.3] - 2020-11-29

### Fixed

- [#334] Fix disabling logger not working

## [v2.2.2] - 2020-10-12

### Fixed

- [#326] Fix lock key on closures

## [v2.2.1] - 2020-10-08

### Fixed

- [#321] Add PHP8 support

## [v2.2.0] - 2020-06-18

### Added

- [#287] Add `task:debug` command
- [#233] Add option to ignore empty context in monolog, thanks to [@rrushton]
- [#298] Add `logger_factory` config option

### Removed

- [#292] Drop Symfony 4.2 support

## [v2.1.0] - 2020-02-02

### Added

- [#274] Symfony 5 support

### Changed

- [#240] cron-expression package, thanks to [@mareksuscak]
- [#280] Hide `closure:run` command

## [v2.0.4] - 2019-12-08

### Fixed

- [#268] Fix Symfony 4.4 deprecations

## [v1.12.4] - 2019-12-08

### Fixed

- [#268] Fix Symfony 4.4 deprecations

## [v2.0.3] - 2019-11-17

### Fixed

- [#261] Release lock on error
- [#264] Revert converting closure result to `int`

## [v1.12.3] - 2019-11-17

### Fixed

- [#261] Release lock on error

## [v2.0.2] - 2019-10-06

### Fixed

- [#251] Update PHPUnit to avoid PHP7.4 deprecations 

## [v1.12.2] - 2019-10-05

### Fixed

- [#243] Sandbox task loading
- [#245] Fix PHP 7.4 compatibility

## [v2.0.1] - 2019-05-10

### Fixed

- [#229] Fix recursive tasks scan

## [v1.12.1] - 2019-05-01

### Fixed

- [#229] Fix recursive tasks scan

## [v2.0.0] - 2019-04-24

### Changed

- [#101] Throw exception on empty timezone
- [#204] More than five parts cron expressions will throw exception
- [#221] Throw `Crunz\Task\WrongTaskInstanceException` when task is not `Schedule` instance
- [#222] Make `\Crunz\Event::setProcess` private
- [#225] Bump dependencies

### Removed

- [#103] Removed `Crunz\Output\VerbosityAwareOutput` class
- [#206] Remove legacy paths recognition
- [#224] Remove `mail` transport

## [v1.12.0] - 2019-04-07

### Added

- [#178], [#217] `timezone_log` configuration option to decide whether
configured `timezone` should be used for logs, thanks to [@SadeghPM]

### Deprecated

- Using `\Crunz\Event::setProcess` is deprecated, this method was intended to be `private`,
but for some reason is `public`.
In `v2.0` this method will became private and result in exception if you call it.
- [#199] Not returning `\Crunz\Schedule` instance from your task is deprecated.
In `v2` this will result in exception.

## [v1.11.2] - 2019-03-16

### Fixed

- [#209], [#210] Composer installs crunz executable to vendor/bin instead of symlink

## [v1.11.1] - 2019-01-27

### Fixed

- [#190] Fix Crunz bin path when running closures

## [v1.11.0] - 2019-01-24

### Fixed

- [#181] Fix missing tasks source
- [#180] Fix deprecation messages not showing

### Deprecated

- Relying on tasks' source/config file recognition related to Crunz bin 

## [v1.11.0-rc.1] - 2018-12-22

### Fixed

- [#171] Fix lock storage bug
- [#173] Remove Symfony 4.2 deprecations
- [#166] Improve task collection debugging

## [v1.11.0-beta.2] - 2018-11-10

### Fixed

- [#162] Fix command error output [closes [#161]]

## [v1.11.0-beta.1] - 2018-10-23

### Added

- [#153] Add support for `symfony/lock`, Thanks to [@digilist]

### Fixed

- [#146] Make paths relative to current working directory - "cwd".
- [#158] Accept only string task number.

## [v1.10.1] - 2018-09-22

### Fixed

- [#139] Do not require `cURL` extension

## [v1.10.0] - 2018-09-22

### Fixed

- [#137] Treat whole output of failed command as "error output".

### Removed

- [#136] Remove guzzle

## [v1.9.0] - 2018-08-18

### Changed

- [#132] Improved container caching in shared servers

### Fixed

- [#131] Crunz can be used with `dragonmantank/cron-expression` package

### Deprecated

- Passing more than five parts (e.g `* * * * * *`) to `Crunz\Event::cron()`

## [v1.8.0] - 2018-08-15

### Added

- [#120] Added `--force` option to `schedule:run` command
- [#129] Add `--task` option for `schedule:run` command

### Fixed

- [#123] Spellfix: `comand` -> `command`, Thanks to [@FallDi]

## [v1.7.3] - 2018-06-15

- [#118] Undefined index: year in `vendor/lavary/crunz/src/Event.php` on line 370, Thanks to [@mindcreations]

## [v1.7.2] - 2018-06-13

### Fixed

- [#116] Do not replace Symfony's polyfills.

## [v1.7.1] - 2018-06-01

### Fixed

- [#110] Fixed config file path guessing.

## [v1.7.0] - 2018-05-27

### Added

- [#94] Added timezone option

### Deprecated
- `timezone` option in config file is now required, lack of it will result in Exception in version `2.0`

### Removed

- [#104] Remove splitCamel helper.

## [v1.6.1] - 2018-05-13

### Fixed

- [#90] Send output by email only if it is not empty.

## [v1.6.0] - 2018-04-22

### Added

- [#69] Option for allowing line breaks in logs, Thanks to [@TomasDuda]
- [#79] Introduce DI container

### Fixed

- [#43] Typos stopping email transport of 'mail', Thanks to [@m-hume]
- [#46] sendOutputTo and appendOutputTo fix, Thanks to [@m-hume]
- [#80] Fixed prevent overlapping on windows
- [#81] Fix Event::in on windows
- [#84] Make comparing date segments strict.
- [#86] Fix closure running on windows
- [#85] Fix changing user
- [#87] Remove error handler

## [v1.5.1] - 2018-04-12

### Added

- [#76] Introduce editorconfig
- [#75] Added changelog file.

### Fixed

- [#77] Fix high cpu usage

[#401]: https://github.com/lavary/crunz/pull/401
[#398]: https://github.com/lavary/crunz/pull/398
[#396]: https://github.com/lavary/crunz/pull/396
[#394]: https://github.com/lavary/crunz/pull/394
[#393]: https://github.com/lavary/crunz/pull/393
[#390]: https://github.com/lavary/crunz/pull/390
[#385]: https://github.com/lavary/crunz/pull/385
[#361]: https://github.com/lavary/crunz/pull/361
[#356]: https://github.com/lavary/crunz/pull/356
[#354]: https://github.com/lavary/crunz/pull/354
[#352]: https://github.com/lavary/crunz/pull/352
[#351]: https://github.com/lavary/crunz/pull/351
[#349]: https://github.com/lavary/crunz/pull/349
[#344]: https://github.com/lavary/crunz/pull/344
[#334]: https://github.com/lavary/crunz/pull/334
[#333]: https://github.com/lavary/crunz/pull/333
[#326]: https://github.com/lavary/crunz/pull/326
[#324]: https://github.com/lavary/crunz/pull/324
[#323]: https://github.com/lavary/crunz/pull/323
[#321]: https://github.com/lavary/crunz/pull/321
[#298]: https://github.com/lavary/crunz/pull/298
[#292]: https://github.com/lavary/crunz/pull/292
[#287]: https://github.com/lavary/crunz/pull/287
[#280]: https://github.com/lavary/crunz/pull/280
[#274]: https://github.com/lavary/crunz/pull/274
[#268]: https://github.com/lavary/crunz/pull/268
[#264]: https://github.com/lavary/crunz/pull/264
[#261]: https://github.com/lavary/crunz/pull/261
[#251]: https://github.com/lavary/crunz/pull/251
[#245]: https://github.com/lavary/crunz/pull/245
[#243]: https://github.com/lavary/crunz/pull/243
[#240]: https://github.com/lavary/crunz/pull/240
[#233]: https://github.com/lavary/crunz/pull/233
[#229]: https://github.com/lavary/crunz/pull/229
[#225]: https://github.com/lavary/crunz/pull/225
[#224]: https://github.com/lavary/crunz/pull/224
[#222]: https://github.com/lavary/crunz/pull/222
[#221]: https://github.com/lavary/crunz/pull/221
[#217]: https://github.com/lavary/crunz/pull/217
[#210]: https://github.com/lavary/crunz/pull/210
[#209]: https://github.com/lavary/crunz/pull/209
[#206]: https://github.com/lavary/crunz/pull/206
[#204]: https://github.com/lavary/crunz/pull/204
[#199]: https://github.com/lavary/crunz/pull/199
[#190]: https://github.com/lavary/crunz/pull/190
[#181]: https://github.com/lavary/crunz/pull/181
[#180]: https://github.com/lavary/crunz/pull/180
[#178]: https://github.com/lavary/crunz/pull/178
[#173]: https://github.com/lavary/crunz/pull/173  
[#171]: https://github.com/lavary/crunz/pull/171
[#166]: https://github.com/lavary/crunz/pull/166
[#164]: https://github.com/lavary/crunz/pull/164
[#163]: https://github.com/lavary/crunz/pull/163
[#162]: https://github.com/lavary/crunz/pull/162
[#161]: https://github.com/lavary/crunz/pull/161
[#159]: https://github.com/lavary/crunz/pull/159
[#158]: https://github.com/lavary/crunz/pull/158
[#157]: https://github.com/lavary/crunz/pull/157
[#155]: https://github.com/lavary/crunz/pull/155
[#154]: https://github.com/lavary/crunz/pull/154
[#153]: https://github.com/lavary/crunz/pull/153
[#151]: https://github.com/lavary/crunz/pull/151
[#150]: https://github.com/lavary/crunz/pull/150
[#149]: https://github.com/lavary/crunz/pull/149
[#148]: https://github.com/lavary/crunz/pull/148
[#147]: https://github.com/lavary/crunz/pull/147
[#146]: https://github.com/lavary/crunz/pull/146
[#142]: https://github.com/lavary/crunz/pull/142
[#141]: https://github.com/lavary/crunz/pull/141
[#140]: https://github.com/lavary/crunz/pull/140
[#139]: https://github.com/lavary/crunz/pull/139
[#138]: https://github.com/lavary/crunz/pull/138
[#137]: https://github.com/lavary/crunz/pull/137
[#136]: https://github.com/lavary/crunz/pull/136
[#133]: https://github.com/lavary/crunz/pull/133
[#132]: https://github.com/lavary/crunz/pull/132
[#131]: https://github.com/lavary/crunz/pull/131
[#130]: https://github.com/lavary/crunz/pull/130
[#129]: https://github.com/lavary/crunz/pull/129
[#123]: https://github.com/lavary/crunz/pull/123
[#120]: https://github.com/lavary/crunz/pull/120
[#119]: https://github.com/lavary/crunz/pull/119
[#118]: https://github.com/lavary/crunz/pull/118
[#117]: https://github.com/lavary/crunz/pull/117
[#116]: https://github.com/lavary/crunz/pull/116
[#113]: https://github.com/lavary/crunz/pull/113
[#112]: https://github.com/lavary/crunz/pull/112
[#111]: https://github.com/lavary/crunz/pull/111
[#110]: https://github.com/lavary/crunz/pull/110
[#109]: https://github.com/lavary/crunz/pull/109
[#107]: https://github.com/lavary/crunz/pull/107
[#105]: https://github.com/lavary/crunz/pull/105
[#104]: https://github.com/lavary/crunz/pull/104
[#103]: https://github.com/lavary/crunz/pull/103
[#102]: https://github.com/lavary/crunz/pull/102
[#101]: https://github.com/lavary/crunz/pull/101
[#100]: https://github.com/lavary/crunz/pull/100
[#98]: https://github.com/lavary/crunz/pull/98
[#97]: https://github.com/lavary/crunz/pull/97
[#96]: https://github.com/lavary/crunz/pull/96
[#95]: https://github.com/lavary/crunz/pull/95
[#94]: https://github.com/lavary/crunz/pull/94
[#92]: https://github.com/lavary/crunz/pull/92
[#90]: https://github.com/lavary/crunz/pull/90
[#89]: https://github.com/lavary/crunz/pull/89
[#88]: https://github.com/lavary/crunz/pull/88
[#87]: https://github.com/lavary/crunz/pull/87
[#86]: https://github.com/lavary/crunz/pull/86
[#85]: https://github.com/lavary/crunz/pull/85
[#84]: https://github.com/lavary/crunz/pull/84
[#82]: https://github.com/lavary/crunz/pull/82
[#81]: https://github.com/lavary/crunz/pull/81
[#80]: https://github.com/lavary/crunz/pull/80
[#79]: https://github.com/lavary/crunz/pull/79
[#77]: https://github.com/lavary/crunz/pull/77
[#76]: https://github.com/lavary/crunz/pull/76
[#75]: https://github.com/lavary/crunz/pull/75
[#74]: https://github.com/lavary/crunz/pull/74
[#73]: https://github.com/lavary/crunz/pull/73
[#72]: https://github.com/lavary/crunz/pull/72
[#69]: https://github.com/lavary/crunz/pull/69
[#50]: https://github.com/lavary/crunz/pull/50
[#46]: https://github.com/lavary/crunz/pull/46
[#43]: https://github.com/lavary/crunz/pull/43
[#36]: https://github.com/lavary/crunz/pull/36
[#25]: https://github.com/lavary/crunz/pull/25
[#24]: https://github.com/lavary/crunz/pull/24
[#23]: https://github.com/lavary/crunz/pull/23
[#17]: https://github.com/lavary/crunz/pull/17
[#16]: https://github.com/lavary/crunz/pull/16
[crunzphp#5]: https://github.com/crunzphp/crunz/pull/5
[crunzphp#24]: https://github.com/crunzphp/crunz/pull/24
[crunzphp#31]: https://github.com/crunzphp/crunz/pull/31
[v1.5.1]: https://github.com/crunzphp/crunz/compare/v1.5.0...v1.5.1
[v1.6.0]: https://github.com/crunzphp/crunz/compare/v1.5.1...v1.6.0
[v1.6.1]: https://github.com/crunzphp/crunz/compare/v1.6.0...v1.6.1
[v1.7.0]: https://github.com/crunzphp/crunz/compare/v1.6.1...v1.7.0
[v1.7.1]: https://github.com/crunzphp/crunz/compare/v1.7.0...v1.7.1
[v1.7.2]: https://github.com/crunzphp/crunz/compare/v1.7.1...v1.7.2
[v1.7.3]: https://github.com/crunzphp/crunz/compare/v1.7.2...v1.7.3
[v1.8.0]: https://github.com/crunzphp/crunz/compare/v1.7.3...v1.8.0
[v1.9.0]: https://github.com/crunzphp/crunz/compare/v1.8.0...v1.9.0
[v1.10.0]: https://github.com/crunzphp/crunz/compare/v1.9.0...v1.10.0
[v1.10.1]: https://github.com/crunzphp/crunz/compare/v1.10.0...v1.10.1
[v1.11.0-beta.1]: https://github.com/crunzphp/crunz/compare/v1.10.1...v1.11.0-beta.1
[v1.11.0-beta.2]: https://github.com/crunzphp/crunz/compare/v1.11.0-beta.1...v1.11.0-beta.2
[v1.11.0-rc.1]: https://github.com/crunzphp/crunz/compare/v1.11.0-beta.2...v1.11.0-rc.1
[v1.11.0]: https://github.com/crunzphp/crunz/compare/v1.11.0-rc.1...v1.11.0
[v1.11.1]: https://github.com/crunzphp/crunz/compare/v1.11.0...v1.11.1
[v1.11.2]: https://github.com/crunzphp/crunz/compare/v1.11.1...v1.11.2
[v1.12.0]: https://github.com/crunzphp/crunz/compare/v1.11.2...v1.12.0
[v1.12.1]: https://github.com/crunzphp/crunz/compare/v1.12.0...v1.12.1
[v1.12.2]: https://github.com/crunzphp/crunz/compare/v1.12.1...v1.12.2
[v1.12.3]: https://github.com/crunzphp/crunz/compare/v1.12.2...v1.12.3
[v1.12.4]: https://github.com/crunzphp/crunz/compare/v1.12.3...v1.12.4
[v2.0.0]: https://github.com/crunzphp/crunz/compare/v1.12.0...v2.0.0
[v2.0.1]: https://github.com/crunzphp/crunz/compare/v2.0.0...v2.0.1
[v2.0.2]: https://github.com/crunzphp/crunz/compare/v2.0.1...v2.0.2
[v2.0.3]: https://github.com/crunzphp/crunz/compare/v2.0.2...v2.0.3
[v2.0.4]: https://github.com/crunzphp/crunz/compare/v2.0.3...v2.0.4
[v2.1.0]: https://github.com/crunzphp/crunz/compare/v2.0.4...v2.1.0
[v2.2.0]: https://github.com/crunzphp/crunz/compare/v2.1.0...v2.2.0
[v2.2.1]: https://github.com/crunzphp/crunz/compare/v2.2.0...v2.2.1
[v2.2.2]: https://github.com/crunzphp/crunz/compare/v2.2.1...v2.2.2
[v2.2.3]: https://github.com/crunzphp/crunz/compare/v2.2.2...v2.2.3
[v2.2.4]: https://github.com/crunzphp/crunz/compare/v2.2.3...v2.2.4
[v2.3.0]: https://github.com/crunzphp/crunz/compare/v2.2.4...v2.3.0
[v2.3.1]: https://github.com/crunzphp/crunz/compare/v2.3.0...v2.3.1
[v3.0.0]: https://github.com/crunzphp/crunz/compare/v2.3.1...v3.0.0
[v3.0.1]: https://github.com/crunzphp/crunz/compare/v3.0.0...v3.0.1
[v3.1.0]: https://github.com/crunzphp/crunz/compare/v3.0.1...v3.1.0
[v3.2.0]: https://github.com/crunzphp/crunz/compare/v3.1.0...v3.2.0
[v3.2.1]: https://github.com/crunzphp/crunz/compare/v3.2.0...v3.2.1
[v3.2.2]: https://github.com/crunzphp/crunz/compare/v3.2.1...v3.2.2
[v3.3.0]: https://github.com/crunzphp/crunz/compare/v3.2.2...v3.3.0
[v3.4.0]: https://github.com/crunzphp/crunz/compare/v3.3.0...v3.4.0
[@andrewmy]: https://github.com/andrewmy
[@arthurbarros]: https://github.com/arthurbarros
[@bashgeek]: https://github.com/bashgeek
[@codermarcel]: https://github.com/codermarcel
[@digilist]: https://github.com/digilist
[@drjayvee]: https://github.com/drjayvee
[@erfan723]: https://github.com/erfan723
[@FallDi]: https://github.com/FallDi
[@iluuu1994]: https://github.com/iluuu1994
[@jhoughtelin]: https://github.com/jhoughtelin
[@m-hume]: https://github.com/m-hume
[@mareksuscak]: https://github.com/mareksuscak
[@mindcreations]: https://github.com/mindcreations
[@PhilETaylor]: https://github.com/PhilETaylor
[@radarhere]: https://github.com/radarhere
[@rrushton]: https://github.com/rrushton
[@SadeghPM]: https://github.com/SadeghPM
[@timurbakarov]: https://github.com/timurbakarov
[@TomasDuda]: https://github.com/TomasDuda
[@vinkla]: https://github.com/vinkla
