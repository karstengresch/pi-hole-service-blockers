# pi-hole-service-blockers
Service definitions for easy Pi-hole group blocking.


## Rationale

Beside ad tracking and malicious site filtering, [Pi-hole](https://pi-hole.net) comes in handy to block DNS access to various internet services that often violate e.g. the guidelines of the [Center for Humane Technology](https://www.humanetech.com/) (which b.t.w. is supported by people actively engaging for the companies in critique) or - more important - are not following the guidelines of my all-time heroes of the [Electronic Frontier Foundation](https://www.eff.org/).

With Pi-hole's [group filter functionality](https://docs.pi-hole.net/database/gravity/example/) you can add the services you want to block for e.g. parental control, workplaces, or self focus, organize them into groups and then assign them to clients.

To do so, we need to add

  1. a wildcard domain for the service in question;
  2. link the wildcard domain to a group;
  3. link a client to this group.

Unfortunately (I), at the moment (2021-03-16) there's no way to add wildcard domains by lists: The handy "adlist" feature only supports exact matched domain names, but neither regex nor wildcard domains (which get automatically converted to wildcard).

Thus, you need to run a script (TBD) for adding the the wildcard domains and add them to your desired group.
Unfortunately (II), I couldn't find built-in ways for CLI
  * to create groups from the command-line
  * to map groups with (regex) domains with groups.

Therefor this quite tedious work needs to be made manually. The auto-generated comments can help you a bit.

## TO DO

  * remove domains for all or for specific services
  * create group for each service
  * link this service-group to created regex domain
  * command to link services to client
  * better documentation
  * UI
  * time based blocking/unblocking

*Issues/pull requests welcome.*

## Services that can be blocked
  * 9gag
  * amazon
  * cloudflare
  * dailymotion
  * dazn
  * discord
  * disneyplus
  * ebay
  * epicgames
  * facebook
  * hulu
  * imgur
  * instagram
  * mail(.ru)
  * netflix
  * ok
  * origin
  * pinterest
  * qq
  * reddit
  * snapchat
  * spotify
  * steam
  * telegram
  * tiktok
  * tinder
  * twitch
  * twitter
  * viber
  * vimeo
  * vk
  * wechat
  * weibo
  * whatsapp
  * youtube