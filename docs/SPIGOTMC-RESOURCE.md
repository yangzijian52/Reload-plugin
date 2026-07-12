[CENTER][SIZE=7][B]Reload[/B][/SIZE]
[SIZE=4]Lightweight Scheduled Console Commands and Live Configuration Reloading[/SIZE][/CENTER]

[COLOR=#ff4d4d][B]Language notice:[/B][/COLOR] The SpigotMC resource page, documentation and support channel are English-only. Chinese-language support is not provided on SpigotMC.

[SIZE=5][B]About Reload[/B][/SIZE]
Reload is a small administration utility for Paper servers. It runs a configurable list of commands from the server console at a fixed interval and lets an authorized administrator reload the configuration without restarting the server.

The plugin itself currently uses Chinese configuration comments, command feedback and console messages. The SpigotMC publishing materials remain English-only.

[SIZE=5][B]Compatibility[/B][/SIZE]
[LIST]
[*][B]Server software:[/B] Paper 26.2 only
[*][B]Java:[/B] 25 or newer
[*][B]Plugin version:[/B] 1.0.2
[*][B]Compile-time API:[/B] Paper API 26.2.build.56-alpha
[*][B]Runtime testing:[/B] The 1.0.2 release passed a clean Maven build; no additional Paper 26.2 live-server test was performed
[*]Spigot, Folia and other server implementations have not been tested and are not claimed as supported
[/LIST]

[SIZE=5][B]Free Resource[/B][/SIZE]
Reload is published as a [B]free resource[/B] with a price of [B]USD 0.00[/B] under the MIT License. It is a compact, single-purpose utility with no paid service, premium integration, account system or commercial backend. A paid listing would not be justified by its current scope.

[SIZE=5][B]Main Features[/B][/SIZE]
[LIST]
[*]Runs one or more configured commands from the server console
[*]Uses a configurable interval measured in seconds
[*]Reloads configuration through [B]/ro config[/B] without a server restart
[*]Creates the default configuration automatically on first startup
[*]Cancels and recreates the scheduled task after configuration reload
[*]Enforces a minimum runtime interval of one second
[*]Has no required third-party plugins
[*]Stores no player, economy or transaction data
[/LIST]

[SIZE=5][B]Command Execution and Security[/B][/SIZE]
Configured entries are dispatched as the [B]server console[/B] and therefore have the same authority as commands typed directly into the console. Only trusted administrators should be allowed to edit [B]plugins/Reload/config.yml[/B]. Never place untrusted player input, secrets or unsafe commands in the command list.

The [B]reload.command[/B] permission protects the configuration reload command. Access should remain limited to trusted staff. Reload does not expose a player-facing command for adding, removing or editing scheduled commands.

[SIZE=5][B]Data and Transaction Behavior[/B][/SIZE]
Reload has no database and does not create player data files, balances, purchase records or transaction logs. Its only persistent file is [B]plugins/Reload/config.yml[/B]. If configured commands modify another plugin's data or economy, that behavior belongs to the command target and is outside Reload's transaction control.

[SIZE=5][B]Scheduling Behavior[/B][/SIZE]
The command list runs immediately when the scheduled task starts and then repeats at the configured interval. Commands are dispatched sequentially on the normal server scheduler. Keep command lists and intervals reasonable to avoid avoidable server load.

[SIZE=5][B]Dependencies[/B][/SIZE]
[LIST]
[*]No third-party plugin dependencies
[*]Paper 26.2 server runtime
[*]Java 25 or newer
[*]Paper API is compile-time only and is not bundled inside the jar
[/LIST]

[SIZE=5][B]Links[/B][/SIZE]
[LIST]
[*][URL=https://github.com/yangzijian52/reload]Source Code[/URL]
[*][URL=https://github.com/yangzijian52/reload/releases]Downloads[/URL]
[*][URL=https://github.com/yangzijian52/reload/issues]English Support and Bug Reports[/URL]
[*][URL=https://github.com/yangzijian52/reload/blob/main/LICENSE]MIT License[/URL]
[/LIST]

[SIZE=5][B]Important Notes[/B][/SIZE]
[LIST]
[*]Back up the configuration before replacing or editing it.
[*]The interval is expressed in seconds; values below 1 are executed as 1 second at runtime.
[*]A configuration reload restarts the scheduler and causes the configured command list to run immediately.
[*]Malformed YAML may result in an empty fallback configuration; review the console after every reload.
[*]Use only commands that are safe to execute repeatedly with console authority.
[*]Paper 26.2 is the only claimed server target for this release.
[/LIST]
