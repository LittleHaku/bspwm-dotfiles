# Ivan's bspwm-dotfiles

<!-- Screenshot -->
![alttext](/assets/initial.jpg)

<p align="center">
  <b> Ivan's BSPWM dotfiles, inspired by s4vitar </b>
</p>

Welcome to my config file, I mainly did this following s4vitar's desktop tutorial [s4vitar's tutorial](https://www.youtube.com/watch?v=mHLwfI1nHHY), these are my first dotfiles and I'm not even sure if I'm missing something, I mainly do this to have a backup for my setup, and in case someone wants to use them feel free to do it.

##

**Here are some details about my setup:**
| Programs | Using |
|----------|-------|
| WM | bspwm |
| OS | Kali Linux|
| Shell| zsh |
| Terminal | qterminal |
| Editor | vscode
| Compositor | picom|
| Launcher | rofi |
| Themes[gtk3] | nordic |
|Icons | Flat-Remix-Blue-Dark |
| Terminal | JetBrainsMono Nerd
| Topbar | Polybar |

##
<!--<details>-->
<summary><strong>SETUP</strong></summary>

  > Take a look at S4vi's [pastebin](https://pastebin.com/EEX1Dsuq)

  1. Install dependencies
     + Dependencies
     + **Kali Linux** (Did this in Kali but should work in all debian based)

     ```shell
     apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev libxcb-keysyms1-dev libxcb-xinerama0-dev libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev
     ```

  2. Install BSPWM and SXHKD
      ```shell
      git clone https://github.com/baskerville/bspwm.git
      git clone <https://github.com/baskerville/sxhkd.git>
      cd bspwm/
      make
      sudo make install
      cd ../sxhkd/
      make
      sudo make install

      sudo apt install bspwm

      ```
    3. Install Polybar
       + Dependencies
       ```shell
       sudo apt install cmake cmake-data pkg-config python3-sphinx libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev libxcb-xkb-dev libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev libjsoncpp-dev libmpdclient-dev libcurl4-openssl-dev libnl-genl-3-dev
       ```

        + Installation
        ``` shell
        git clone --recursive https://github.com/polybar/polybar
        cd polybar/
        mkdir build
        cd build/
        cmake ..
        make -j$(nproc)
        sudo make install
        ```

      4. Install Picom
         + Dependencies
         ```shell
         sudo apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev libpcre2-dev libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev
         ```
         + Installation
         ```shell
         git clone https://github.com/ibhagwan/picom.git
         cd picom/
         git submodule update --init --recursive
         meson --buildtype=release . build
         ninja -C build
         sudo ninja -C build install
         ```
      5. Install Rofi
         ```shell
         sudo apt install rofi
          ```

<!--</details>-->