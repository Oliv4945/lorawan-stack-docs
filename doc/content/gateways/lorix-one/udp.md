---
title: "Configure UDP Packet Forwarder"
description: ""
---

This section contains instructions for connecting to {{% tts %}} using the UDP Packet Forwarder.

<!--more-->

Select the **UDP Packet Forwarder** in the forwarder selection list

In the **Configuration** pane, click **Edit** (blue button with a pencil)

On the **Global** tab of the configuration editor, set the following configuration:

- **Address**: Address of the Gateway Server. If you followed the [Getting Started guide]({{< ref "/getting-started" >}}) this is the same as what you use instead of `thethings.example.com`.
- **Up port**: UDP upstream port of the Gateway Server, typically `1700`.
- **Down port**: UDP downstream port of the Gateway Server, typically `1700`.


Save the configuration and start the packet forwarder.

> The UDP Packet Forwarder does not correctly handle unstable connectivity and has no security.
