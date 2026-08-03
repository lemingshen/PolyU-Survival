---
icon: cat
layout:
  width: default
  title:
    visible: true
  description:
    visible: true
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
---

# Clash Verge

[Clash Verge](https://www.clashverge.dev/) is a fork of the Clash project that focuses on enhancing the user experience and adding new features to the original Clash proxy tool. It aims to provide a more intuitive interface and improved performance for users who require advanced proxy functionalities.

## 1. Download & Installation

- Visit the [installation page](https://www.clashverge.dev/install.html) to download the latest version of Clash Verge for your operating system (Windows, macOS, Linux).
- Follow the installation instructions provided on the website to set up Clash Verge on your device.

## 2. Import Configuration

- Open Clash Verge after installation.
- Click on the "Profiles" tab in the sidebar.
- Paste the URL I provided into the "Import from URL" field and click "Import".
<figure><img src="../.gitbook/assets/research/clash/import_config.png" alt=""><figcaption></figcaption></figure>

## 3. Select Preferred Nodes

- Click on the "Proxies" tab to view the list of available proxy nodes.
- Browse through the list and select your preferred nodes by clicking on them based on different rules.
<figure><img src="../.gitbook/assets/research/clash/select_node.png" alt=""><figcaption></figcaption></figure>
<figure><img src="../.gitbook/assets/research/clash/select_node2.png" alt=""><figcaption></figcaption></figure>

## 4. Start System Proxy

- Click on the "Home" tab.
- Select a proxy mode on the right panel
  - Rule Mode: Routes traffic based on predefined rules.
  - Global Mode: Routes all traffic through the selected proxy.
  - Direct Mode: Direct use your own network.
- Toggle the "System Proxy" switch to enable system-wide proxying.
<figure><img src="../.gitbook/assets/research/clash/start_proxy.png" alt=""><figcaption></figcaption></figure>

## 5. Additional Settings (Strongly Recommended)

- **Motivation**: In Hong Kong, we only need proxies for specific services (e.g., OpenAI, Claude). Therefore, I recommend configuring Clash Verge to only route traffic for these services through the proxy, while allowing other traffic to use your own network (our university's network provides 1000 MB bandwidth!!!). This approach optimizes performance and reduces unnecessary load on the proxy servers. Also, the traffic flow consumption (2400 GB per year) can be saved.
- How to customize your configurations:
  - Click on the "Profiles" tab.
  - Right click on the previously imported profile and select "Edit Info"
  - Input "Clash_CN.yaml" in the "Name" field to rename the previously imported profile.
  <figure><img src="../.gitbook/assets/research/clash/rename_config.png" alt=""><figcaption></figcaption></figure>

  - Then, re-import the same configuration URL again and rename it to "Clash_HK.yaml".
  - Next, right click on "Clash_HK.yaml" and select "Edit File".
  - Scroll down and find the "rules:" section.
  <figure><img src="../.gitbook/assets/research/clash/replace_rules.png" alt=""><figcaption></figcaption></figure>

  - Replace all the existing rules with the following rules (last update: Feb 4, 2026):

  ```
  rules:
    - 'DOMAIN,sub-2025.gwshudong.lol,DIRECT'
    - 'RULE-SET,Local-LAN,DIRECT'
    - 'RULE-SET,SteamCN,DIRECT'
    - 'DOMAIN-SUFFIX,cm.steampowered.com,DIRECT'
    - 'DOMAIN-SUFFIX,steamserver.net,DIRECT'
    - 'DOMAIN-SUFFIX,steamcontent.com,DIRECT'
    - 'DOMAIN-SUFFIX,v.smtcdns.net,DIRECT'
    - 'DOMAIN-SUFFIX,snssdk.com,DIRECT'
    - 'DOMAIN-SUFFIX,playstation.net,DIRECT'
    - 'DOMAIN-SUFFIX,cnlang.org,DIRECT'
    - 'DOMAIN-SUFFIX,atlassian.com,DIRECT'
    - 'DOMAIN-SUFFIX,download.parallels.com,DIRECT'
    - 'RULE-SET,OpenAI,Ai+'
    - 'RULE-SET,Claude,Ai+'
    - 'RULE-SET,Domestic,DIRECT'
    - 'RULE-SET,CN-IP-ipcidr,DIRECT'
    - 'GEOIP,LAN,DIRECT'
    - 'GEOIP,CN,DIRECT'
    - 'MATCH,DIRECT'
  ```

  - Then, right click on the "Clash_HK.yaml" profile and modify the "Update Interval" to a very very very large number. Otherwise, the rules will be overwritten during automatic updates.
  <figure><img src="../.gitbook/assets/research/clash/update_interval.png" alt=""><figcaption></figcaption></figure>

- As such, in Hong Kong, you can keep the proxy on the moment you start your PC. Only network traffics related to those domains listed in the rules will be routed through the proxy, while all other traffics will use your own network directly.
- You can freely adjust the node you like in the "🎬ai" section.
- In Hong Kong, you can choose the "Clash_HK.yaml" profile, while in China, you can switch to the "Clash_CN.yaml" profile to enjoy unrestricted internet access.
- Finally, change the system settings to make Clash Verge start automatically when your computer boots up:
<figure><img src="../.gitbook/assets/research/clash/system_setting.png" alt=""><figcaption></figcaption></figure>

- For windows users, please exempt all UWP processes from the proxy. Click on "Settings", scroll down, and find "Open UWP tool". Select all and click "Exempt All" and "Save Changes".
<figure><img src="../.gitbook/assets/research/clash/uwp.png" alt=""><figcaption></figcaption></figure>
<figure><img src="../.gitbook/assets/research/clash/uwp_exempt.png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}

# Important

If you may use OpenAI or other AI tools in Windows Terminal, you MUST NOT exempt it. For example,

<figure><img src="../.gitbook/assets/research/clash/no_exempt.png" alt=""><figcaption></figcaption></figure>
{% endhint %}

## 6. Setup on Mobile Devices

- For IOS devices, Shadowrocket is recommended. You can download Shadowrocket from the App Store (non-China region): [https://apps.apple.com/ca/app/shadowrocket/id932747118](https://apps.apple.com/ca/app/shadowrocket/id932747118)
- For Android devices, Clash for Android is recommended. You can download it from here: [https://en.clashforandroid.org/](https://en.clashforandroid.org/)
- Import configurations (Shadowrocket example):
  - Click "Config".
  - Click the "+" button at the top right corner.
  - Input the configuration URL I provided and click "Download".
  <figure><img src="../.gitbook/assets/research/clash/shadow.png" alt="" width="300pt"><figcaption></figcaption></figure>

- Click "Home", select a node, and toggle the switch (on the top) to start the proxy.

{% hint style="warning" %}
**I strongly recommend using nodes whose names start with "Pro-".**

To visit Google Scholar, nodes whose names contain "家庭宽带" should be selected.
{% endhint %}
