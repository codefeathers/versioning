# codever

`codever` is CodeFeathers's versioning system. Answer to debates about whether or not another standard is required: [Standards](https://xkcd.com/927). It's okay to have just one more.

> Node: To facilitate your program working with other programs, it's necessary to be compatible with [semver](https://semver.org). But since this is a restriction, I've decided to have an internal version number and external version number. CodeFeathers projects must always have an internal `codever` number, and if any use in external applications is anticipated, an external `semver` version number can also used when a release is created, thereby removing the ugly `-b0.8.2` qualifiers.

x.y.z.yyyymmdd

X is major, Y is feature update (backwards compatible) and Z is minor. yyyymmdd is optional but useful for daily builds and patch releases.

0.1.z to 0.9.z is considered pre release and 1.0.0 is stable. Any updates should be done from 1.0.z to 1.8.z. 1.9.0 onwards is considered new version, which lands in 2.0.0

## Format

**X.Y.Z.yymmdd-p** OR **X.Y.Z**

- WHERE
  - `X` is a major version which introduces new features that are potentially backwards incompatible or could require a migration.
  - `Y` is a backwards compatible feature update.
  - `Z` is a minor update.
  - `yymmdd` Patch numbers are dated. Backdating is not allowed for any projects that are taken up from before 2000. This part can be completely ignored in case of a new minor update is released later.
  - In case multiple patches are released on the same day, an optional single digit `-p` is added.

## Examples

`humanCSS c.0.8.1.171102 v.0.8.0`, `OutFocusRED c.2.9.3.170516-1`, `up c.0.1.0`.