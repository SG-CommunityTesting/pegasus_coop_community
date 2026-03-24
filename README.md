This catalogue syncs to FGS development environment.

The data flow is like this:

pegasus_core (base game files) > pegasus_1v1_community > Pegasus_coop_community > Map overrides.

So any updates to pegasus_1v1_community will be inherited here, and be overidden by the same JSONs in pegasus_coop_community or the map data.

There are some older data overrides still present in this catalogue. Things that may override newer data for units or heroes. We can delete or change these safely as long as it tests well.

Faction data for co-op heroes was originally setup like this:

Vanguardbarclay > Faction Enum 1001. All the progression perks are present here.
3v3 heroes use: Vanguardbarclay2 > faction Enum 101. No progression perks on these.

Each hero has a '2' faction variant that is more polished and up to date. We'd like to work towards migrating all hero data to the v2 variants and get 3v3 + coop heroes to use the same data.
TO do this, it will probably make sense to do all hero work in pegasus_1v1_community.
