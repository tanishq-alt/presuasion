# presuasion

Two agent skills synthesized from influence / persuasion books using [book-to-skill](https://github.com/virgiliojr94/book-to-skill):

- **[cialdini-pre-suasion/](cialdini-pre-suasion/)** — knowledge base from *Pre-Suasion: A Revolutionary Way to Influence and Persuade* by Robert Cialdini. Pre-suasion, privileged moments, channeled attention, the seven universal principles of influence (reciprocation, liking, social proof, authority, scarcity, consistency, unity), associations, metaphor, geographies, if/when-then plans, ethical use, post-suasion.
- **[jones-exactly-what-to-say/](jones-exactly-what-to-say/)** — knowledge base from *Exactly What to Say: The Magic Words for Influence and Impact* by Phil M. Jones. 23 Magic Phrases for openers, follow-ups, objections, closing, referrals.

The two complement each other: **Cialdini** sets up *before* the conversation (the frame, the moment, the principle). **Jones** gives you the exact words *during* the conversation.

## Structure

```
cialdini-pre-suasion/
├── SKILL.md              (entry point)
├── glossary.md
├── patterns.md
├── cheatsheet.md
└── chapters/             (14 chapter files, loaded on demand)

jones-exactly-what-to-say/
├── SKILL.md              (entry point)
├── glossary.md
├── patterns.md
├── cheatsheet.md
└── chapters/             (23 chapter files, loaded on demand)
```

`SKILL.md` is the index — compact, always-loaded (<4K tokens). Chapters load on demand when you ask about a topic, so the skills stay small in context.

## Install (Claude Code)

```bash
# Clone
git clone <this-repo-url> ~/.agents/skills-presuasion
cd ~/.agents/skills-presuasion

# Symlink into ~/.claude/skills so Claude Code sees them
mkdir -p ~/.claude/skills
ln -sfn "$(pwd)/cialdini-pre-suasion" ~/.claude/skills/cialdini-pre-suasion
ln -sfn "$(pwd)/jones-exactly-what-to-say" ~/.claude/skills/jones-exactly-what-to-say
```

Restart Claude Code to pick up new skills.

## Install (other Agent Skills hosts)

Both skill folders follow the root-level `SKILL.md` convention and are installable with `npx skills add` on any Agent Skills–compatible host.

## Note on content

Each skill contains **synthesized summaries, not the book text.** The chapter files extract frameworks, principles, techniques, and worked examples — not raw passages. They are for study and application, not substitutes for the books. Both source books remain under third-party copyright; buy them from the authors/publishers if the frameworks are useful to you.
