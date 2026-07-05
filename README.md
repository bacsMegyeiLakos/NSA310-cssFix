## Zyxel NSA310 cssFix

My NAS's specifications:
Firmware version: V4.70(AFK.2) (Patched against CVE-2020-9054)
Storage: 4TB WD RED

## Why is this?

For some reason my NAS's webUI shows some elements out of place or not centered, which is a bit odd... IDK if it's just me or everyone else who has the same NAS, but here's the fix.

## The fix

You need a way to inject CSS code into your webUI's code, for this I use the [Custom CSS by Denis](https://chromewebstore.google.com/detail/custom-css-by-denis/cemphncflepgmgfhcdegkbkekifodacd).

After installing the extension, grant permission to your NAS's IP and paste the following code:

div.dojoDialog {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}

This will center the popup boxes instead of having them at the bottom of the screen.

Before:
![kép](https://kephost.net/t/b5-LU4lYlWgBHEQ2qpjKoQ.png)
