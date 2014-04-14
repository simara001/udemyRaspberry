### Basic Configuration

#### Default Configuration

```bash
$ sudo raspbi-config
```

Here it is a quick explanation of the variables:

**Expand rootfs**
You should always choose this option; this will enlarge the filesystem to let you use the whole SD card.

**Overscan**
Leave the overscan option disabled at first. If you have a high definition monitor you may find that text runs off the side of the screen. To fix this, enable the overscan and change the values to fit the image to the screen. The values indicate the amount of overscan so the display software can correct; use positive values if the image goes off the screen, negative if there are black borders around the edge of the display.

**Keyboard**
The default keyboard settings are for a generic keyboard in a UK-style layout. If you want they keys to do what they’re labeled to do, you’ll definitely want to select a keyboard type and mapping that corresponds to your setup. Luckily the keyboard list is very robust. Note that your locale settings can affect your keyboard settings as well.

**Password**
It’s a good idea to change the default password from raspberry to something a little stronger.

**Change Locale**
If you’re outside the UK you should change your locale to reflect your language and character encoding preferences. The default setting is for UK English with a standard UTF-8 character encoding (en_GB.UTF-8). Select en_US.UTF-8 if you’re in the US.

**Change timezone**
You’ll probably want to set this.

**Memory split**
This option allows you to change the amount of memory used by the CPU and the GPU. Leave the default split for now.

**Overclock**
You now have the option of running the processor at speeds higher than 700MHz with this option. For your first time booting, leave the default settings or try Medium or Modest. You may want to return to this later (Turbo mode can run at 1000MHz).