---
description:
  This module provides a collective timeline of all actions taken within the project. These detailed records allow for
  auditing user activity and enforcing accountability.
readTime: 2 min read
---

# Activity Log

> This module provides a collective timeline of all _data-changing_ actions taken within your project. These detailed
> records help you audit user activity and enforce accountability.

## Overview

<video title="Activity Log Overview" autoplay playsinline muted loop controls>
	<source src="https://cdn.directus.io/docs/v9/configuration/activity-log/activity-log-20220816/activity-log-20220816A.mp4" type="video/mp4" />
</video>

The Activity Log is the only Module in Directus Core that is not found in the
[Module Bar](/app/overview.html#_1-module-bar). Instead, it is accessed via the notifications tray of the
[Sidebar](/app/overview#_4-sidebar). The Activity Log page has the same features and functionality as the
[Collection Page](/app/content/collections).

To ensure proper accountability, the majority of activity items are **readonly** by design. However, users with an Admin
role do have the ability to modify **Create** and **Update** items from the Activity Log that were generated in the last
day.

You can also filter activities by type from the Navigation Bar.

::: warning External Changes

The platform can only track the events which actually pass through it. Therefore, any changes made to the database
_directly_ are not tracked.

:::

## Activity Log Default Fields

![Activity Log Default Fields](https://cdn.directus.io/docs/v9/configuration/activity-log/activity-log-20220816/activity-log-default-fields-20220816A.webp)

The following information is stored for each item in the activity log.

- **User** — The platform user that performed the action
- **Action** — The specific action taken, e.g., Create, Update, Delete, Authenticate
- **TimeStamp** — The timestamp of when the action was performed
- **IP Address** — The IP address of the device from which the action was performed
- **User Agent** — The description of the browser that was used to perform the action
- **Collection** — The Collection affected by the action
- **Item** — The item (within the above Collection) affected by the action
- **Comment** — When applicable; the comment left by the user
