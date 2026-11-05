# SACT competency passport

This repository holds the **SACT competency passport** framework, published by
Royal United Hospitals Bath NHS Foundation Trust. A framework is one published document written as a set
of competencies. Somebody records their progress against it in their
clinician passport in Quill.

## What is here

- `frameworks/ruh_sact_passport.yaml` is the framework itself. Its id is
  `ruh_sact_passport`, and every competency id in it starts with `ruh_sact_passport_`.

## How a change reaches Quill

1. Make the change on a branch named `feature/...`, and raise the
   framework's `version` by exactly one.
2. Open a pull request. The pipeline checks the file with Quill's own
   loader, and lists every competency whose wording changed.
3. Merge it. The pipeline starts Quill's framework sync, which stores the
   new version. Every earlier version stays, because a sign-off names
   the version it was made against.

A version never goes down, and a competency id is never removed.

## Licence

For now, the wording is under the same licence as Quill Medical, the GNU Affero
General Public License version 3. See `LICENSE`.
