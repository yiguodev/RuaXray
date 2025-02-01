# RuaXray

RuaXray is a cross platform Xray-core and Hysteria 2 client. You need to have a certain understanding of Xray-core and Hysteria 2 to use this client smoothly.


This application does not collect user network activity data. All data will remain on your device and will not be uploaded to our servers.


This application does not include any VPN service. You need to build your own Xray-core or Hysteria 2 server, or purchase Xray-core or Hysteria 2 nodes. Please comply with local laws when using this application.


Protocols:

1. VLESS (supports reality)
2. VMess
3. Shadowsocks
4. Trojan
5. Socks
6. Hysteria 2


Transports:

1. RAW (tcp)
2. XHTTP
3. mKCP
4. gRPC
5. WebSocket
6. HTTPUpgrade
7. Hysteria 2


Subscription:

1. Support VMessAEAD/VLESS sharing protocol and Xray json configuration.
2. Support Clash.Meta configuration.
3. Support Hysteria 2 URI scheme.
4. Support importing configuration through camera, album, file, clipboard or link.

[Privacy Policy](https://yiguo.dev/privacy/)

## Supported Platform

| Distribution | Version                   | Architecture         |
| ------------ | ------------------------- | -------------------- |
| macOS        | 12.0 (Monterey) and above | Apple Silicon, Intel |
| iOS          | 15.5 and above            | aarch64              |
| Android      | 9.0 (Pie) and above       | aarch64, x86_64      |
| Ubuntu       | 24.04 (Noble Numbat)      | aarch64, x86_64      |
| Debian       | 12 (bookworm)             | aarch64, x86_64      |

Other linux distributions should also work, but we don't test them.

## Usage

### Linux

#### deb package

```shell
sudo dpkg -i ruaxray-{version}-linux-{architecture}.deb
```

#### zip package

Before start the app, install the dependencies.

```shell
sudo apt install -y libcap2-bin
sudo apt install -y libayatana-appindicator3-1
```
Then, grant these files network permissions.

```shell
cd ruaxray/bin
sudo setcap cap_net_admin+epi ruax.tun
sudo setcap cap_net_admin+epi ruax.core
```

Here is a template desktop file, you can edit it and put it in the applications folder.

```
[Desktop Entry]
Name=RuaXray
Comment=Cross Platform Xray-core and Hysteria 2 client
Exec=${ReplaceMeWithRealPath}/ruaxray
Icon=${ReplaceMeWithRealPath}/data/flutter_assets/assets/logo.png
Terminal=false
Type=Application
Categories=Network;
```

```shell
nano ~/.local/share/applications/ruaxray.desktop
```
