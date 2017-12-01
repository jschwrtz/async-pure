# CHANGELOG

v1.6.1 / 2017-12-01
===================

  * 1.6.1
  * 1.0.0
  * 0.4.0
  * 0.3.0
  * 0.2.0
  * :memo: updating docs
  * :memo: updating docs
  * :bento: updating screenshot
  * :rocket: deploy package
  * Prevent multiple prompt resets in one execution cycle (#368)
  * More thorough handling (hiding) of match results
  * Avoid implicit creation of global var prompt_pure_git_arrows

v1.6.0 / 2017-10-27
===================

  * 1.6.0
  * Link to pure.zsh and async.zsh for better clarity (#358)
  * Readme tweaks
  * Link to a Pure-inspired prompt done in Rust
  * Avoid implicit global var creation and cleanup (#347)
  * Fix grammar in readme (#344)
  * Update oh-my-zsh instructions in readme
  * Remove extra $fpath from npm postinstall fail instructions
  * Simplify readme avatar URLs
  * Use glob instead of regex for dir matching (#328)
  * Simplify oh-my-zsh instructions, avoid confusion
  * Add support for python virtualenv (#325)
  * Change dirty check delay threshold from 2 to 5 secs (#326)
  * Remove deprecated clear-screen ZLE widget (#322)
  * Use pattern to matching newline, fix regex compile
  * Restore old virtualenv behavior by only modifying preprompt (#321)
  * Perform all git checks (vcs_info) asynchronously (#273)
  * Update prezto link and instructions in readme
  * Add `purer` fork to readme (#307)

v1.5.2 / 2017-03-18
===================

  * 1.5.2
  * Ensure prompt_subst is unset when the expanded preprompt is stored (#305)
  * Parse git aliases for better pull/fetch detection (#289)
  * Link inside pure directory as npm install fallback (#285)

v1.5.1 / 2017-02-12
===================

  * 1.5.1
  * Fix wrong assumption about promptinit in setup (#291)

v1.5.0 / 2017-01-20
===================

  * 1.5.0
  * Check and set `prompt_opts` when not using `promptinit` (#277)
  * Check for git arrows asynchronously (#272)
  * Evaluate $PROMPT at render time (#274)
  * Update zsh-async to 1.5.0 (#271)
  * Disable interactive passwords in SSH for git fetch (#269)
  * Change prezto url to the active prezto repo (#268)
  * Simplify zplug instructions in readme (#267)
  * Change integration examples from commands to configuration lines (#265)
  * Add zplug install instructions (#261)
  * Readme improvements (#259)
  * Add install instructions for Zim (#262)
  * Add issue template (#260)

v1.4.1 / 2016-12-12
===================

  * 1.4.1
  * Update zsh-async to fix issue with zsh 5.3
  * Mention intelfx/pure fork in readme (#247)
  * `HyperTerm` => `Hyper`
  * Restore prompt_subst setopt when rendering prompt (#231)
  * Update zsh-async to fix multi-space path bug
  * Use ; instead of && for promptinit (#227)
  * Prevent parameter expansion in preprompt
  * Revert "Fix double variable interpolation in branch name"
  * Fix double variable interpolation in branch name
  * Fix link to bash port (#219)

v1.4.0 / 2016-07-27
===================

  * 1.4.0
  * Compare expanded preprompt when rendering (#214)
  * Update async.zsh (#218)
  * update screenshot
  * Correct link to Droid Sans Mono Font (#216)
  * Add async.zsh to the download step in the readme
  * Merge pull request #205 from fvargas/master
  * Move footnote number
  * Merge pull request #204 from fvargas/master
  * Add note about screenshot color space
  * Merge pull request #201 from fvargas/master
  * Update and simplify oh-my-zsh integration instructions
  * readme - mention that the git check is done asynchronously #187
  * Merge pull request #196 from sindresorhus/emacs-fixes
  * Use zle reset-prompt to restore cursor instead of relying on ansi codes
  * Disable setting title in emacs terminal (not supported)
  * Clarify Prezto usage
  * Close #192 PR: Added `console` language where needed.
  * Merge pull request #186 from edouard-lopez/patch-1
  * move Ports below FAQ
  * fix typo thank to  @mafredri
  * add Shell Ports section
  * Merge pull request #181 from caarlos0/patch-1
  * Added antibody instructions
  * Merge pull request #178 from jedahan/master
  * Use builtin cd, in case cd::cd has been redefined
  * Merge pull request #177 from veggiemonk/patch-1
  * avoid double slashes in dest path
  * Close #175 PR: Refresh pure screenshot.

v1.3.0 / 2015-11-17
===================

  * 1.3.0
  * Update bundled zsh-async to 1.1.0
  * Close #171 PR: Attempt to detect user initiated git fetch. Fixes #162
  * Merge pull request #164 from sindresorhus/set-title-function
  * Deduplicate code by creating a set_title function
  * Update oh-my-zsh instructions

1.2.0 / 2015-08-25
==================

  * 1.2.0
  * Bump zsh-async to 1.0.0, prevents mixed stdout/stderr
  * Merge pull request #153 from sindresorhus/preprompt-update-fix
  * Render new preprompt with previous one in mind
  * Merge pull request #149 from mafredri/pure-nitro
  * Refactor to avoid subshell usage, prefer variables
  * Close #147 PR: Preserve preprompt on Ctrl+L. Fixes #145
  * Remove cr from prompt_opts, fixes #127
  * Merge pull request #142 from zmwangx/string-length-fix
  * fix last-char-of-preprompt-on-last-column condition
  * move subtraction by one out of prompt_pure_string_length
  * Merge pull request #144 from zmwangx/rename-prompt-to-preprompt
  * Default to 0 for git rev-list left and right. Fixes #137.
  * Close #140 PR: Add git arrows customization. Fixes #139.
  * prompt_pure_preprompt_render: rename prompt to preprompt

1.1.1 / 2015-07-04
==================

  * 1.1.1
  * Disable prompt expansion for running command
  * Merge pull request #130 from zmwangx/rename-variables-for-readability
  * rename two internal variables for readability
  * Use standard `[[ ]]` for conditional and add clarifications
  * fix: do the PURE_GIT_PULL check in the correct place

1.1.0 / 2015-06-01
==================

  * 1.1.0
  * Close #124 PR: Show hostname in terminal title if session is over ssh.
  * Merge pull request #125 from sindresorhus/dirty-check
  * Use slightly faster git dirty check for untracked files
  * import bug-fix release from zsh-async, fixes async job flushing
  * readme: faq clarificaitons
  * readme: add zpty error to faq with explanation and potential solutions
  * readme: update instructions for antigen and oh-my-zsh. remove incompatible async.plugin.zsh
  * use cd -q to prevent hooks from firing
  * prevent git status leakage when testing if dirty
  * fix paths that are split due to spaces in directory names
  * add @mafredri as a maintainer

1.0.0 / 2015-05-23
==================

  * 1.0.0
  * minor tweaks
  * Close #108 PR: Refactor async logic and allow for async git status..
  * Merge pull request #112 from mafredri/fix-git-terminal-prompt
  * Only disable git terminal prompt for git fetch
  * fast git execution
  * Merge pull request #110 from ehamberg/noautogc
  * Make sure git background fetch doesn't trigger gc
  * Merge pull request #107 from mafredri/spacing-fix-2
  * Fix ssh/root spacing issue.
  * Merge pull request #105 from mafredri/master
  * Fix prompt precmd spacing.
  * Merge pull request #104 from MoOx/patch-2
  * Add a note about the prompt loop that has been fixed in git 2.3

v0.5.1 / 2015-02-06
===================

  * 0.5.1
  * disable auth prompting on git 2.3+ - fixes #76
  * fix indent
  * Merge pull request #103 from MoOx/patch-1
  * Add shell loop/auth issue in the FAQ
  * add FAQ section

v0.5.0 / 2014-12-31
===================

  * 0.5.0
  * fix indent
  * Merge pull request #96 from danielhan/master
  * Close #100 PR: PURE_PROMPT_SYMBOL added.
  * Merge pull request #97 from sorin-ionescu/patch-1
  * Update Prezto instructions
  * work tree check bug fix

v0.4.0 / 2014-12-15
===================

  * 0.4.0
  * Close #94 PR: Show when root.

v0.3.1 / 2014-09-30
===================

  * 0.3.1
  * Merge pull request #87 from azuwis/master
  * Skip checking git remote if working tree is $HOME
  * add note about minimum requirements - fixes #85
  * tweaks
  * Update readme.md

v0.3.0 / 2014-08-09
===================

  * 0.3.0
  * readme tweaks
  * Close GH-80: Include untracked files in dirtiness check. Fixes #1, Fixes #79
  * Update readme.md

v0.2.2 / 2014-06-22
===================

  * 0.2.2
  * Merge pull request #75 from Tarrasch/symlink-plugin-zsh
  * Symlink pure.plugin.zsh ---> pure.zsh

v0.2.1 / 2014-06-08
===================

  * 0.2.1
  * Merge pull request #72 from AndreaGiardini/master
  * Double quote fix
  * readme - mention zsh-syntax-highlighting

v0.2.0 / 2014-05-29
===================

  * 0.2.0
  * update screenshot with pull/push arrows
  * readme - add note about push/pull arrows
  * Close GH-67: provide arrows for push and pull.
  * Close GH-65: Use $EPOCHSECONDS.. Fixes #64
  * Merge pull request #62 from Zearin/patch-1
  * readme.md: Minor formatting tweaks
  * Update readme.md

v0.1.3 / 2014-04-03
===================

  * 0.1.3
  * package.json - fix logging of error message

v0.1.2 / 2014-03-30
===================

  * 0.1.2
  * package.json - create dest dirs if they don't exist
  * Update readme.md

v0.1.1 / 2014-03-30
===================

  * 0.1.1
  * publish pure on npm
  * Close GH-61: Fixed PKGBUILD further.
  * Merge pull request #60 from emfa/master
  * Update PKGBUILD
  * Update readme.md
  * Merge pull request #48 from skippednote/master
  * Fix Prezto path
  * Merge pull request #47 from tlvince/bug/time-minutes
  * Fix minutes typo in human_time()
  * Humanize the execution time. Fixes #46
  * Close GH-45: Fix antigen theme integration..
  * Merge pull request #44 from sindresorhus/pb-doc-updates
  * Add notes about user install and prezto to readme
  * describe pure.zsh-theme
  * Close GH-41: Add integration with antigen.. Fixes #16
  * Prevent `%` from showing on unfinished lines
  * Add instructions for oh-my-zsh usage. #40
  * Use arithmetic evaluation to test git pull flag
  * Conditionalise git pull check
  * Merge pull request #34 from alanpearce/patch-1
  * Don't show pull indicator when ahead of remote
  * Merge pull request #31 from kouk/ansi-escapes
  * use more standard ansi+csr escapes. Refs #30
  * Use a lighter gray. Fixes #13
  * fix mangled prompts. closes #30
  * Use `command` for git and silence `git fetch`
  * fix quoting and simplify upstream reference check
  * Add a git pull check
  * Merge pull request #23 from sindresorhus/fix-printp
  * Fix problem with `print -Pn` and awk
  * Close GH-20: Fix bug and more.
  * Merge pull request #15 from pbrisbin/pull-request
  * Rename Arch package
  * minor tweaks
  * Switch back to tab indentation
  * Tweak readme
  * Close GH-14: Make pure.zsh loadable by the prompt system..
  * add screenshot of directory+cmd in title
  * readme tweaks
  * New feature: now shows current path in the title
  * Use modern syntax
  * Improve SSH if syntax
  * minor cleanup
  * readme tweaks
  * Followup to #11
  * Close GH-11: Remote user. Fixes #9
  * Revert "Only set the option locally"
  * Only set the option locally
  * Closure over the local variables by wrapping everything in a anonymous function
  * Use zsh hooks instead of overriding preexec and precmd
  * Add an example
  * Move the options out of the prompt
  * Rename prompt.zsh to pure.zsh
  * Use standard light gray color for the git branch
  * comments consistency
  * Enable prompt substitution
  * Improve logic for checking if inside a git repo
  * Call `git` directly and bypass aliases
  * Return early if folder isn't a git repo
  * Minor tweaks
  * Display the execution time of the last command
  * Add superfast way to detect if the branch is dirty
  * init
# CHANGELOG

v1.0.0 / 2017-12-01
===================

  * 1.0.0
  * 0.4.0
  * 0.3.0
  * 0.2.0
  * :memo: updating docs
  * :memo: updating docs
  * :bento: updating screenshot
  * :rocket: deploy package
  * Prevent multiple prompt resets in one execution cycle (#368)
  * More thorough handling (hiding) of match results
  * Avoid implicit creation of global var prompt_pure_git_arrows

v1.6.0 / 2017-10-27
===================

  * 1.6.0
  * Link to pure.zsh and async.zsh for better clarity (#358)
  * Readme tweaks
  * Link to a Pure-inspired prompt done in Rust
  * Avoid implicit global var creation and cleanup (#347)
  * Fix grammar in readme (#344)
  * Update oh-my-zsh instructions in readme
  * Remove extra $fpath from npm postinstall fail instructions
  * Simplify readme avatar URLs
  * Use glob instead of regex for dir matching (#328)
  * Simplify oh-my-zsh instructions, avoid confusion
  * Add support for python virtualenv (#325)
  * Change dirty check delay threshold from 2 to 5 secs (#326)
  * Remove deprecated clear-screen ZLE widget (#322)
  * Use pattern to matching newline, fix regex compile
  * Restore old virtualenv behavior by only modifying preprompt (#321)
  * Perform all git checks (vcs_info) asynchronously (#273)
  * Update prezto link and instructions in readme
  * Add `purer` fork to readme (#307)

v1.5.2 / 2017-03-18
===================

  * 1.5.2
  * Ensure prompt_subst is unset when the expanded preprompt is stored (#305)
  * Parse git aliases for better pull/fetch detection (#289)
  * Link inside pure directory as npm install fallback (#285)

v1.5.1 / 2017-02-12
===================

  * 1.5.1
  * Fix wrong assumption about promptinit in setup (#291)

v1.5.0 / 2017-01-20
===================

  * 1.5.0
  * Check and set `prompt_opts` when not using `promptinit` (#277)
  * Check for git arrows asynchronously (#272)
  * Evaluate $PROMPT at render time (#274)
  * Update zsh-async to 1.5.0 (#271)
  * Disable interactive passwords in SSH for git fetch (#269)
  * Change prezto url to the active prezto repo (#268)
  * Simplify zplug instructions in readme (#267)
  * Change integration examples from commands to configuration lines (#265)
  * Add zplug install instructions (#261)
  * Readme improvements (#259)
  * Add install instructions for Zim (#262)
  * Add issue template (#260)

v1.4.1 / 2016-12-12
===================

  * 1.4.1
  * Update zsh-async to fix issue with zsh 5.3
  * Mention intelfx/pure fork in readme (#247)
  * `HyperTerm` => `Hyper`
  * Restore prompt_subst setopt when rendering prompt (#231)
  * Update zsh-async to fix multi-space path bug
  * Use ; instead of && for promptinit (#227)
  * Prevent parameter expansion in preprompt
  * Revert "Fix double variable interpolation in branch name"
  * Fix double variable interpolation in branch name
  * Fix link to bash port (#219)

v1.4.0 / 2016-07-27
===================

  * 1.4.0
  * Compare expanded preprompt when rendering (#214)
  * Update async.zsh (#218)
  * update screenshot
  * Correct link to Droid Sans Mono Font (#216)
  * Add async.zsh to the download step in the readme
  * Merge pull request #205 from fvargas/master
  * Move footnote number
  * Merge pull request #204 from fvargas/master
  * Add note about screenshot color space
  * Merge pull request #201 from fvargas/master
  * Update and simplify oh-my-zsh integration instructions
  * readme - mention that the git check is done asynchronously #187
  * Merge pull request #196 from sindresorhus/emacs-fixes
  * Use zle reset-prompt to restore cursor instead of relying on ansi codes
  * Disable setting title in emacs terminal (not supported)
  * Clarify Prezto usage
  * Close #192 PR: Added `console` language where needed.
  * Merge pull request #186 from edouard-lopez/patch-1
  * move Ports below FAQ
  * fix typo thank to  @mafredri
  * add Shell Ports section
  * Merge pull request #181 from caarlos0/patch-1
  * Added antibody instructions
  * Merge pull request #178 from jedahan/master
  * Use builtin cd, in case cd::cd has been redefined
  * Merge pull request #177 from veggiemonk/patch-1
  * avoid double slashes in dest path
  * Close #175 PR: Refresh pure screenshot.

v1.3.0 / 2015-11-17
===================

  * 1.3.0
  * Update bundled zsh-async to 1.1.0
  * Close #171 PR: Attempt to detect user initiated git fetch. Fixes #162
  * Merge pull request #164 from sindresorhus/set-title-function
  * Deduplicate code by creating a set_title function
  * Update oh-my-zsh instructions

1.2.0 / 2015-08-25
==================

  * 1.2.0
  * Bump zsh-async to 1.0.0, prevents mixed stdout/stderr
  * Merge pull request #153 from sindresorhus/preprompt-update-fix
  * Render new preprompt with previous one in mind
  * Merge pull request #149 from mafredri/pure-nitro
  * Refactor to avoid subshell usage, prefer variables
  * Close #147 PR: Preserve preprompt on Ctrl+L. Fixes #145
  * Remove cr from prompt_opts, fixes #127
  * Merge pull request #142 from zmwangx/string-length-fix
  * fix last-char-of-preprompt-on-last-column condition
  * move subtraction by one out of prompt_pure_string_length
  * Merge pull request #144 from zmwangx/rename-prompt-to-preprompt
  * Default to 0 for git rev-list left and right. Fixes #137.
  * Close #140 PR: Add git arrows customization. Fixes #139.
  * prompt_pure_preprompt_render: rename prompt to preprompt

1.1.1 / 2015-07-04
==================

  * 1.1.1
  * Disable prompt expansion for running command
  * Merge pull request #130 from zmwangx/rename-variables-for-readability
  * rename two internal variables for readability
  * Use standard `[[ ]]` for conditional and add clarifications
  * fix: do the PURE_GIT_PULL check in the correct place

1.1.0 / 2015-06-01
==================

  * 1.1.0
  * Close #124 PR: Show hostname in terminal title if session is over ssh.
  * Merge pull request #125 from sindresorhus/dirty-check
  * Use slightly faster git dirty check for untracked files
  * import bug-fix release from zsh-async, fixes async job flushing
  * readme: faq clarificaitons
  * readme: add zpty error to faq with explanation and potential solutions
  * readme: update instructions for antigen and oh-my-zsh. remove incompatible async.plugin.zsh
  * use cd -q to prevent hooks from firing
  * prevent git status leakage when testing if dirty
  * fix paths that are split due to spaces in directory names
  * add @mafredri as a maintainer

1.0.0 / 2015-05-23
==================

  * 1.0.0
  * minor tweaks
  * Close #108 PR: Refactor async logic and allow for async git status..
  * Merge pull request #112 from mafredri/fix-git-terminal-prompt
  * Only disable git terminal prompt for git fetch
  * fast git execution
  * Merge pull request #110 from ehamberg/noautogc
  * Make sure git background fetch doesn't trigger gc
  * Merge pull request #107 from mafredri/spacing-fix-2
  * Fix ssh/root spacing issue.
  * Merge pull request #105 from mafredri/master
  * Fix prompt precmd spacing.
  * Merge pull request #104 from MoOx/patch-2
  * Add a note about the prompt loop that has been fixed in git 2.3

v0.5.1 / 2015-02-06
===================

  * 0.5.1
  * disable auth prompting on git 2.3+ - fixes #76
  * fix indent
  * Merge pull request #103 from MoOx/patch-1
  * Add shell loop/auth issue in the FAQ
  * add FAQ section

v0.5.0 / 2014-12-31
===================

  * 0.5.0
  * fix indent
  * Merge pull request #96 from danielhan/master
  * Close #100 PR: PURE_PROMPT_SYMBOL added.
  * Merge pull request #97 from sorin-ionescu/patch-1
  * Update Prezto instructions
  * work tree check bug fix

v0.4.0 / 2014-12-15
===================

  * 0.4.0
  * Close #94 PR: Show when root.

v0.3.1 / 2014-09-30
===================

  * 0.3.1
  * Merge pull request #87 from azuwis/master
  * Skip checking git remote if working tree is $HOME
  * add note about minimum requirements - fixes #85
  * tweaks
  * Update readme.md

v0.3.0 / 2014-08-09
===================

  * 0.3.0
  * readme tweaks
  * Close GH-80: Include untracked files in dirtiness check. Fixes #1, Fixes #79
  * Update readme.md

v0.2.2 / 2014-06-22
===================

  * 0.2.2
  * Merge pull request #75 from Tarrasch/symlink-plugin-zsh
  * Symlink pure.plugin.zsh ---> pure.zsh

v0.2.1 / 2014-06-08
===================

  * 0.2.1
  * Merge pull request #72 from AndreaGiardini/master
  * Double quote fix
  * readme - mention zsh-syntax-highlighting

v0.2.0 / 2014-05-29
===================

  * 0.2.0
  * update screenshot with pull/push arrows
  * readme - add note about push/pull arrows
  * Close GH-67: provide arrows for push and pull.
  * Close GH-65: Use $EPOCHSECONDS.. Fixes #64
  * Merge pull request #62 from Zearin/patch-1
  * readme.md: Minor formatting tweaks
  * Update readme.md

v0.1.3 / 2014-04-03
===================

  * 0.1.3
  * package.json - fix logging of error message

v0.1.2 / 2014-03-30
===================

  * 0.1.2
  * package.json - create dest dirs if they don't exist
  * Update readme.md

v0.1.1 / 2014-03-30
===================

  * 0.1.1
  * publish pure on npm
  * Close GH-61: Fixed PKGBUILD further.
  * Merge pull request #60 from emfa/master
  * Update PKGBUILD
  * Update readme.md
  * Merge pull request #48 from skippednote/master
  * Fix Prezto path
  * Merge pull request #47 from tlvince/bug/time-minutes
  * Fix minutes typo in human_time()
  * Humanize the execution time. Fixes #46
  * Close GH-45: Fix antigen theme integration..
  * Merge pull request #44 from sindresorhus/pb-doc-updates
  * Add notes about user install and prezto to readme
  * describe pure.zsh-theme
  * Close GH-41: Add integration with antigen.. Fixes #16
  * Prevent `%` from showing on unfinished lines
  * Add instructions for oh-my-zsh usage. #40
  * Use arithmetic evaluation to test git pull flag
  * Conditionalise git pull check
  * Merge pull request #34 from alanpearce/patch-1
  * Don't show pull indicator when ahead of remote
  * Merge pull request #31 from kouk/ansi-escapes
  * use more standard ansi+csr escapes. Refs #30
  * Use a lighter gray. Fixes #13
  * fix mangled prompts. closes #30
  * Use `command` for git and silence `git fetch`
  * fix quoting and simplify upstream reference check
  * Add a git pull check
  * Merge pull request #23 from sindresorhus/fix-printp
  * Fix problem with `print -Pn` and awk
  * Close GH-20: Fix bug and more.
  * Merge pull request #15 from pbrisbin/pull-request
  * Rename Arch package
  * minor tweaks
  * Switch back to tab indentation
  * Tweak readme
  * Close GH-14: Make pure.zsh loadable by the prompt system..
  * add screenshot of directory+cmd in title
  * readme tweaks
  * New feature: now shows current path in the title
  * Use modern syntax
  * Improve SSH if syntax
  * minor cleanup
  * readme tweaks
  * Followup to #11
  * Close GH-11: Remote user. Fixes #9
  * Revert "Only set the option locally"
  * Only set the option locally
  * Closure over the local variables by wrapping everything in a anonymous function
  * Use zsh hooks instead of overriding preexec and precmd
  * Add an example
  * Move the options out of the prompt
  * Rename prompt.zsh to pure.zsh
  * Use standard light gray color for the git branch
  * comments consistency
  * Enable prompt substitution
  * Improve logic for checking if inside a git repo
  * Call `git` directly and bypass aliases
  * Return early if folder isn't a git repo
  * Minor tweaks
  * Display the execution time of the last command
  * Add superfast way to detect if the branch is dirty
  * init
