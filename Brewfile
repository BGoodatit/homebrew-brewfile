
require 'date'

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

# Homebrew Update and Taps
tap "homebrew/core"
tap "homebrew/cask"
tap "homebrew/services" 
tap "homebrew/bundle" 
tap "powershell/tap" 
tap "homebrew/cask-fonts" 
tap "powershell/tap", 
tap "felixkratz/formulae"
tap "homebrew/autoupdate"   
tap "homebrew/bundle"         # [https://github.com/Homebrew/homebrew-bundle]
tap "homebrew/cask-fonts"     # [https://github.com/Homebrew/homebrew-cask-fonts]
tap "homebrew/services"       # [https://github.com/Homebrew/homebrew-services]

# Set global arguments for all 'brew install --cask' commands
cask_args appdir: "~/Applications", require_sha: true

# Unix Tools Installation
brew "git"
brew "wget"
brew "curl"
brew "tree"
brew "htop"
brew "mas"
brew "xz"
brew "openssl@3"
brew "ascii"
brew "coreutils"
brew "asdf"
brew "sqlite"
brew "python@3.12"
brew "autojump"
brew "bash"
brew "bash-completion"
brew "bash-completion@2"
brew "bats-core"
brew "bdw-gc"
brew "black"
brew "icu4c"
brew "boost"
brew "c-ares"
brew "fontconfig"
brew "gettext"
brew "libxext"
brew "catimg"
brew "cava"
brew "ccache"
brew "chruby"
brew "clang-format"
brew "cmake"
brew "colordiff"
brew "cookiecutter"
brew "dart-sdk"
brew "dotenv-linter"
brew "doxygen"
brew "unbound"
brew "harfbuzz"
brew "libsodium"
brew "numpy"
brew "tbb"
brew "theora"
brew "fish"
brew "fisher"
brew "flavours"
brew "fontforge"
brew "gh"
brew "git-gui"
brew "git-interactive-rebase-tool"
brew "gnu-sed"
brew "gnu-time"
brew "grc"
brew "node"
brew "gulp-cli"
brew "httrack"
brew "hugo"
brew "imagemagick"
brew "ipython"
brew "jp2a"
brew "jq"
brew "pandoc"
brew "jupyterlab"
brew "libgpg-error"
brew "lua"
brew "lmod"
brew "lolcat"
brew "lsd"
brew "ruby"
brew "macvim"
brew "mercurial"
brew "mypy"
brew "zlib"
brew "neofetch"
brew "ninja"
brew "nox"
brew "nvm"
brew "openjdk"
brew "pdftk-java"
brew "pipx"
brew "poetry"
brew "pre-commit"
brew "pyenv"
brew "python-urllib3"
brew "python@3.11"
brew "qt"
brew "ruby-build"
brew "rbenv"
brew "rename"
brew "root"
brew "ruff"
brew "rust"
brew "shellcheck"
brew "shfmt"
brew "starship"
brew "subversion"
brew "swig"
brew "terminal-notifier"
brew "thefuck"
brew "tmux"
brew "tor"
brew "tox"
brew "vcs"
brew "virtualenv"
brew "virtualenvwrapper"
brew "w3m"
brew "yarn"
brew "zplug"
brew "zsh-autosuggestions"
brew "zsh-syntax-highlighting"
brew "felixkratz/formulae/sketchybar"
brew "powershell/tap/powershell"

# Cask Applications Installation
cask "google-chrome"
cask "firefox-developer-edition"
cask "visual-studio-code"
cask "slack"
cask "spotify"
cask "docker"
cask "iterm2"
cask "adobe-creative-cloud"
cask "alacritty"
cask "amethyst"
cask "balenaetcher"
cask "brave-browser"
cask "cakebrew"
cask "diffmerge"
cask "disk-drill"
cask "dropbox"
cask "etrecheckpro"
cask "font-fira-mono"
cask "font-fira-mono-for-powerline"
cask "font-fira-sans"
cask "font-fira-sans-condensed"
cask "font-fira-sans-extra-condensed"
cask "font-firago"
cask "font-mononoki"
cask "fontforge"
cask "gimp"
cask "gulp"
cask "imazing"
cask "imazing-converter"
cask "imazing-profile-editor"
cask "ipvanish-vpn"
cask "macdown"
cask "mactex"
cask "mattermost"
cask "megasync"
cask "miniconda"
cask "motrix"
cask "powershell"
cask "sf-symbols"
cask "spline"
cask "texstudio"
cask "tor-browser"
cask "warp"
cask "whatsapp"
cask "wireshark"

# Mac App Store Installations
mas install 442397431 # Address Book Clearout 2.1.10
mas install 1451544217 # Adobe Lightroom 7.2
mas install 6447312365 # AI Chat Bot 14.1.2
mas install 1037126344 # Apple Configurator 2.17
mas install 1028905953 # Betternet VPN 3.6.0
mas install 1518425043 # Boop 1.4.0
mas install 6449970704 # Brand Identity - Stylescape 1.0
mas install 897446215 # Canva 1.84.0
mas install 1500855883 # CapCut 3.7.0
mas install 1456386228 # Clockology 1.4.8
mas install 1130254674 # CloudMounter 4.5
mas install 1516894961 # Codye 2.0.3
mas install 1531594277 # Color Widgets 4.5.1
mas install 6476814377 # com.xavyx.Easy-Face-Blur 1.4.2
mas install 595191960 # CopyClip 1.9.8
mas install 1487937127 # Craft 2.7.8
mas install 6476924627 # Create Custom Symbols 1.6
mas install 980888073 # Crypto Pro 8.0.0
mas install 640199958 # Developer 10.5.1
mas install 1588151344 # Essentials 1.5.2
mas install 923463607 # Faviconer 1.1.2
mas install 1462114288 # Grammarly for Safari 9.73
mas install 1460330618 # Hype 4 4.1.16
mas install 1487860882 # iMazing Profile Editor 1.9.0
mas install 408981434 # iMovie 10.4
mas install 409183694 # Keynote 14.0
mas install 1602158108 # Logo Maker 2.4
mas install 6445850897 # Logo Maker & Creator 3.7
mas install 1369145272 # Logo Maker - Design Monogram 10.2.3
mas install 1458866808 # MacFamilyTree 9 9.3.3
mas install 441258766 # Magnet 2.14.0
mas install 1480068668 # Messenger 208.0
mas install 462058435 # Microsoft Excel 16.83
mas install 784801555 # Microsoft OneNote 16.83
mas install 985367838 # Microsoft Outlook 16.83.3
mas install 462062816 # Microsoft PowerPoint 16.83
mas install 462054704 # Microsoft Word 16.83
mas install 1464222390 # Model Pro 1.2
mas install 1551462255 # MouseBoost 3.3.8
mas install 1592917505 # Noir 2024.1.9
mas install 409203825 # Numbers 14.0
mas install 1471867429 # OTP Auth 2.18.0
mas install 409201541 # Pages 14.0
mas install 600925318 # Parallels Client 19.3.24686
mas install 1085114709 # Parallels Desktop 1.9.2
mas install 1472777122 # PayPal Honey 16.5.1
mas install 715483615 # Picture Collage Maker 3 Lite 3.7.10
mas install 1289583905 # Pixelmator Pro 3.5.8
mas install 1571283503 # Redirect Web for Safari 5.1.1
mas install 403195710 # Remote Mouse 3.302
mas install 1503136033 # Service Station 2020.9
mas install 1095562398 # Shopping for Amazon 3.3.1
mas install 442168834 # SiteSucker 5.3.2
mas install 863015334 # Sparkle 5.5.1
mas install 1633701470 # Sticklets 1.1.1
mas install 1150887374 # Sticky Notes 2.1.2
mas install 1082989794 # Templates for Pixelmator 3.0.0
mas install 899247664 # TestFlight 3.5.1
mas install 425424353 # The Unarchiver 4.3.6
mas install 1241342461 # Transcribe 4.18.13
mas install 1450874784 # Transporter 1.2.5
mas install 1482454543 # Twitter 9.30
mas install 1211437633 # Universe 2023.47
mas install 497799835 # Xcode 15.3

# VSCode Extensions Installation
vscode "ahkohd.glance"
vscode "akvelonprimary.autocomment"
vscode "alefragnani.bookmarks"
vscode "alefragnani.project-manager"
vscode "alexmunteanu.toggle-block-comments"
vscode "andrsdc.base16-themes"
vscode "antfu.browse-lite"
vscode "antfu.vite"
vscode "atishay-jain.all-autocomplete"
vscode "bmalehorn.shell-syntax"
vscode "bmalehorn.vscode-fish"
vscode "bobmagicii.autofoldyeah"
vscode "casperstorm.directory-files"
vscode "chekweitan.compare-view"
vscode "chiro2001.digital-ocean-manager"
vscode "christian-kohler.npm-intellisense"
vscode "codesandbox-io.codesandbox-projects"
vscode "codestream.codestream"
vscode "codezombiech.gitignore"
vscode "coenraads.disableligatures"
vscode "ctf0.macros"
vscode "dae.vscode-mac-color-picker"
vscode "danidandev.comment-remover"
vscode "dart-code.dart-code"
vscode "dawranliou.minimal-theme-vscode"
vscode "dbaeumer.vscode-eslint"
vscode "devsense.composer-php-vscode"
vscode "devsense.intelli-php-vscode"
vscode "devsense.phptools-vscode"
vscode "devsense.profiler-php-vscode"
vscode "dhedgecock.radical-vscode"
vscode "dotiful.dotfiles-syntax-highlighting"
vscode "dsoloha.native-macos"
vscode "eamodio.gitlens"
vscode "ecmel.vscode-html-css"
vscode "eg2.vscode-npm-script"
vscode "esbenp.prettier-vscode"
vscode "evolution-gaming.evolution-gaming--vscode-eslint"
vscode "firefox-devtools.vscode-firefox-debug"
vscode "formulahendry.code-runner"
vscode "foxundermoon.shell-format"
vscode "github.codespaces"
vscode "github.remotehub"
vscode "github.vscode-pull-request-github"
vscode "golang.go"
vscode "gruntfuggly.todo-tree"
vscode "hoovercj.vscode-settings-cycler"
vscode "htmlhint.vscode-htmlhint"
vscode "ibm.output-colorizer"
vscode "inu1255.easy-snippet"
vscode "irongeek.vscode-env"
vscode "jabacchetta.vscode-essentials"
vscode "jacobkucera.codepen-theme"
vscode "jakearl.search-editor-apply-changes"
vscode "jasonlhy.hungry-delete"
vscode "jkjustjoshing.vscode-text-pastry"
vscode "jock.svg"
vscode "johnpapa.vscode-peacock"
vscode "jpruliere.env-autocomplete"
vscode "lacroixdavid1.vscode-format-context-menu"
vscode "lakshits11.best-themes-redefined"
vscode "lostintangent.vsls-whiteboard"
vscode "merko.merko-green-theme"
vscode "metaseed.metago"
vscode "metaseed.metajump"
vscode "metaseed.metaword"
vscode "mhutchie.git-graph"
vscode "micnil.vscode-checkpoints"
vscode "miguelsolorio.fluent-icons"
vscode "mikestead.dotenv"
vscode "moshfeu.diff-merge"
vscode "ms-python.debugpy"
vscode "ms-python.python"
vscode "ms-python.vscode-pylance"
vscode "ms-vscode-remote.remote-containers"
vscode "ms-vscode-remote.remote-ssh"
vscode "ms-vscode-remote.remote-ssh-edit"
vscode "ms-vscode.azure-repos"
vscode "ms-vscode.cmake-tools"
vscode "ms-vscode.live-server"
vscode "ms-vscode.makefile-tools"
vscode "ms-vscode.powershell"
vscode "ms-vscode.remote-explorer"
vscode "ms-vscode.remote-repositories"
vscode "ms-vscode.remote-server"
vscode "ms-vsliveshare.vsliveshare"
vscode "mubaidr.vuejs-extension-pack"
vscode "nerudevs.jellyfish-dark"
vscode "ngryman.codesandbox-theme"
vscode "nhoizey.gremlins"
vscode "peterschmalfeldt.explorer-exclude"
vscode "pkief.material-icon-theme"
vscode "pnp.polacode"
vscode "pranaygp.vscode-css-peek"
vscode "rassek96.vscode-comment-selection"
vscode "redhat.java"
vscode "remimarche.cspell-tech"
vscode "rioj7.vscode-json-validate"
vscode "ritwickdey.liveserver"
vscode "rvest.vs-code-prettier-eslint"
vscode "sankeyteam.dcd"
vscode "sdras.vue-vscode-snippets"
vscode "shayanalijalbani.next-jelly-fish"
vscode "simonsiefke.svg-preview"
vscode "skyapps.fish-vscode"
vscode "slevesque.vscode-multiclip"
vscode "smatdnepr.svg-sprite-viewer-generator"
vscode "stkb.rewrap"
vscode "streetsidesoftware.code-spell-checker"
vscode "svipas.code-autocomplete"
vscode "svipas.control-snippets"
vscode "tamasfe.even-better-toml"
vscode "timonwong.shellcheck"
vscode "tlevesque2.duplicate-finder"
vscode "tombonnike.vscode-status-bar-format-toggle"
vscode "tomoki1207.pdf"
vscode "trabpukcip.vscode-npm-scripts"
vscode "twxs.cmake"
vscode "usernamehw.errorlens"
vscode "victoriadrake.kabukicho"
vscode "visualstudioexptteam.intellicode-api-usage-examples"
vscode "visualstudioexptteam.vscodeintellicode"
vscode "vitest.explorer"
vscode "vscjava.vscode-java-debug"
vscode "vscjava.vscode-java-dependency"
vscode "vscjava.vscode-java-pack"
vscode "vscjava.vscode-java-test"
vscode "vscjava.vscode-maven"
vscode "vsls-contrib.gistfs"
vscode "vue.volar"
vscode "wayou.vscode-todo-highlight"
vscode "xabikos.javascriptsnippets"
vscode "xyz.local-history"
vscode "yakenoharashinnosuke.insistent-comments"
vscode "yutengjing.vscode-archive"
vscode "zgm.vscode-fish"
vscode "zignd.html-css-class-completion"
vscode "ziterz.codesandbox-black-theme"


# Handle specific configurations for Apple Silicon
on_apple_silicon do
  # Architecture-specific settings
  set_arch "arm64"
end
