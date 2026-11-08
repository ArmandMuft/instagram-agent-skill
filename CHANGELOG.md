# Changelog

## 1.1.0

### Fixed

- **humanize.py** left `growth.!` behind when a deleted phrase took its own
  punctuation with it ("...to unlock growth. Follow for more!"). The surviving
  sentence now keeps its full stop.
- **humanize.py** turned an em dash between two whole sentences into a comma
  splice ("your website is important, it's not just a page"). A dash in front
  of a new clause now becomes a full stop, and paired dashes around an aside
  become a pair of commas.
- **humanize.py** capitalised the word after an ellipsis ("Wait... What."). A
  trailing ellipsis is a pause, not a sentence end.
- **hookscore.py** never counted a proper noun as the payload word in
  FRONTLOAD. The "not at the start of the line" check ran on single words, so
  every name was at its own start and always failed.
- **swipe.py** crashed when `--out` was a plain filename with no folder.
- **slop.json** flagged five hashtags as a "wall" while `caption.py` treats
  five as the allowed maximum, and the fix text said LinkedIn. It now flags six
  or more, with Instagram's cap in the message.
- **ig-reel** showed example scores the script does not produce (86 STRONG
  for a hook that scored 51). The example now shows real output.

### Changed

- **hookscore.py** weights follow the measurement in the README: SPECIFICITY
  counts double, STAKES and ADDRESS count half. Only LENGTH, SPECIFICITY and
  FRONTLOAD can cap the score or be reported as the weakest property. A
  dealbreaker caps a hook at 49, so it can never rank as worth shooting.
  Generic hooks with nothing concrete in them no longer pass on "you" and
  "nobody" alone. Not re-validated against the original corpus, which is not
  in the repo.
- **Every writing skill reads voice.md.** The README said they did; only
  ig-reel and ig-plan actually did. Caption, carousel, story, profile, comment,
  reply, DM and repurpose now read it first.
- **Files work on claude.ai.** Skills look for `voice.md`, `swipe.md`,
  `log.md` and `plan.md` in `~/.claude/instagram/`, then in the project's
  knowledge, then in attached files. On claude.ai, where the working folder is
  wiped between chats, they hand over the contents to add to the project
  instead of claiming to have saved them.
- **ig-plan** plans to the cadence the user can hold, read from `voice.md`,
  instead of always pushing four to five posts a week. It rotates the content
  mix across a fortnight on lighter schedules and prioritises collab posts
  when the data shows they outperform.
- **ig-dm** adds a fourth kind of DM: the researched approach to a local
  business, for accounts that sell services to businesses, with its own
  four-line structure.
- **ig-audit** separates collab posts from solo posts before comparing them.
- **voice.md** template has a section for posting cadence, hours and collabs,
  and says where to keep the file on claude.ai versus Claude Code.
- **README** covers installing the plugin on claude.ai.
