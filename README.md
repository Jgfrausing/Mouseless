# My Journey for Seamless Keyboard Usage: A Nerd-Out Adventure

_Let's face it, I was a keyboard klutz. But as a software developer, that just wouldn't do. So, I embarked on a quirky, year-long mission to morph into a keyboard ninja. From wrestling with a compact Planck keyboard to overhauling my VSCode setup, this tale is about my geeky quest for coding harmony. Join me as I recount the ups, downs, and nerdy detours of making my fingers dance effortlessly across the keys._

To be honest, I am a terrible keyboard craftsman. As a software engineer, I have always felt embarrassed by that - how can I spend all day at a keyboard only to be able to type 40 words per minute? Previously, I often had to look down to find keys on the keyboard. Not in the sense that I had to search for them, but because my hands were rarely in the correct position, so I constantly had to adjust a little. There is an easy fix for this: learn the 10-finger system, where index fingers always return to the F and J keys. When coding, however, I find that I am navigating as much as I am actually typing. This means that the right hand is always switching between the arrow keys and back to its home position with the index finger on J when I am ready to start typing again. I have heard stories about how good typists forget that they are using a keyboard as the thoughts they have seem to magically appear on the screen without them thinking about how to type them. Having to move the hand, repositioning, and consequently, having to look down to adjust, I feel, is getting in the way of achieving this state of flow. This post is about my 1-year journey in the pursuit (nerd-out) of removing these obstacles.

## The Shift to Planck Keyboard:

About a year ago, I stumbled upon the Planck keyboard [link] by ZSA. This minimalist, 4-row, 37-keys layered device intrigued me. Its ortholinear layout was an interesting contrast to the staggered keys of traditional keyboards. The learning curve was steep, but the idea that the hands should never move away from the home row (index fingers on F and J), was intriguing. Albeit it meant that there were no obvious locations for arrow keys, numbers, F-keys, and a lot of other necessary keys.

## Configuring My Setup:

I was hoping that moving to a smaller keyboard would by default, prevent me from doing keyboard acrobatics. However, instead I had replaced the act of moving my hand with 20-or-so different complex key combinations where my mind and my fingers would engage in something I can best describe as playing piano while having epilepsy. To be able to do something as simple as marking two consecutive words, I had to hold down shift+ctrl+layershift and then press the arrow key on that new layer twice. While holding down three keys simultaneously is not something absurd, it still requires that I move my hand a lot and make unnatural hand postures. This was not what I had envisioned my "perfect setup" would feel like.

After six months of experimentation, I settled on a Vim-inspired setup. The 'F' and 'J' keys, usually home to my index fingers, became the gateways to a Vim navigation layer. Holding either of these down would allow me to navigate with Vim-like ease using W, B, H, J, K, 0, $, etc. This configuration allowed me to navigate through text in any editor or application seamlessly. Similarly, I also have keys for enabling a visual-, copying-, and deletion-layer. A sidenote - ZSA's configuration tooling is amazing.

## Avoid using my mouse

I have for years been a big fan of using Git CLI. Aside from requiring me to really understand what happens under the hood, it also relieves me from using a mouse. A mouse is, similarly to reaching for arrow keys, requires us to move our hand away from the home row. VSCode and many other editors have a good range of shortcuts to avoid using the mouse. However, with the default setup, I kept falling into the habit of using the mouse for many tasks. Each command seemed to have a different modifier. Some start with ctrl, others are just an F-key, etc. Also, ctrl+b opens the sidebar - unless you are in an .md file, in which case it makes something bold. This is not intuitive to me. The [Which Key extension](https://marketplace.visualstudio.com/items?itemName=VSpaceCode.whichkey) provides a common entry point for commands. An example could be C+f+f (C being a which-key trigger), which lets you search for a file and open it. This is similar to ctrl+p. At first glance, this seems to be an additional key press to do the same. However, what the first f does is opening all file-related commands. From here, you can also create a new file, rename a file, etc. C+tab goes to the previously opened file, C+x opens all text-related commands. All of this is of course customizable and if you forget a command you can press C+? which allows you to search for it.

### Transforming VSCode:

Using Which Key gives me a single entry point to commands. Whenever I encounter an action that requires me to use the mouse, I look for an option in Which Key. If none is available 9/10 times there is an extension that with commands that can be used. Before I dive into these, I will cover the changes I have made to the visual layout of VSCode. Using VSCode's Zen mode, I have a very simplistic layout:

- No tabs. Tabs allow you to use the mouse to switch to another file.
- The sidebar is hidden by default. The sidebar is very difficult to navigate without using the mouse, so hiding it forces usage of the keyboard, if possible.
- The bottom panel is also hidden by default. It contains a terminal tab and a problems tab. In addition, I have also moved the explorer from the sidebar to the panel, as this can be navigated using the keyboard easily.
  - This is mostly to gain an overview of the file structure when I forget.
- The scrollbar minimap is disabled. This is to me just a distraction.

The visual settings are configured by:

```
"zenMode.hideLineNumbers": false,
"zenMode.showTabs": "none",
"zenMode.hideStatusBar": true,
"zenMode.hideActivityBar": true,
"zenMode.restore": false,
"zenMode.fullScreen": true,
"zenMode.centerLayout": false,
"zenMode.silentNotifications": false,
"editor.minimap.enabled": false,
"workbench.statusBar.visible": false,
```

All of the above results in _just_ the current code file being visible when I am actually coding. I have easily accessible commands through Which Key to open the terminal, explorer, and problems tabs.

All of this has actually caused me to rotate my primary screen, as I no longer have a need for the width. Text is 125% to make reading a bit easier, while still being able to easily have +80 characters per line.

### Extensions

- [Which Key extension](https://marketplace.visualstudio.com/items?itemName=VSpaceCode.whichkey) - the enabler.
- [VSpaceCode](https://marketplace.visualstudio.com/items?itemName=VSpaceCode.vspacecode) - spacemacs-like bindings.
- [Advanced New File](https://marketplace.visualstudio.com/items?itemName=patbenatar.advanced-new-file) - create a new file in a location (instead of creating a new untitled)
- [Better Search](https://marketplace.visualstudio.com/items?itemName=travisthieman.better-search) - search solution. Results open as an editor with links to the results. This removes most of the needs for the search sidebar.
- [Fuzzy Search](https://marketplace.visualstudio.com/items?itemName=jacobdufault.fuzzy-search) - Fuzzy search in active file
- [File Browser](https://marketplace.visualstudio.com/items?itemName=bodil.file-browser) - Keyboard-driven file browser.

## The Challenges Along the Way:

Adopting this setup wasn't without its challenges. The initial weeks (months) with the new keyboard were riddled with typos and slow typing speeds as my fingers adjusted to the new layout. Customizing VSCode was a task of trial and error, balancing functionality with simplicity. But with each passing day, muscle memory kicked in, and the advantages began to outweigh the initial discomfort.

## Conclusion

This journey with my Planck keyboard and customized VSCode setup has been more than just about efficiency; it's been a journey of learning and personalization. It's a testament to how a bit of curiosity and willingness to experiment can lead to a significantly improved coding experience. For fellow developers looking to enhance their workflow, I highly recommend exploring the world of custom keyboards and IDE customizations. It might just change the way you code. And to answer your question; No, I will never get back the hours I have spent customizing my IDE or keyboard. If I had just done my job instead, productivity would have been way higher - but where's the fun in that?
