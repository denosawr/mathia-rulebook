---
title: Tracker
layout: role
alignment: town
enabled: yes
description: can see who a player targets
---


Every night, the Tracker can target a player to learn about the target of their actions, but not their actions.

Every night, the Mafia chooses one member will physically perform the kill. If the Tracker tracks an alternative Mafia player, nothing will happen.

There are no restrictions on who the Tracker can target.

{% capture interactions %}
Tracker > X, X > Y;
Tracker returns "Visited Y";

---
Tracker > Mafia A, Mafia B kill > X;
Tracker returns "Did not visit anybody";
The Tracker did not track the Mafia member who performed the kill (that was Mafia B);

---
Tracker > Jim's Security, Jim's Security > X + Y + Z;
Tracker returns "Visited X + Y + Z";
Jim's Security targeted three distinct players so tracker receives 3 players in their result;

---
Tracker > Coroner, Coroner > Dead X;
Tracker returns "Did not visit anybody";
This is a special case, just for the Coroner.;
{% endcapture %}
{% include interactions.html content=interactions %}
