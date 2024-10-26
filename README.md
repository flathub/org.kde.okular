# Okular (org.kde.okular)

## Permissions rationale

This application requests the following additional permissions:

- Read/write access to the host filesystem: `--filesystem=host`.
  Required for ‘Open Recent’ and for drag & drop support,
  see [QTBUG-91357](https://bugreports.qt.io/browse/QTBUG-91357).
  Write access required for ‘Annotations’ and ‘Digitally Sign…’.
- Access to network: `--share=network`.
  Required for opening URLs.
- Access to audio: `--socket=pulseaudio`.
  Required for PDFs with sounds, see https://okular.kde.org/formats/.
- Bluetooth access: `--allow=bluetooth`.
  Required for ‘Send via Bluetooth…’.
- Talk to session D-Bus: `--talk-name=org.freedesktop.ScreenSaver`.
  Required to inhibit screen saver while presenting.
- Talk to session D-Bus: `--talk-name=org.freedesktop.login1`.
  Required to inhibit sleep while presenting.
