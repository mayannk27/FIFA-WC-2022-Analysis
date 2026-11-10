# Data dictionary

This is a high-level guide based on the columns used by the original notebook. The CSVs contain additional fields.

## `matches.csv`

| Column | Meaning |
|---|---|
| `date` | Match date |
| `home_team`, `away_team` | Competing national teams |
| `home_score`, `away_score` | Goals scored |
| `tournament` | Competition name |
| `city`, `country` | Match location |
| `neutral` | Whether the match was played at a neutral venue |

## Player files

The notebook selects these fields from each player dataset:

| Column | Meaning |
|---|---|
| `short_name` | Player display name |
| `overall` | Overall player rating |
| `age` | Player age |
| `club_name` | Player's club |
| `nationality_name` | Player's nationality |
| `mentality_aggression` | Aggression attribute |
| `mentality_interceptions` | Interceptions attribute |
| `mentality_positioning` | Positioning attribute |
| `mentality_vision` | Vision attribute |
| `mentality_penalties` | Penalties attribute |

The notebook ranks players by overall rating, selects up to 23 per nationality, and aggregates selected attributes by nationality and year.

## `country_rating.csv`

| Column | Meaning |
|---|---|
| `country` | National team |
| `year` | Rating year |
| `att` | Attack rating |
| `mid` | Midfield rating |
| `def` | Defence rating |
| `ovr` | Overall team rating |

## Derived target

The notebook derives a result label from `home_score - away_score`: home win, away win, or draw. Inspect the notebook's later preprocessing cells for the exact encoding and filtering used in the training data.
