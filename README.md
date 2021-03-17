# pi-hole-service-blockers
Service definitions for easy Pi-hole group blocking.


## Rationale

Beside ad tracking and malicious site filtering, [Pi-hole](https://pi-hole.net) comes in handy to block DNS access to various internet services that often violate e.g. the guidelines of the [Center for Humane Technology](https://www.humanetech.com/) (which b.t.w. is supported by people actively engaging for the companies in critique) or - more important - are not following the guidelines of my all-time heroes of the [Electronic Frontier Foundation](https://www.eff.org/).

With Pi-hole's [group filter functionality](https://docs.pi-hole.net/database/gravity/example/) you can add the services you want to block for e.g. parental control, workplaces, or self focus, organize them into groups and then assign them to clients.

To do so, we need to add

  1. a wildcard domain for the service in question;
  2. link the wildcard domain to a group;
  3. link a client to this group.

Unfortunately, at the moment (2021-03-16) there's no way to add wildcard domains by lists: The handy "adlist" feature only supports exact matched domain names (###).

Thus, you need to run a script (TBD) for adding the the wildcard domains and add them to your desired group.

Issues/pull requests welcome.

## List-URLs


