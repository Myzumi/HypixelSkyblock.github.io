## The new report system - overview

The new report system includes 3 new channels:
```markdown 
#reports
#mod-logs
#status
```

Which each serve a different purpose, these will be explained later on in this post.

There is also a few more command which too will be explained later on. They are:

```markdown 
!report
!add_evidence
!rule_list
!logs
!remove_report
!view_case
!unmute
```

---

## Rational

```markdown
- The rational for this system were a large variety of reason.
- To eliminate the dependancy on CarlBot for punishments. 
- Carlbot having a multitude of finicky side effects.
- To create a more custom and tailored system, which works well for us.
- To eliminate subjectivity, and remove that bearing from the staff members.
- And many more.
```
---

## Definitions and explanations

To prefix the following section, some definitions and explanations might be necessery, although for many of you this is already second nature.

###### `1. A message link.`
A message link is a link given to you by discord when right clicking a message and clicking **"Copy message link"**.
It will be in this form: https://discord.com/channels/571681282652766208/715722306651029554/784164860484780093
Where the first id is the guild, the second the channel, and the third, the message id, you don't have to worry about these numbers, but being able to get a message link is very much necessery for this system to work.

###### `2. A report embed.`
This is an embed found in **#mod-logs** which was sent by the bot and contains all the information about a punishment: It's case id, the rule they broke, who reported them, the proof (In the form of text, an image, or both), and the report's status.
This will be the main point of proof, explaination of punishments, etc.

###### `3. The report categories.`
Each punishment will need to go under a category, these can be found by doing `!rule_list`.
When reporting, you should use the abbreviation (E.g. if they used spamming, you'd report for `SP`).
A more in-depth explanation of each rule can be found on the forum here: https://hypixelskyblock.de/forum/threads/skyblock-discord-staff-punishment-guidelines.43/

###### `4. Arguments and attachments.`
An argument is an input for a command, in text. For example, if we had an add command, such as `!add 5 6`
The *command* would be `add`, and both `5` and `6` both would be *arguments*.
If we had an `!upload` command, you might attach an image, this is an *attachment*, `!upload` might not take any *arguments*, but might take an *attachment*. Know the difference!

---

## Commands

The main command with this system is, predictably, `!report`.
This command takes 2 *arguments*.
###### `1. A message link.`
This message link will be obtained by right clicking a message of the person who has broken the rules, and the message inwhich they have done so. For example, is Person A sends two different messages, the first being "What costs more, a gold block or iron block" and their second being "I hope you die in a hole", you would report the second message.
###### `2. An abbreviated rule broken.`
An example of this might be "SP", "IRL" or "FB".

An example of a valid report command with correct syntax might be:
`!report https://discord.com/channels/571681282652766208/571708643888726017/794935864475910185 IC`

You would use this command in **#reports**, and with this new command, you generally don't need to also screenshot proof, or get the user's ID, with the only exception of this being Spamming (for the most part).

If something needs extra evidence, such as spamming (Since reporting one instance of what they spammed doesn't act as sufficient proof)
You can use the `!add_evidence` command.

This command takes 2 parameters.
1. A message link
2. An attachment, an image to act as more proof.

Nb: If you reported them for an image they sent, and add more proof, the original image will be overriden!

The message link in this instance, is *not* of the message you want to report, but instead, of the report embed that you want to add evidence to. So please head over to **#mod-logs**, right click the report embed, and copy that link, then attach the proof as an attachment.
This image can be a screenshot of the person spamming, spanning over multiple messages.

## Extra, less used commands:

### `!logs <target's discord id>`
This is similar to the old .modlogs, but will show their entire history, in a cleaner, more readable fashion.
Use this to see everyone who has reported someone, and for what.

### `!remove_report <case id>`
If someone was falsely reported, and it was accepted, you can remove this report from the database, just grab the case id, and use
!remove_report. 
Nb: This will not undo any punishments, e.g. if it caused them to get muted, this will not unmute them, so use the following command to do that.

### `!unmute <discord_id>`
Unmutes someone if they were falsely muted.

### `!view_case <case id>`
Shows all information about a case, e.g. the user, the staff member, when it happened, etc.

### `!rule_list`
Shows all the rules and abbreviations.

---

## Reports

When a report has been made, it'll either be a <span style="color:blue">Low Tier Report</span> (for less serious things, such as Spamming, etc) which will lead to a mute on the first instance, or a <span style="color:orange">High Tier Report</span> (IRL trading, Scamming etc).

If it's <span style="color:orange">High Tier Report</span>, it'll need to be accepted by a mod, and will be <span style="color:orange">Orange</span>. (Mods will also be pinged)
If it's <span style="color:blue">Low Tier Report</span>, it'll need to be accepted by the person who reported it or a mod, and be <span style="color:blue">Blue</span> (Mods can accept or deny any report).

Once it's accepted, it'll change to <span style="color:green">Green</span>, and **#status** will show that the punishment has taken effect (It will also show when the punishment has warn off).

When it's accepted, the user will get a certain amount of **penalty points**. This varies for each punishment but it goes between 1 and 8.
- Having 1 point is a 1 day mute.
- Having 5 points is a 30 day ban.
- Having 8 points is a permanent ban.

And all the ones in-between. They will be notified of the punishment, the type of punishment (mute or ban), the length, and for what for. They will **not** be told who reported them. This is confidential.

The amount of points varies for each category, but SP is 1 point, and IRL is 8 points.
Punishments will expire after 30 days, but only if no active punishments exist, e.g. if you're half way through one punishment, and get another, the second one will expire in 15 (from the previous punishment) + 30 days (for the second punishment).

For breaking the same rule twice, the amount of points will *increase*, compared to the base value for each punishment.
E.g. SP - Spamming is 1 point, but the second instance, it would add 1.4 points (1 for the base, +0.4 for the second time), and then 1.8 points etc.

This is to prevent people from breaking the rules once a month and being just fine, if they spam enough (even when serving the punishments) they will eventually be banned.

What this means is that staff are no longer held responsible for dictating the punishment length or severity, and are instead more focused on reporting people breaking the rules, and generally helping out amongst the server and being good role models for players.

This system may be a little overwelming to begin with, but makes a lot of sense when you get used to it, and should steamline reporting people, getting them punished, helping find evidence, and more.

If you do have any questions, please contact Skezza in DMs or #staff-chat.
