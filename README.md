# Cyber Certs

A community-maintained list of cybersecurity certifications — cost, issuer, official link, security domain and skill level for each one.

Curated by [InfoSec Campus](https://infoseccampus.com) and published at [infoseccampus.com/cyber-certs](https://infoseccampus.com/cyber-certs/). This works is inspired by Paul Jerimy's [Security Certification Roadmap](https://pauljerimy.com/security-certification-roadmap/) into one filterable page.

Licensed under **[CC BY-SA 4.0](LICENSE.txt)**.

## The file

All data lives in [`cyber-certs/cyber-certs.json`](cyber-certs/cyber-certs.json), as a `meta` block plus a flat `certs` array:

```json
{
  "id": "crtp",
  "name": "CRTP",
  "full": "Certified Red Team Professional",
  "issuer": "Altered Security",
  "url": "https://www.alteredsecurity.com/post/certified-red-team-professional-crtp",
  "domain": "Security Operations",
  "level": "intermediate",
  "team": "red",
  "cost": "$249 (30-day lab + exam attempt); $99 re-attempt",
  "note": "Active Directory red teaming fundamentals."
}
```

| Field    | Required | Description |
|----------|:--------:|-------------|
| `id`     | ✅ | Unique, lowercase slug (letters, digits, hyphens). |
| `name`   | ✅ | Short display name, e.g. `"CRTP"`. |
| `full`   | ✅ | Full official certification name. |
| `issuer` | ✅ | Organisation that issues it. |
| `url`    | ✅ | Link to the **issuer's own page** for this certification — not a blog post, article or reseller. |
| `domain` | ✅ | One of the 8 values below — spelling and capitalisation must match exactly. |
| `level`  | ✅ | `"beginner"`, `"intermediate"`, or `"expert"`. |
| `team`   | ✅ | `"red"` or `"blue"` if offense/defense-focused, otherwise `null`. |
| `cost`   | ✅ | The certification's own price, as published by the issuer (e.g. `"$299 exam"` or `"Free"`). No travel, hotel or incidental costs. |
| `note`   | ✅ | One short, useful sentence (prerequisite, validity period, what's included), or `null`. |

Every field must be present in every entry — use JSON's `null` for `team`/`note` when they don't apply, rather than leaving the key out.

## How to contribute

1. Fork this repo.
2. Add your certification as a new object in the `certs` array in `cyber-certs.json`, filling in **every field** above (`null` for `team`/`note` if they don't apply).
3. Open a pull request.
4. InfoSec Campus reviews it against the issuer's own page and merges.

That's it — one entry, all fields filled in, one PR.

**Won't be merged:** certifications with no public, verifiable price; training with no exam or assessment; duplicate entries for an existing credential; affiliate/referral links instead of the issuer's own URL.

## Questions

Open an issue here, or reach InfoSec Campus at [infoseccampus.com](https://infoseccampus.com).
