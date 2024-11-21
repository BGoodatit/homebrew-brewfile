# file location: ${HOME}/Brewfile

  require 'date'
  require 'open-uri'

  # brew version
  hb = `brew -v`
  # bash version
  bv = `bash -c 'echo $BASH_VERSION'`
  sh = `echo $SHELL`
  # current date
  now = DateTime.now
  now.strftime("%B %d %Y")
  # auto-update status
  au = ENV.fetch("HOMEBREW_AUTO_UPDATE_COMMAND")
  status = au ? "True" : "False"

  # fail if Homebrew is not installed, (or if it's not in $PATH)
  if !hb.include? "Homebrew"
    abort("ERROR: Homebrew does not appear to be installed!")
  end

  # display some basic system env information
  puts("--------------------------------")
  puts("HOMEBREW_PRODUCT    : " + ENV.fetch("HOMEBREW_PRODUCT"))
  puts("HOMEBREW_SYSTEM     : " + ENV.fetch("HOMEBREW_SYSTEM"))
  puts("HOMEBREW_OS_VERSION : " + ENV.fetch("HOMEBREW_OS_VERSION"))
  puts("HOMEBREW_VERSION    : " + ENV.fetch("HOMEBREW_VERSION"))
  puts("HOMEBREW_PROCESSOR  : " + ENV.fetch("HOMEBREW_PROCESSOR"))
  puts("AUTO_UPDATE_ENABLED : " + status + " (" + au + ")")
  puts("BASH_VERSION        : " + bv)
  puts("CURRENT_USER_SHELL  : " + sh)
  puts("--------------------------------")
  puts("\n")

  # give us time to CTRL-C
  sleep(5)

  ###############################################################################
  # Determine the Homebrew installation prefix dynamically
  brew_prefix = `brew --prefix`.chomp

  # Update Homebrew and set up taps
  tap "homebrew/services"
  tap "homebrew/bundle"
  tap "homebrew/cask-fonts"
  tap "homebrew/autoupdate"
  tap "powershell/tap"
  tap "felixkratz/formulae"
  tap "buo/cask-upgrade"
  tap "homebrew/cask-versions"
  # unnecessary taps in v4: https://brew.sh/2023/02/16/homebrew-4.0.0/
  if ENV.fetch("HOMEBREW_VERSION") < '4.0.0'
    tap "homebrew/cask"         # [https://github.com/Homebrew/homebrew-cask]
    tap "homebrew/core"         # [https://github.com/Homebrew/homebrew-core]
  end

  brew "asdf"                   # [https://asdf-vm.com/]
  brew "bash"                 # [https://www.gnu.org/software/bash/]
  brew "bash-completion@2"      # [https://github.com/scop/bash-completion]
  brew "bats-core"              # [https://github.com/bats-core/bats-core]
  brew "boost"                  # [https://www.boost.org/]
  brew "ccache"                 # [https://ccache.dev/]
  brew "clang-format"           # [https://clang.llvm.org/docs/ClangFormat.html]
  brew "cmake"                  # [https://cmake.org/]
  brew "cookiecutter"           # [https://cookiecutter.readthedocs.io/]
  brew "dart-sdk"               # [https://dart.dev/]
  brew "go"                     # [https://go.dev/]
  brew "llvm@17"                # [https://llvm.org/]
  brew "lua"                    # [https://www.lua.org/]
  brew "node"                   # [https://nodejs.org/]
  brew "pipx"                   # [https://github.com/pypa/pipx]
  brew "poetry"                 # [https://python-poetry.org/]
  brew "pyenv"                  # [https://github.com/pyenv/pyenv]
  brew "ruby"                   # [https://www.ruby-lang.org/]
  brew "ruby-build"             # [https://github.com/rbenv/ruby-build]
  brew "rbenv"                  # [https://github.com/rbenv/rbenv]
  brew "rust"                   # [https://www.rust-lang.org/]
  brew "subversion"             # [https://subversion.apache.org/]
  brew "virtualenv"             # [https://virtualenv.pypa.io/]
  brew "virtualenvwrapper"      # [https://virtualenvwrapper.readthedocs.io/]
  brew "wget"                   # [https://www.gnu.org/software/wget/]
  brew "autojump"               # [https://github.com/wting/autojump]
  brew "coreutils"              # [https://www.gnu.org/software/coreutils/]
  brew "create-dmg"             # [https://github.com/andreyvit/create-dmg]
  brew "curl"                   # [https://curl.se/]
  brew "gettext"                # [https://www.gnu.org/software/gettext/]
  brew "gnu-sed"                # [https://www.gnu.org/software/sed/]
  brew "gnu-time"               # [https://www.gnu.org/software/time/]
  brew "grc"                    # [http://korpus.juls.savba.sk/~garabik/software/grc.html]
  brew "jq"                     # JSON processor [https://stedolan.github.io/jq/]
  brew "lsd"                    # [https://github.com/lsd-rs/lsd]
  brew "mackup"                 # [https://github.com/lra/mackup]
  brew "neofetch"               # [https://github.com/dylanaraps/neofetch]
  brew "rename"                 # [https://plasmasturm.org/code/rename/]
  brew "sha3sum"                # [https://github.com/mjosaarinen/sha3sum]
  brew "terminal-notifier"      # [https://github.com/julienXX/terminal-notifier]
  brew "thefuck"                # [https://github.com/nvbn/thefuck]
  brew "tree"                   # [https://linux.die.net/man/1/tree]
  brew "w3m"                    # [http://w3m.sourceforge.net/]
  brew "zplug"                  # [https://github.com/zplug/zplug]
  brew "htop"                   # [https://htop.dev/]
  brew "httrack"                # [https://www.httrack.com/]
  brew "tor"                    # [https://www.torproject.org/]
  brew "unbound"                # [https://nlnetlabs.nl/projects/unbound/]
  brew "fontconfig"             # [https://www.freedesktop.org/wiki/Software/fontconfig/]
  brew "flavours"               # [https://github.com/Misterio77/flavours]
  brew "felixkratz/formulae/sketchybar" # [https://github.com/felixkratz/SketchyBar]
  brew "git"                    # [https://git-scm.com/]
  brew "git-gui"                # [https://git-scm.com/docs/git-gui]
  brew "git-interactive-rebase-tool" # [https://github.com/MitMaro/git-interactive-rebase-tool]
  brew "gh"                     # GitHub CLI [https://github.com/cli/cli]
  brew "mercurial"              # [https://www.mercurial-scm.org/]
  brew "black"                  # [https://github.com/psf/black]
  brew "jupyterlab"             # [https://jupyterlab.readthedocs.io/]
  brew "mypy"                   # [https://github.com/python/mypy]
  brew "numpy"                  # [https://numpy.org/]
  brew "tox"                    # [https://tox.readthedocs.io/]
  # Additional Python Development Tools
  brew "micropython"          # Python for microcontrollers [https://www.micropython.org/]
  brew "pyenv", link: false   # Simple Python version management [https://github.com/pyenv/pyenv]
  brew "pipenv", link: false  # Virtualenvs for projects [https://pipenv.pypa.io/]
  brew "pyenv-virtualenv", link: false
  brew "python", link: false  # Python system package
  brew "imagemagick"            # [https://imagemagick.org/]
  brew "jp2a"                   # [https://csl.name/jp2a/]
  brew "lolcat"                 # [https://github.com/busyloop/lolcat]
  brew "libsodium"              # [https://libsodium.org/]
  brew "shellcheck"             # [https://www.shellcheck.net/]
  brew "shfmt"                  # [https://github.com/mvdan/sh]
  brew "asdf"                   # [https://asdf-vm.com/]
  brew "zsh-autosuggestions"    # [https://github.com/zsh-users/zsh-autosuggestions]
  brew "zsh-completions"        # [https://github.com/zsh-users/zsh-completions]
  brew "zsh-syntax-highlighting" # [https://github.com/zsh-users/zsh-syntax-highlighting]
  brew "powershell/tap/powershell" # [https://github.com/PowerShell/PowerShell]
  
  # Cask
  cask "firefox@developer-edition" # Developer edition of Firefox [https://www.mozilla.org/firefox/developer/]
  cask "google-chrome" # Google Chrome [https://www.google.com/chrome/]
  cask "tor-browser"   # Tor Browser [https://www.torproject.org/]
  cask "font-anonymous-pro"      # https://www.marksimonson.com/fonts/view/anonymous-pro
  cask "font-bebas-neue"         # https://fonts.adobe.com/fonts/bebas-neue
  cask "font-courier-prime"      # https://quoteunquoteapps.com/courierprime/
  cask "font-fira-code"          # https://github.com/tonsky/FiraCode
  cask "font-ia-writer-duo"      # https://github.com/iaolo/iA-Fonts/
  #cask "font-ia-writer-duospace" # https://ia.net/topics/in-search-of-the-perfect-writing-font
  cask "font-ia-writer-mono"     # https://github.com/iaolo/iA-Fonts/
  cask "font-ia-writer-quattro"  # https://ia.net/topics/a-typographic-christmas
  cask "font-inconsolata"        # https://levien.com/type/myfonts/inconsolata.html
  cask "font-input"              # https://input.djr.com/
  cask "font-intel-one-mono"     # https://github.com/intel/intel-one-mono/
  cask "font-jetbrains-mono"     # https://www.jetbrains.com/lp/mono/
  cask "font-iosevka"            # https://typeof.net/Iosevka/customizer
  cask "font-liberation"         # https://github.com/liberationfonts/liberation-fonts
  cask "font-red-hat-mono"       # https://github.com/RedHatOfficial/RedHatFont
  cask "font-ubuntu-mono"        # https://design.ubuntu.com/font
  cask "font-victor-mono"        # https://github.com/rubjo/victor-mono
  cask "font-dejavu-sans-mono-nerd-font"
  cask "font-inconsolata-go-nerd-font"
  cask "font-jetbrains-mono-nerd-font"
  cask "font-fira-mono"                       # Fira Mono [https://mozilla.github.io/Fira/]
  cask "font-fira-mono-for-powerline"         # Fira Mono with Powerline support
  cask "font-fira-sans"                       # Fira Sans
  cask "font-fira-sans-condensed"             # Fira Sans Condensed
  cask "font-fira-sans-extra-condensed"       # Fira Sans Extra Condensed
  cask "font-firago"                          # Firago [https://github.com/bBoxType/FiraGO]
  cask "font-jetbrains-mono"                  # JetBrains Mono [https://www.jetbrains.com/lp/mono/]
  cask "font-lekton-nerd-font"                # Lekton Nerd Font [https://www.nerdfonts.com/]
  cask "font-mononoki"                        # Mononoki Font [https://madmalik.github.io/mononoki/]
  cask "font-recursive-mono-nerd-font"        # Recursive Mono Nerd Font [https://www.recursive.design/]
  cask "font-ubuntu-sans-nerd-font"           # Ubuntu Sans Nerd Font
  cask "font-zed-mono-nerd-font"              # Zed Mono Nerd Font
  # cask "fork"                          # Fork Git client [https://git-fork.com/]
  # cask "gstreamer-development"        # GStreamer Development [https://gstreamer.freedesktop.org/]
  # cask "gstreamer-runtime"            # GStreamer Runtime
  cask "iterm2@beta"                   # iTerm2 (Beta) [https://iterm2.com/]
  cask "mono-mdk-for-visual-studio"    # Mono MDK for Visual Studio [https://www.mono-project.com/]
  cask "visual-studio"                 # Visual Studio [https://visualstudio.microsoft.com/]
  cask "visual-studio-code"            # Visual Studio Code [https://code.visualstudio.com/]
  # cask "macdown"                      # MacDown Markdown Editor [https://macdown.uranusjr.com/]
  # cask "mactex"                      # MacTeX [https://tug.org/mactex/]
  cask "warp"                          # Warp Terminal [https://www.warp.dev/]
  cask "sf-symbols"                    # SF Symbols [https://developer.apple.com/sf-symbols/]
  # cask "miniconda"                   # Miniconda Python distribution [https://docs.conda.io/en/latest/miniconda.html]
  # cask "mongodb-compass@beta"        # MongoDB Compass (Beta) [https://www.mongodb.com/products/compass]
  # cask "motrix"                      # Motrix Download Manager [https://motrix.app/]
  # cask "porting-kit"                 # Porting Kit [https://portingkit.com/]
  # cask "balenaetcher"                # Balena Etcher [https://www.balena.io/etcher/]
  # cask "disk-drill"                  # Disk Drill Data Recovery [https://www.cleverfiles.com/]
  # cask "etrecheckpro"                # EtreCheckPro [https://etrecheck.com/]
  cask "imazing"                       # iMazing Backup Manager [https://imazing.com/]
  cask "imazing-converter"            # iMazing HEIC Converter [https://imazing.com/converter]
  cask "imazing-profile-editor"       # iMazing Profile Editor [https://imazing.com/profile-editor]
  cask "ipvanish-vpn"                 # IPVanish VPN [https://www.ipvanish.com/]
  cask "megasync"                     # MEGAsync Cloud Storage [https://mega.io/]
  cask "parallels"                    # Parallels Desktop [https://www.parallels.com/]
  cask "wine-stable"                  # Wine Stable [https://www.winehq.org/]
  cask "spline"                       # Spline 3D Design [https://spline.design/]
  cask "warp"

  # VS Code Extensions (Alphabetized)
  vscode "ahkohd.glance"                                  # Quick file preview
  vscode "akvelonprimary.autocomment"                     # Auto-generate comments for code
  vscode "alefragnani.bookmarks"                          # Bookmarks for navigating code
  vscode "alefragnani.project-manager"                   # Manage multiple projects easily
  vscode "alexmunteanu.toggle-block-comments"             # Quickly toggle block comments
  vscode "antfu.browse-lite"                              # Lightweight web browser in VS Code
  vscode "antfu.vite"                                     # Integration for Vite projects
  vscode "atishay-jain.all-autocomplete"                  # Improved auto-completion across files
  vscode "bmalehorn.shell-syntax"                         # Better syntax highlighting for shell scripts
  vscode "bmalehorn.vscode-fish"                          # Fish shell integration
  vscode "bobmagicii.autofoldyeah"                        # Auto-folding sections of code
  vscode "casperstorm.directory-files"                    # Enhanced file directory management
  vscode "chekweitan.compare-view"                        # Compare two files or versions
  vscode "chiro2001.digital-ocean-manager"                # Manage Digital Ocean resources
  vscode "christian-kohler.npm-intellisense"              # Auto-complete npm modules
  vscode "codesandbox-io.codesandbox-projects"            # Manage CodeSandbox projects
  vscode "codestream.codestream"                          # Collaboration tool for code reviews
  vscode "codezombiech.gitignore"                         # Snippets for .gitignore files
  vscode "coenraads.disableligatures"                     # Disable font ligatures in editor
  vscode "ctf0.macros"                                    # Define reusable macros
  vscode "dae.vscode-mac-color-picker"                    # Color picker for macOS
  vscode "danidandev.comment-remover"                     # Easily remove comments in code
  vscode "dart-code.dart-code"                            # Dart language support
  vscode "dbaeumer.vscode-eslint"                         # ESLint integration
  vscode "devsense.composer-php-vscode"                   # Composer support for PHP
  vscode "devsense.intelli-php-vscode"                    # PHP IntelliSense
  vscode "devsense.phptools-vscode"                       # Advanced PHP tools
  vscode "devsense.profiler-php-vscode"                   # PHP profiling
  vscode "dotiful.dotfiles-syntax-highlighting"           # Syntax highlighting for dotfiles
  vscode "eamodio.gitlens"                                # GitLens for advanced Git visualization
  vscode "ecmel.vscode-html-css"                          # HTML and CSS support
  vscode "esbenp.prettier-vscode"                         # Prettier code formatter
  vscode "evolution-gaming.evolution-gaming--vscode-eslint" # Evolution Gaming's ESLint config
  vscode "firefox-devtools.vscode-firefox-debug"          # Debug with Firefox DevTools
  vscode "formulahendry.code-runner"                      # Run code snippets in editor
  vscode "foxundermoon.shell-format"                      # Format shell scripts
  vscode "github.codespaces"                              # Codespaces integration
  vscode "github.remotehub"                               # Work with GitHub repositories
  vscode "github.vscode-pull-request-github"              # GitHub pull request integration
  vscode "golang.go"                                      # Go language support
  vscode "gruntfuggly.todo-tree"                          # Manage TODOs in code
  vscode "hoovercj.vscode-settings-cycler"                # Cycle through different settings
  vscode "htmlhint.vscode-htmlhint"                       # HTML linting
  vscode "ibm.output-colorizer"                           # Colorize terminal output
  vscode "inu1255.easy-snippet"                           # Manage snippets easily
  vscode "iocave.customize-ui"                            # Customize VS Code UI
  vscode "iocave.monkey-patch"                            # Modify editor behavior
  vscode "irongeek.vscode-env"                            # Manage environment variables
  vscode "jabacchetta.vscode-essentials"                  # Collection of essential extensions
  vscode "jakearl.search-editor-apply-changes"            # Apply changes directly from search
  vscode "jasonlhy.hungry-delete"                         # Smart deletion
  vscode "jkjustjoshing.vscode-text-pastry"               # Advanced text manipulation
  vscode "jock.svg"                                       # SVG editing and preview
  vscode "johnpapa.vscode-peacock"                        # Color-code your workspace
  vscode "jonathanschlitt.open-in-system-terminal"        # Open folder in system terminal
  vscode "lacroixdavid1.vscode-format-context-menu"       # Format code from context menu
  vscode "lostintangent.vsls-whiteboard"                  # Whiteboard collaboration in VS Code
  vscode "maxcutlyp.dotenv-autocomplete"                  # Autocomplete `.env` files
  vscode "metaseed.metago"                                # Navigate code faster
  vscode "metaseed.metajump"                              # Jump between code references
  vscode "metaseed.metaword"                              # Work with words in code
  vscode "mhutchie.git-graph"                             # Visualize Git history
  vscode "micnil.vscode-checkpoints"                      # Checkpoint your work
  vscode "mikestead.dotenv"                               # `.env` file support
  vscode "moshfeu.diff-merge"                             # Manage and resolve diffs
  vscode "ms-azuretools.vscode-azureresourcegroups"       # Azure resource groups support
  vscode "ms-azuretools.vscode-azurevirtualmachines"      # Azure virtual machines integration
  vscode "ms-azuretools.vscode-docker"                   # Docker integration
  vscode "ms-python.debugpy"                              # Debugging support for Python
  vscode "ms-python.python"                               # Python language support
  vscode "ms-python.vscode-pylance"                      # Pylance for Python
  vscode "ms-vscode-remote.remote-containers"            # Development inside containers
  vscode "ms-vscode-remote.remote-ssh"                   # Remote SSH development
  vscode "ms-vscode-remote.remote-ssh-edit"              # Edit files over SSH
  vscode "ms-vscode.azure-account"                       # Azure account management
  vscode "ms-vscode.azure-repos"                         # Azure Repos integration
  vscode "ms-vscode.cmake-tools"                         # CMake project support
  vscode "ms-vscode.live-server"                         # Live server for web development
  vscode "ms-vscode.makefile-tools"                      # Makefile support
  vscode "ms-vscode.powershell"                          # PowerShell language support
  vscode "ms-vscode.remote-explorer"                     # Explore remote environments
  vscode "ms-vscode.remote-repositories"                 # Access remote repositories
  vscode "ms-vscode.remote-server"                       # Remote server access
  vscode "ms-vsliveshare.vsliveshare"                    # Live Share collaboration
  vscode "mubaidr.vuejs-extension-pack"                  # Vue.js development pack
  vscode "nhoizey.gremlins"                              # Detect invisible characters
  vscode "parallelsdesktop.parallels-desktop"            # Parallels Desktop support
  vscode "peterschmalfeldt.explorer-exclude"             # Manage excluded files in explorer
  vscode "pnp.polacode"                                  # Generate code screenshots
  vscode "pranaygp.vscode-css-peek"                      # Peek CSS definitions
  vscode "rassek96.vscode-comment-selection"             # Comment/uncomment code
  vscode "redhat.java"                                   # Java support by Red Hat
  vscode "remimarche.cspell-tech"                        # Spell-checking for technical terms
  vscode "rioj7.vscode-json-validate"                    # JSON schema validation
  vscode "ritwickdey.liveserver"                        # Live server for HTML
  vscode "rvest.vs-code-prettier-eslint"                 # Prettier and ESLint integration
  vscode "sankeyteam.dcd"                                # Dependency control
  vscode "sdras.vue-vscode-snippets"                     # Vue.js snippets
  vscode "silofy.hackthebox"                             # HackTheBox integration
  vscode "simonsiefke.svg-preview"                       # SVG preview support
  vscode "skyapps.fish-vscode"                           # Fish shell syntax highlighting
  vscode "slevesque.vscode-multiclip"                    # Multi clipboard manager
  vscode "smatdnepr.svg-sprite-viewer-generator"         # Generate SVG sprites
  vscode "stkb.rewrap"                                   # Rewrap long lines
  vscode "streetsidesoftware.code-spell-checker"         # Spell checker
  vscode "svipas.code-autocomplete"                      # Autocomplete assistance
  vscode "svipas.control-snippets"                      # Control over snippets
  vscode "tamasfe.even-better-toml"                      # TOML support
  vscode "timonwong.shellcheck"                          # ShellCheck for shell scripts
  vscode "tlevesque2.duplicate-finder"                   # Find duplicate files
  vscode "tombonnike.vscode-status-bar-format-toggle"    # Toggle status bar formatting
  vscode "tomoki1207.pdf"                                # PDF viewer
  vscode "trabpukcip.vscode-npm-scripts"                 # NPM scripts integration
  vscode "tusaeff.vscode-iterm2-theme-sync"              # Sync iTerm2 themes with VS Code
  vscode "twxs.cmake"                                    # CMake support
  vscode "usernamehw.errorlens"                         # Highlight errors inline
  vscode "visualstudioexptteam.intellicode-api-usage-examples" # IntelliCode examples
  vscode "visualstudioexptteam.vscodeintellicode"        # IntelliCode suggestions
  vscode "vitest.explorer"                               # Vitest test explorer
  vscode "vscjava.vscode-java-debug"                     # Java debugging tools
  vscode "vscjava.vscode-java-dependency"                # Java dependency management
  vscode "vscjava.vscode-java-pack"                      # Java development pack
  vscode "vscjava.vscode-java-test"                      # Java testing tools
  vscode "vscjava.vscode-maven"                          # Maven integration
  vscode "vsls-contrib.gistfs"                           # Access GitHub Gists
  vscode "vue.volar"                                     # Vue.js tooling
  vscode "wayou.vscode-todo-highlight"                   # Highlight TODOs in code
  vscode "xabikos.javascriptsnippets"                   # JavaScript snippets
  vscode "xyz.local-history"                             # Local history for files
  vscode "yakenoharashinnosuke.insistent-comments"       # Inline commenting tools
  vscode "yutengjing.vscode-archive"                     # Archive browsing
  vscode "zgm.vscode-fish"                               # Fish shell integration
  vscode "zignd.html-css-class-completion"               # HTML/CSS class name completion
  # *

  # MAS Commands (Alphabetized)

  # mas "Address Book Clearout", id: 442397431                  # Clean up duplicate contacts [https://apps.apple.com/us/app/address-book-clearout/id442397431]
  # mas "Apple Configurator", id: 1037126344                   # Configure iOS and iPadOS devices [https://apps.apple.com/us/app/apple-configurator/id1037126344]
  # mas "Betternet VPN", id: 1028905953                        # VPN service [https://apps.apple.com/us/app/betternet-vpn/id1028905953]
  # mas "CloudMounter", id: 1130254674                         # Mount cloud storage as local drives [https://apps.apple.com/us/app/cloudmounter/id1130254674]
  # mas "CopyClip", id: 595191960                              # Clipboard manager [https://apps.apple.com/us/app/copyclip/id595191960]
  # mas "Developer", id: 640199958                             # Developer toolset by Apple [https://apps.apple.com/us/app/developer/id640199958]
  # mas "EnhanceFox", id: 1544212575                           # AI photo enhancement [https://apps.apple.com/us/app/enhancefox-photo-enhance/id1544212575]
  # mas "Essentials", id: 1588151344                           # Essential tools collection [https://apps.apple.com/us/app/essentials/id1588151344]
  # mas "Grammarly for Safari", id: 1462114288                 # Grammar checker for Safari [https://apps.apple.com/us/app/grammarly-for-safari/id1462114288]
  # mas "Hand Mirror", id: 1502839586                          # Quick webcam access [https://apps.apple.com/us/app/hand-mirror/id1502839586]
  # mas "iMazing Profile Editor", id: 1487860882              # Profile editor for mobile devices [https://apps.apple.com/us/app/imazing-profile-editor/id1487860882]
  # mas "MacFamilyTree 9", id: 1458866808                      # Genealogy software [https://apps.apple.com/us/app/macfamilytree-9/id1458866808]
  # mas "Magnet", id: 441258766                                # Window manager [https://apps.apple.com/us/app/magnet/id441258766]
  # mas "Messenger", id: 1480068668                            # Facebook Messenger [https://apps.apple.com/us/app/messenger/id1480068668]
  # mas "Microsoft Remote Desktop", id: 1295203466             # Remote desktop client [https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466]
  # mas "Model Pro", id: 1464222390                            # Modeling tool [https://apps.apple.com/us/app/model-pro/id1464222390]
  # mas "Numbers", id: 409203825                               # Spreadsheet app [https://apps.apple.com/us/app/numbers/id409203825]
  # mas "OTP Auth", id: 1471867429                             # Two-factor authentication app [https://apps.apple.com/us/app/otp-auth/id1471867429]
  # mas "Pages", id: 409201541                                 # Word processing app [https://apps.apple.com/us/app/pages/id409201541]
  # mas "Parallels Desktop", id: 1085114709                    # Virtualization software [https://apps.apple.com/us/app/parallels-desktop/id1085114709]
  # mas "PayPal Honey", id: 1472777122                         # Honey coupon and deals app [https://apps.apple.com/us/app/paypal-honey/id1472777122]
  # mas "Pixelmator Pro", id: 1289583905                       # Advanced photo editing [https://apps.apple.com/us/app/pixelmator-pro/id1289583905]
  # mas "Shopping for Amazon", id: 1095562398                 # Amazon shopping app [https://apps.apple.com/us/app/shopping-for-amazon/id1095562398]
  # mas "Sticklets", id: 1633701470                            # Sticky notes app [https://apps.apple.com/us/app/sticklets/id1633701470]
  # mas "Sticky Notes", id: 1150887374                         # Sticky notes for your desktop [https://apps.apple.com/us/app/sticky-notes/id1150887374]
  # mas "The Unarchiver", id: 425424353                        # Archive extraction utility [https://apps.apple.com/us/app/the-unarchiver/id425424353]
  # mas "Transcribe", id: 1241342461                           # Transcription app [https://apps.apple.com/us/app/transcribe/id1241342461]
  # mas "Transporter", id: 1450874784                          # Upload media to the App Store [https://apps.apple.com/us/app/transporter/id1450874784]
  # mas "Twitter", id: 1482454543                              # Twitter app [https://apps.apple.com/us/app/twitter/id1482454543]
  # mas "Universe", id: 1211437633                             # Website builder app [https://apps.apple.com/us/app/universe/id1211437633]
  # mas "Xcode", id: 497799835                                 # IDE for macOS and iOS development [https://apps.apple.com/us/app/xcode/id497799835]
