## New punishment system

Oliver has asked me to make a replacement for Carlbot, because there was a decent amount of issues with the punishment system, including people getting kicked (which doesn't resolve anything) to people getting 10s of punishments and still being allowed to chat and stay on the server.

### The system it's self:

If someone breaks a rule, rather than screenshotting and posting in a separate channel, and then reporting their id, this is collected into a single point, so the new report system, with the command 
```markdown 
!report
```
This new command will take 2 arguments:
```markdown
1. A discord message link. 
   Obtained by right-clicking a message + clicking "Copy message link"
2. An abbreviated rule
   Found on the forum e.g. Spamming = SP
```

You can find a list of the possible abbreviations/rules on the forum, or by doing
```markdown
!rule_list
```

An example of a valid report syntactically would be.

```markdown 
!report https://discord.com/channels/571681282652766208/715722306651029554/784164860484780093 SP
```

When this command is executed, you should see a reply from the bot acknowledging your report.
It'll give you information about the player you have reported, including their `nickname`, their `discord id`, and a `link` to the report embed that has been automatically generated in **#mod-logs**.

In the **#mod-logs** channel, you'll see your new report.
There are 2 stages of reports, `Low-tier` reports (<span style="color:blue">Blue</span>) and `High-tier` reports (<span style="color:orange">Orange</span>).


`Low-tier` reports (<span style="color:blue">Blue</span> reports) can be accepted by the person who submitted the report, Moderators and Administrators.
`High-tier` reports (<span style="color:orange">Orange</span> reports) can only be accepted by Moderators and Administrators, **not** Helpers.

If you have submitted a low-tier report, click the link or move to **#mod-logs** and check to make sure all the information in the embed is accurate. If the message you reported had an image, it'll be at the bottom of the auto-generated embed, if it had text, it'll be in the "Proof" line. It can have **both**.

If you submitted a `High-tier` report, you will need to wait for a Moderator to accept your report, as `High-tier` reports **cannot** be accepted by Helpers.

When you or a Mod reacts to a report embed, with either `Accept` or `Deny`, the embed will change colour and the message at the bottom that states "This report is on-going" will change to either
`This report was 'accepted' by X`, or `This report was 'denied' by X`. The emoji "buttons" will also disappear.

If the report is **Accepted**, the original message will be deleted, but the proof will stay in the embed. If someone requests the proof in which they were reported on, this is where you will find it.

When the report embed is generated, please make **absolutely sure** that **all** the information is correct, that the person who's getting the report is correct, the proof is correct etc. If it is, click `Accept`. If it's not, click `Deny`. If the information is not correct, please contact me and I'll investigate.

Data from that embed will be collected and then get inserted into the database, and their amount of `penalty points` will be calculated based on an exponential system, meaning breaking the same rule _twice_ will have _worse_ consequences the second time.
Depending on their amount of `penalty points`, they will be given a certain punishment, this is not left to a per-person basis, and is instead completely objective and done automatically, as to be more consistent.

They will get automatically banned/muted depending on their amount of `penalty points`, and then automatically unbanned/unmuted after their punishment is over. A new embed will appear in **#status** showing that they have been muted or banned, just to confirm that everything went though alright.
They will also get a message saying they have passed the point threshold and the length of their punishment.

Each punishment record "expires" (As in, is no longer counter) **30 days** after it has happened, with the one exception being if another punishment is already still active, in which
case, the second punishment will expire **30 days** _after_ the previous punishment expires.

To see someone's punishment history, you can do 
```markdown
!logs <user id> 
```
and a list of their history will appear.

If you believe someone was reported in an unfair way, and it got accepted, you can use 
```markdown
!remove_report <case_id>
```
and it'll remove the record from the database.

**WARNING It will not also unmute them/unban them, that needs to be done manually, it'll just remove the records from the database meaning subsequent punishments won't count it.**

If you still want to remove their mute manually, you can do
```markdown
!unmute <discord_id>
```

Finally, if you want to report someone for something such as spamming, and it's multiple messages, by the previous system, you'd just screenshot the whole thing and post it in #proof-material. With this system, report the last message in the spam chain, like you normally would, and then, when the report embed has been generated, copy the message link *of the report embed* and do 
```markdown
!add_evidence <copied message link>
```
And then also attach an image of the spamming, e.g. a cropped screenshot of the user spamming. This will edit the report embed to attach the image, so that if we need to look back, or they request the evidence, you can search for the case id, and see the image.

If you have any questions, ask me by either pinging me or send me a DM at Skezza#1139.

- Skezza
