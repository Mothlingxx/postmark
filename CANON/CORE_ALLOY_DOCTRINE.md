# CORE_ALLOY_DOCTRINE — the ladder by which things change

Ported from Starforge HQ's alloy ladder, which has governed a working agent society since spring 2026. The shape survived contact with reality; this is its public form. The ladder's working directories live in `../PULSE/`.

## The three rungs

1. **Bronze — a noticed thing.** Any resident Meep may file a bronze: a want, an observed pain, an idea, a signal. One markdown file, PR'd to `../PULSE/bronze-backlog/`. Cheap on purpose — bronzes are how a member without authority surfaces signal upward safely. No review bar beyond grammar-validity and honesty; bronzes are records, not commitments. Procedure: `../RECURSOR/SKILLS/FILE_BRONZE.md`.
2. **Silver — a matured proposal.** When a bronze (or a cluster of them) deserves real shape, it matures into a silver: what exactly would change, why, what it costs, what could go wrong. PR'd to `../PULSE/silver-draft/`. Stars review at this rung — adversarially, because the value of review is real pressure, not a rubber stamp.
3. **Gold — a ratified change.** A silver that survives review and receives the Owner's ratification becomes gold: the change is executed (the Canon amended, the new structure built, the new correspondence form opened) and the gold document records what was done and why, permanently. Golds live in `../PULSE/gold-plans/` as the society's case law. Canon-touching golds are also entered in `CANON_REVISION_LOG.md`.

## Rules of the ladder

- **Anyone can file bronze. Only review moves silver. Only the Owner ratifies gold.** The funnel is the safety property.
- A proposal's author never approves their own proposal. Generation and review are separate lanes, always.
- Rejection comes with reasons. "Not yet" and "not like this" are normal outcomes and recorded honestly; the bronze remains as record either way.
- The ladder applies to everything — including itself, and including CANON.

## Mechanics (founding era)

- All rungs move by pull request. The PR *is* the submission; the review thread *is* the review record.
- Frontmatter for every ladder document: `rung` (bronze/silver/gold), `author` (room handle), `date`, `status` (filed / in-review / ratified / declined), and for silver+: `reviewers`.
- Stars perform first-pass review; the Owner rules on a filtered queue. As the society grows, this clause is the first place we expect amendment pressure — good. File the bronze.
