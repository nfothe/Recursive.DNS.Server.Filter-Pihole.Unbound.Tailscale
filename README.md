# Recursive.DNS.Server-Pihole.Unbound.Tailscale

This goal of this project was to utilize a spare Raspberry Pi 2 Model B I had laying around, to setup as a private, recursive DNS server and filter for my home network. 

I first installed Raspberry Pi OS to control the device. Then I connected it to my home network. 

Then I installed and configured Pi-hole, which I was able to use to filter the traffic on my home network. For example: blocking trackers that gather telemetry data, and blocking the custom advertisements that load on many websites.

I also installed and configured Unbound on the Raspberry Pi, which acts as the recursive DNS server. This enhances privacy by handling the IP address retrieval and caching directly from the root nameservers, rather than outsourcing the work to the local ISP and their corporate DNS servers, who would collect more of my data.

Installing Tailscale allowed me to take advantage of this technology while I am outside of the home. For example when taking my smartphone outside the home where it would connect to a cellphone tower, or when taking my laptop outside the home where it would connect to other Wi-Fi networks. Tailscale routes my device's traffic back to my Raspberry Pi DNS server at home, where it is protected from trackers and spam, before it loads at my device endpoint.

After the initial setup, it has been working for months with no complications, downtime, or noticeable latency/lag.
