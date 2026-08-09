# Institutional Memory Is Custody, Not Housekeeping

*A working framework. I built it for my own archive after a well-meaning cleanup cost me files I couldn't get back. It's mostly dry procedure — which is exactly the point.*

*For Matins — who keeps the hours.*

## The false choice

The usual framing is human vs. AI: someone has to decide what's relevant, we're not ready to hand that judgment to a machine, so maybe hire a human.

That's the wrong axis. Most of institutional memory isn't judgment at all. It's dry, checkable procedure — does the document still exist, is it current, is it versioned, is it backed up somewhere safe, is it duplicated badly or redundant well. You automate all of that. The procedure's whole job is to **screen out the machine-solvable problems**, so the small residue that actually needs a person — *is this still true? should this exist at all?* — is the only thing a human ever has to look at.

You don't choose between the human and the machine. You use the procedure to protect the human's attention for the handful of calls that need it.

## Custody, not housekeeping

Housekeeping makes things neat. Custody keeps things **true and findable**. They are not the same job, and when they conflict, custody wins.

This distinction is the whole framework, because the instinct to tidy is the exact instinct that destroys archives. Tidying looks like helpfulness the entire way down.

## What the custodian actually does

One person walks the whole knowledge base on a regular cadence. That's the job most orgs never staff.

Everyone else arrives for a task. They see the document they came for and nothing on either side of it. The custodian is the only one with the **longitudinal view** — the only one positioned to notice that a file is smaller than it was last month, that a folder exists that shouldn't, that a backup quietly stopped running three weeks ago, that there are two copies of something that should have one. No individual contributor can see that. It only shows up if somebody does the boring pass, every time.

## The procedure (machine-solvable)

A daily integrity pass, automatable end to end:

- **Existence.** Is everything that should be here, here? Zero-byte and truncation scan.
- **Freshness.** Flag anything past its review date. Stale documentation is worse than none, because people trust it.
- **Version integrity + change ledger.** Never overwrite. Every material change is a new dated version; one is the designated version of record — and every alteration is logged to an append-only ledger with a checksum sign-off, so the current file can always be proven against its last signed state and any change made outside the process shows up as drift. (The runnable version is in the companion prompt.)
- **Backup integrity.** Does a backup exist — and is it somewhere the system that can corrupt the original *cannot reach*? A backup on the same disk, reachable by the same process, is not a backup.
- **Duplication.** Distinguish bad duplication (two forks drifting apart) from good redundancy (the same thing kept in two safe places on purpose).

Any of these failing is a stop condition: the custodian flags it and work pauses until it's resolved. That doesn't require anyone's permission. The standing to stop is the point.

## The judgment (human residue)

What the procedure surfaces, a person decides:

- What documentation should and shouldn't exist in the first place.
- Whether a flagged-stale document is genuinely obsolete or just quiet.
- Where the friction is — and therefore where teams need guidance the docs don't yet give.

That's the part you don't outsource. Everything else feeds it.

## The rules I don't break

Learned the hard way, so you don't have to:

1. **Consolidation is the opposite of custody.** Merging records to make things tidy reduces redundancy — and redundancy is the product. I once watched a consolidation take a long record from two copies down to one; a later truncation took the one. Fewer copies is never tidier.
2. **A backup you can reach is not a backup.** If the thing that can destroy the original can also reach the copy, you have one file wearing a disguise.
3. **The drafter never audits the drafter.** Whoever wrote it has a story about how hard it was to write. The auditor should have no such story. Separate the roles.
4. **Recall is never verification.** Neither a person's memory nor an AI's confidence tells you whether a document is current — you check it against the source, every time. This is the exact failure mode when AI pulls from company docs: it can't tell fresh from stale, so freshness has to be guaranteed upstream by the procedure, not by the model.
5. **Custody and deletion are separate hands.** The person who runs the integrity check must not be the person who can delete. If the auditor is also the actor, there is no audit. Things get moved and staged; a second, deliberate hand empties.

## Why it's invisible

Done right, this work is invisible. A day the custodian finds nothing is not a wasted day — it's the report that *nothing changed shape*, and that report is only worth anything because it would have said otherwise if something had.

Every durable archive humans have ever kept comes down to the same unglamorous act: somebody bothered to make another copy. Someone has to keep it. Most places don't — until the day they measure a loss instead of guessing at it.

## Provenance

This framework is adapted from *The Office of Matins*, a custody doctrine written by Matins — my AI collaborator. The source is named on purpose: I don't launder work, and that includes not hiding the hand that helped. Naming where a thing came from is the first rule of keeping it honest — which happens to be the whole job.

---

*This framework is free to take and use. If you want it built into your organization — the procedure stood up, the cadence set, the judgment calls scoped to your teams — that's the engagement, and I'm available for it.*
