# Quick Start

This "hacked" version of `Github Profile Trophy` (ryo-ma) allows you to show all secret trophies.

In this file, some modifications and improvements are added!

About usage, you can check [How to use](/USAGE.md).

## Self Deploy

You'll have to deploy yourself, for [Vercel](/VercelDeployGuide.md)) or [local](/LocalDeployGuide.md)

If you want to configure which trophies you automatically get, configure these booleans in [src/card.ts at line 13](/src/trophy.ts#L13)

```ts
let wantAllSuperRank = true;
let wantMultipleLang = true;
let wantLongTimeAccount = true;
let wantAncientAccount = false;
let wantNewAccount = false;
let wantMultipleOrganizations = true;
```

## Current Rank System

Secret Trophies

| Name of trophy | want = true | default |
| --- | --- | --- |
| MultipleLangTrophy | 5 | 10 |
| AllSuperRankTrophy | 0 | 1 |
| NewAccountTrophy | 0 | 1 |
| AncientAccountTrophy | 0 | 1 |
| LongTimeAccountTrophy | 0 | 5 |
| MultipleOrganizationsTrophy | 1 | 3 |

Base Trophies

| Name of trophy | C | B | A | AA | AAA | S | SS | SSS |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| TotalStarTrophy | 1 | 10 | 20 | 50 | 100 | 200 | 500 | 1000 |
| TotalCommitTrophy | 1 | 10 | 100 | 200 | 500 | 700 | 1000 | 2000 |
| TotalFollowerTrophy | 1 | 10 | 20 | 50 | 100 | 200 | 500 | 1000 |
| TotalIssueTrophy | 1 | 5 | 10 | 20 | 50 | 100 | 200 | 500 |
| TotalPullRequestTrophy | 1 | 5 | 10 | 20 | 50 | 100 | 200 | 500 |
| TotalRepositoryTrophy | 1 | 10 | 20 | 30 | 40 | 50 | 70 | 100 |

## Change logs

- renewing trophy "NewUserTrophy" instead of "Joined2020Trophy"
- condition of "newUserTrophy" from `==2020` to `>=2020`
- unit system of "LongTimeAccountTrophy" from `pt` to `year(s)`
- condition of "LongTimeAccountTrophy" from `10years` to `5years`
- show all trophies including secrets (conditions remain the same)
- Open the "wantAllSuperRank" and "wantMultipleLang" trophies by default (conditions is 0)
- conditions of "MultipleOrganizations" from `3` to `1` (open by default)
- change the distance between conditions and reduce the difficulty of "TotalStarTrophy"
  - A Rank from `30` to `20`
  - SS Rank from `700` to `500`
  - SSS Rank from `2000` to `1000`
- change the distance between conditions and reduce the difficulty of "TotalCommitTrophy"
  - S Rank from `1000` to `700`
  - SS Rank from `2000` to `1000`
  - SSS Rank from `4000` to `2000`
- change condition of "TotalFollowerTrophy"
  - SS Rank from `400` to `500`
- change the distance between conditions and reduce the difficulty of "TotalIssueTrophy"
  - B Rank from `10` to `5`
  - A Rank from `20` to `10`
  - AA Rank from `50` to `20`
  - AAA Rank from `100` to `50`
  - S Rank from `200` to `100`
  - SS Rank from `500` to `200`
  - SSS Rank from `1000` to `500`
- change the distance between conditions and reduce the difficulty of "TotalPullRequestTrophy"
  - B Rank from `10` to `5`
  - A Rank from `20` to `10`
  - AA Rank from `50` to `20`
  - AAA Rank from `100` to `50`
  - S Rank from `200` to `100`
  - SS Rank from `500` to `200`
  - SSS Rank from `1000` to `500`
- change the distance between conditions and reduce the difficulty of "TotalRepositoryTrophy"
  - AAA Rank from `50` to `40`
  - S Rank from `80` to `50`
  - SS Rank from `90` to `70`

If you choose to use my deployment, it would be really appreciated if you gave me a star 🙃.
