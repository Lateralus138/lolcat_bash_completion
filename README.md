# lolcat Bash Completion

1. [About](#about)
   1. [Description](#description)
      1. [What Is Bash Completion](#what-is-bash-completion)
   2. [Motivation](#motivation)
   3. [File](#file)
      1. [File Information](#file-information)
      2. [Current lolcat Bash Completion File MD5](#current-lolcat-bash-completion-file-md5)
2. [Usage](#usage)
   1. [Obtaining](#obtaining)
   2. [Installation](#installation)
   3. [Use](#use)
3. [LICENSE](#license)
4. [Support Me If You Like](#support-me-if-you-like)

---

## About

### Description

<details>
  <summary>Under Construction</summary>
  This README is not finished, but the the script/release should work just fine.
</details>

Very basic Bash completion file for the program 'lolcat' found here (and other forks):

[https://github.com/busyloop/lolcat](https://github.com/busyloop/lolcat)

This simply provides a basic word list of the switches provided in the program; the script verbatim:

```Bash
# Very basic Bash completion for 'lolcat'.
# Filenames can be implemented if ever a
# -P, --path, or --file switch is ever
# added to the program. There are ways
# this can be achieved without a switch
# but not always reliable.

lolcat_opts=(
  -h --help
  -p --spread
  -F --freq
  -S --seed
  -a --animate
  -d --duration
  -s --speed
  -f --force
  -v --version
)
complete -W "$(printf '%s\n' "${lolcat_opts[@]}")" lolcat
unset lolcat_opts

```

#### What Is Bash Completion

Bash completion allows one to list or auto-complete a program's options/switches by pressing the [*Tab*] key ([Tab][Tab]... to circulate through them).

Various web searches on "what is Bash Completion" (Google is blocked on anything I own, of course, you're free to do your own search):

Duck Duck Go: [https://duckduckgo.com/?q=What+is+Bash+completion&ia=web](https://duckduckgo.com/?q=What+is+Bash+completion&ia=web)

Ecosia (Bing): [https://www.ecosia.org/search?method=index&q=what%20is%20Bash%20Completion](https://www.ecosia.org/search?method=index&q=what%20is%20Bash%20Completion)

Bing: [https://www.bing.com/search?q=What+is+Bash+Completion&ghsh=0&ghacc=0&ghpl](https://www.bing.com/search?q=What+is+Bash+Completion&ghsh=0&ghacc=0&ghpl)

### Motivation

Some (at least the APT/Debian version for all I know) versions of ***lolcat*** don't come with Bash Completion and I wanted it. Plain and simple.

### File

#### File Information

![COMPLETE FILE SIZE](https://img.shields.io/github/size/Lateralus138/lolcat_bash_completion/usr/share/bash-completion/completions/lolcat?label=lolcat%20bash%20completion%20file%20Size&labelColor=1d1d1d&color=ffff99&style=for-the-badge)

#### Current lolcat Bash Completion File MD5

This information is generated in a *GitHub Action* immediately after the successful build of this project.

![Linux MD5](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/Lateralus138/lolcat_bash_completion/master/docs/json/lolcat_complete_md5.json)

---

## Usage

### Obtaining

You can either download it from the [Releases](https://github.com/Lateralus138/lolcat_bash_completion/releases) page, the [file](./usr/share/bash-completion/completions/lolcat) itself directly from the source directory, or copy and paste it from the script displayed above into your own file (but it must be named '*lolcat*').

### Installation

Bash Completion files in **Linux** are located (from my experience) in the directory `/usr/share/bash-completion/completions` and as such this file must be placed there.

Since it is in a system directory it must be installed with root priveldges (assuming sudo isn't disabled (or for some reason? if a user is root)).

You can copy the file from wherever you downloaded it to either by using a file manager as root (not necessarily recommended) or from the command line (recommended):

```Bash
sudo cp /path/to/the/downloaded/file /usr/share/bash-completion/completions

# more than likely:

sudo cp ~/Downloads/lolcat /usr/share/bash-completion/completions

# you can also download and install with curl (or wget or axel) (don't have to remove (rm), that's your preference):

curl -O "https://raw.githubusercontent.com/Lateralus138/lolcat_bash_completion/master/usr/share/bash-completion/completions/lolcat" &&
sudo cp lolcat  /usr/share/bash-completion/completions/lolcat &&
rm lolcat

```

Removal:

Simlply delete the completion file with a file manager as root (NOT recommended) or from the command line (recommended):

```Bash
sudo rm /usr/share/bash-completion/completions/lolcat
```

and reload your shell.

### Use

Bash Comletion is usually enabled for most Bash shells and as long as the completion file is in the correct directory it should load when you start a Bash shell. If you want to enable it directly after installation from the command line:

```Bash
. /usr/share/bash-completion/completions/lolcat

# or

source /usr/share/bash-completion/completions/lolcat

```

Once loaded you can use the lolcat's completion the same way as any other with [*Tab*] as stated above.

---

## [LICENSE](./LICENSE)

![License Info](https://img.shields.io/github/license/Lateralus138/lolcat_bash_completion?style=for-the-badge&labelColor=1D1D1D&color=ffff99)

<details>
  <summary>License Excerpt</summary>
  <br>
  <blockquote>
  &#x20;&#x54;&#x68;&#x69;&#x73;&#x20;&#x70;&#x72;&#x6F;&#x67;&#x72;&#x61;&#x6D;&#x20;&#x69;&#x73;&#x20;&#x66;&#x72;&#x65;&#x65;&#x20;&#x73;&#x6F;&#x66;&#x74;&#x77;&#x61;&#x72;&#x65;&colon;&#x20;&#x79;&#x6F;&#x75;&#x20;&#x63;&#x61;&#x6E;&#x20;&#x72;&#x65;&#x64;&#x69;&#x73;&#x74;&#x72;&#x69;&#x62;&#x75;&#x74;&#x65;&#x20;&#x69;&#x74;&#x20;&#x61;&#x6E;&#x64;&sol;&#x6F;&#x72;&#x20;&#x6D;&#x6F;&#x64;&#x69;&#x66;&#x79;&#x20;&#x69;&#x74;&#x20;&#x75;&#x6E;&#x64;&#x65;&#x72;&#x20;&#x74;&#x68;&#x65;&#x20;&#x74;&#x65;&#x72;&#x6D;&#x73;&#x20;&#x6F;&#x66;&#x20;&#x74;&#x68;&#x65;&#x20;&#x47;&#x4E;&#x55;&#x20;&#x47;&#x65;&#x6E;&#x65;&#x72;&#x61;&#x6C;&#x20;&#x50;&#x75;&#x62;&#x6C;&#x69;&#x63;&#x20;&#x4C;&#x69;&#x63;&#x65;&#x6E;&#x73;&#x65;&#x20;&#x61;&#x73;&#x20;&#x70;&#x75;&#x62;&#x6C;&#x69;&#x73;&#x68;&#x65;&#x64;&#x20;&#x62;&#x79;&#x20;&#x74;&#x68;&#x65;&#x20;&#x46;&#x72;&#x65;&#x65;&#x20;&#x53;&#x6F;&#x66;&#x74;&#x77;&#x61;&#x72;&#x65;&#x20;&#x46;&#x6F;&#x75;&#x6E;&#x64;&#x61;&#x74;&#x69;&#x6F;&#x6E;&comma;&#x20;&#x65;&#x69;&#x74;&#x68;&#x65;&#x72;&#x20;&#x76;&#x65;&#x72;&#x73;&#x69;&#x6F;&#x6E;&#x20;&#x33;&#x20;&#x6F;&#x66;&#x20;&#x74;&#x68;&#x65;&#x20;&#x4C;&#x69;&#x63;&#x65;&#x6E;&#x73;&#x65;&comma;&#x20;&#x6F;&#x72;&#x20;&lpar;&#x61;&#x74;&#x20;&#x79;&#x6F;&#x75;&#x72;&#x20;&#x6F;&#x70;&#x74;&#x69;&#x6F;&#x6E;&rpar;&#x20;&#x61;&#x6E;&#x79;&#x20;&#x6C;&#x61;&#x74;&#x65;&#x72;&#x20;&#x76;&#x65;&#x72;&#x73;&#x69;&#x6F;&#x6E;&period;
  </blockquote>
  <br>
  <blockquote>
  &#x54;&#x68;&#x69;&#x73;&#x20;&#x70;&#x72;&#x6F;&#x67;&#x72;&#x61;&#x6D;&#x20;&#x69;&#x73;&#x20;&#x64;&#x69;&#x73;&#x74;&#x72;&#x69;&#x62;&#x75;&#x74;&#x65;&#x64;&#x20;&#x69;&#x6E;&#x20;&#x74;&#x68;&#x65;&#x20;&#x68;&#x6F;&#x70;&#x65;&#x20;&#x74;&#x68;&#x61;&#x74;&#x20;&#x69;&#x74;&#x20;&#x77;&#x69;&#x6C;&#x6C;&#x20;&#x62;&#x65;&#x20;&#x75;&#x73;&#x65;&#x66;&#x75;&#x6C;&comma;&#x20;&#x62;&#x75;&#x74;&#x20;&#x57;&#x49;&#x54;&#x48;&#x4F;&#x55;&#x54;&#x20;&#x41;&#x4E;&#x59;&#x20;&#x57;&#x41;&#x52;&#x52;&#x41;&#x4E;&#x54;&#x59;&semi;&#x20;&#x77;&#x69;&#x74;&#x68;&#x6F;&#x75;&#x74;&#x20;&#x65;&#x76;&#x65;&#x6E;&#x20;&#x74;&#x68;&#x65;&#x20;&#x69;&#x6D;&#x70;&#x6C;&#x69;&#x65;&#x64;&#x20;&#x77;&#x61;&#x72;&#x72;&#x61;&#x6E;&#x74;&#x79;&#x20;&#x6F;&#x66;&#x20;&#x4D;&#x45;&#x52;&#x43;&#x48;&#x41;&#x4E;&#x54;&#x41;&#x42;&#x49;&#x4C;&#x49;&#x54;&#x59;&#x20;&#x6F;&#x72;&#x20;&#x46;&#x49;&#x54;&#x4E;&#x45;&#x53;&#x53;&#x20;&#x46;&#x4F;&#x52;&#x20;&#x41;&#x20;&#x50;&#x41;&#x52;&#x54;&#x49;&#x43;&#x55;&#x4C;&#x41;&#x52;&#x20;&#x50;&#x55;&#x52;&#x50;&#x4F;&#x53;&#x45;&period;&#x20;&#x20;&#x53;&#x65;&#x65;&#x20;&#x74;&#x68;&#x65;&#x20;&#x47;&#x4E;&#x55;&#x20;&#x47;&#x65;&#x6E;&#x65;&#x72;&#x61;&#x6C;&#x20;&#x50;&#x75;&#x62;&#x6C;&#x69;&#x63;&#x20;&#x4C;&#x69;&#x63;&#x65;&#x6E;&#x73;&#x65;&#x20;&#x66;&#x6F;&#x72;&#x20;&#x6D;&#x6F;&#x72;&#x65;&#x20;&#x64;&#x65;&#x74;&#x61;&#x69;&#x6C;&#x73;&period;
  </blockquote>
</details>

---

## Support Me If You Like

If you like this project and care to donate to my ***PayPal***:

[![PayPal Donation](./docs/media/images/paypal_donate_button.png)](https://paypal.me/ianapride?locale.x=en_US)

Or ***Buy Me A Coffee*** if your prefer:

[![Buy Me A Coffee](./docs/media/images/buymeacoffe_a.png)](https://www.buymeacoffee.com/ianalanpride)