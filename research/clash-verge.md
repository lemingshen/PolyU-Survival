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

* Visit the [installation page](https://www.clashverge.dev/install.html) to download the latest version of Clash Verge for your operating system (Windows, macOS, Linux).
* Follow the installation instructions provided on the website to set up Clash Verge on your device.

## 2. Import Configuration

* Open Clash Verge after installation.
* Click on the "Profiles" tab in the sidebar.
* Paste the URL I provided into the "Import from URL" field and click "Import".
<figure><img src="../.gitbook/assets/research/clash/import_config.png" alt=""><figcaption></figcaption></figure>

## 3. Select Preferred Nodes

* Click on the "Proxies" tab to view the list of available proxy nodes.
* Browse through the list and select your preferred nodes by clicking on them based on different rules.
<figure><img src="../.gitbook/assets/research/clash/select_node.png" alt=""><figcaption></figcaption></figure>
<figure><img src="../.gitbook/assets/research/clash/select_node2.png" alt=""><figcaption></figcaption></figure>

## 4. Start System Proxy

* Click on the "Home" tab.
* Select a proxy mode on the right panel
    * Rule Mode: Routes traffic based on predefined rules.
    * Global Mode: Routes all traffic through the selected proxy.
    * Direct Mode: Direct use your own network.
* Toggle the "System Proxy" switch to enable system-wide proxying.
<figure><img src="../.gitbook/assets/research/clash/start_proxy.png" alt=""><figcaption></figcaption></figure>


## 5. Additional Settings (Strongly Recommended)

* **Motivation**: In Hong Kong, we only need proxies for specific services (e.g., OpenAI, Gemini, Claude). Therefore, I recommend configuring Clash Verge to only route traffic for these services through the proxy, while allowing other traffic to use your own network (our university's network provides 1000 MB bandwidth!!!). This approach optimizes performance and reduces unnecessary load on the proxy servers. Also, the traffic flow consumption (2400 GB per year) can be saved.
* How to customize your configurations:
    * Click on the "Profiles" tab.
    * Right click on the previously imported profile and select "Edit Info"
    * Input "Clash_CN.yaml" in the "Name" field to rename the previously imported profile.
    <figure><img src="../.gitbook/assets/research/clash/rename_config.png" alt=""><figcaption></figcaption></figure>

    * Then, re-import the same configuration URL again and rename it to "Clash_HK.yaml".
    * Next, right click on "Clash_HK.yaml" and select "Edit File".
    * Scroll down and find the "rules:" section.
    <figure><img src="../.gitbook/assets/research/clash/replace_rules.png" alt=""><figcaption></figcaption></figure>

    * Replace all the existing rules with the following rules (last update: Jan 29, 2026):
    
    ```
    rules:
      - DOMAIN-SUFFIX,smtp,DIRECT
      - DOMAIN-KEYWORD,aria2,DIRECT

      - DOMAIN,browser-intake-datadoghq.com,🎬ai
      - DOMAIN,static.cloudflareinsights.com,🎬ai
      - DOMAIN-SUFFIX,ai.com,🎬ai
      - DOMAIN-SUFFIX,t-mobile.com,🎬ai
      - DOMAIN-SUFFIX,aistudio.google.com,🎬ai
      - DOMAIN-SUFFIX,ai.google.dev,🎬ai
      - DOMAIN-SUFFIX,algolia.net,🎬ai
      - DOMAIN-SUFFIX,meta.ai,🎬ai
      - DOMAIN-SUFFIX,api.statsig.com,🎬ai
      - DOMAIN-SUFFIX,labs.google.com,🎬ai
      - DOMAIN-SUFFIX,auth0.com,🎬ai
      - DOMAIN-SUFFIX,chatgpt.com,🎬ai
      - DOMAIN-SUFFIX,chatgpt.livekit.cloud,🎬ai
      - DOMAIN-SUFFIX,client-api.arkoselabs.com,🎬ai
      - DOMAIN-SUFFIX,events.statsigapi.net,🎬ai
      - DOMAIN-SUFFIX,featuregates.org,🎬ai
      - DOMAIN-SUFFIX,host.livekit.cloud,🎬ai
      - DOMAIN-SUFFIX,identrust.com,🎬ai
      - DOMAIN-SUFFIX,intercom.io,🎬ai
      - DOMAIN-SUFFIX,intercomcdn.com,🎬ai
      - DOMAIN-SUFFIX,launchdarkly.com,🎬ai
      - DOMAIN-SUFFIX,oaistatic.com,🎬ai
      - DOMAIN-SUFFIX,oaiusercontent.com,🎬ai
      - DOMAIN-SUFFIX,observeit.net,🎬ai
      - DOMAIN-SUFFIX,segment.io,🎬ai
      - DOMAIN-SUFFIX,sentry.io,🎬ai
      - DOMAIN-SUFFIX,play.google.com,🎬ai
      - DOMAIN-SUFFIX,stripe.com,🎬ai
      - DOMAIN-SUFFIX,turn.livekit.cloud,🎬ai
      - DOMAIN-KEYWORD,openai,🎬ai
      - DOMAIN-KEYWORD,gemini,🎬ai
      - DOMAIN-KEYWORD,sora,🎬ai
      - DOMAIN-KEYWORD,claude,🎬ai
      - DOMAIN-KEYWORD,tiktok,🎬ai
      - DOMAIN-KEYWORD,anthropic,🎬ai
      - DOMAIN-KEYWORD,tccd,🎬ai
      - DOMAIN-KEYWORD,notebooklm,🎬ai
      - DOMAIN-KEYWORD,aistudio,🎬ai
      - DOMAIN-KEYWORD,antigravity,🎬ai
      - DOMAIN-SUFFIX,oaiusercontent.com,🎬ai
      - DOMAIN-SUFFIX,deepmind.com,🎬ai
      - DOMAIN-SUFFIX,bard.google.com,🎬ai
      - DOMAIN-SUFFIX,generativelanguage.googleapis.com,🎬ai
      - DOMAIN-SUFFIX,makersuite.google.com,🎬ai

      - IP-CIDR,119.28.28.28/32,DIRECT,no-resolve
      - GEOIP,CN,DIRECT

      - MATCH,DIRECT
    ```
    * Then, right click on the "Clash_HK.yaml" profile and modify the "Update Interval" to a very very very large number. Otherwise, the rules will be overwritten during automatic updates.
    <figure><img src="../.gitbook/assets/research/clash/update_interval.png" alt=""><figcaption></figcaption></figure>
* As such, in Hong Kong, you can keep the proxy on the moment you start your PC. Only network traffics related to those domains listed in the rules will be routed through the proxy, while all other traffics will use your own network directly.
* You can freely adjust the node you like in the "🎬ai" section.
* In Hong Kong, you can choose the "Clash_HK.yaml" profile, while in China, you can switch to the "Clash_CN.yaml" profile to enjoy unrestricted internet access.
* Finally, change the system settings to make Clash Verge start automatically when your computer boots up:
<figure><img src="../.gitbook/assets/research/clash/system_setting.png" alt=""><figcaption></figcaption></figure>

* For windows users, please exempt all UWP processes from the proxy. Click on "Settings", scroll down, and find "Open UWP tool". Select all and click "Exempt All" and "Save Changes".
<figure><img src="../.gitbook/assets/research/clash/uwp.png" alt=""><figcaption></figcaption></figure>
<figure><img src="../.gitbook/assets/research/clash/uwp_exempt.png" alt=""><figcaption></figcaption></figure>


## 6. Setup on Mobile Devices

* For IOS devices, Shadowrocket is recommended. You can download Shadowrocket from the App Store (non-China region): [https://apps.apple.com/ca/app/shadowrocket/id932747118](https://apps.apple.com/ca/app/shadowrocket/id932747118)
* For Android devices, Clash for Android is recommended. You can download it from here: [https://en.clashforandroid.org/](https://en.clashforandroid.org/)
* Import configurations (Shadowrocket example):
    * Click "Config".
    * Click the "+" button at the top right corner.
    * Input the configuration URL I provided and click "Download".
    <figure><img src="../.gitbook/assets/research/clash/shadow.png" alt="" width="300pt"><figcaption></figcaption></figure>

* Click "Home", select a node, and toggle the switch (on the top) to start the proxy.


{% hint style="warning" %}
**I strongly recommend using nodes whose names start with "Pro-".**

To visit Google Scholar, nodes whose names contain "家庭宽带" should be selected.
{% endhint %}
   

