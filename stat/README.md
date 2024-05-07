# Interesting statistics and observations

I'm finally done archiving all the charts from the chart repositories in the ArcCreate Discord.

Meanwhile, I've bodged up a convenient tool to read the metadata of the .arcpkg files fast, without having to read through the discord documents, and dump all the data from that in a sqlite .db file.

It's unfeasible for me to go through all the charts in the server (All 1936 of them, as of 07/05/2024), and type out the data manually, so there are obviously empty fields where the charters failed to include it in the .arcpkg files.

## Chart Constant

Using the data we have, here are the top 10 chart constants.

![Chart of frequency against CC](./resources/Count%20vs%20CC.png)

Note that I did not include a way to infer the actual chart constant from the displayed chart constant. The 9.7 count is not a result of considering all 9+s without an explicit chart constant as 9.7.

Honestly, this wasn't very surprising.

The actual surprising part comes when you include the null values. I've used -1 to substitute for a null value.

![Chart of frequency against CC, including nulls](./resources/Count%20vs%20CC%20w.-1s.png)

I don't know why there's so many. 

Maybe I've not mapped enough.

Regardless, if anyone any free time, I need volunteers (Not particularly urgently) to help fill in the chart constants.

More interesting chart constants:

| Chart Constant | Frequency | Comments |
| --- | --- | --- |
| 0.0 | 2 ||
| 6.9 | 1 ||
| 42.00 | 1 ||
| 69.0 | 2 ||
| 69.42 | 1 ||
| 72.7 | 1 ||
| 77.7 | 1 ||
| 909.0 | 1 ||

Of course there's a handful of 69s and 42s.

## Composers

Composers are much more evenly spread compared to chart constants.

The issue now comes from the aliases that each artist has. I don't have the time to research every artist listed, and make a regex for every single one of them.

I manually wrote the regexes for a handful of artists that I like, or were in the top 11.

Why 11? Because Camellia was in the top 10 twice.

![Chart of frequency against composer](./resources/Count%20vs%20Composer.png)

Anyways, if you have any artists you want to see if I ever write another document on this topic, write the regex when you send it to me.

More interesting composer statistics:

| Composer | Frequency | Comments |
| --- | --- | --- |
| nayuta | 11 | Queried because I suddenly remembered staringsky loved nayuta. |
| Sasakure.UK | 15 | |
| N/A | 9 | How? |

If anyone has any free time, I need volunteers (Not particularly urgently) to help create a table of composer aliases so I can easily query each artist.

## Charters

Here are the brave souls who have sacrificed their youths for this community, or however it goes.

I don't know enough to write out the aliases that each charters use, so I just took the top 11 results at face value.

![Chart of frequency against charter](./resources/Count%20vs%20Charter.png)

Arcthesia is the default anonymous name for contest submissions, from what I gather, but I've included it for completeness. That's why I selected the top 11 charters.

Thank you for your service, if you're reading this.

## BPM

Unexpectedly or otherwise, it seems that the BPM actually approaches a round number.

![Chart of frequency against BPM](./resources/Count%20vs%20BPM.png)

Honestly, nothing surprising here. So, to keep the average viewer (Who may not enjoy staring at some vertical lines) interested, I'll plot every single BPM, sorted, to showcase the perfect normal distribution.

![Chart of frequency against sorted BPMs](./resources/Count%20vs%20sorted%20BPM.png)

Well, nevermind. That's not very normal of you, distribution.

## Difficulty

I suppose this is to be expected, too, but honestly, I expected a more even split between Future and Beyond.

![Chart of frequency against difficulty](./resources/Count%20vs%20Difficulty.png)

## Side

I don't know what you'd expect, but it's exactly as you'd expect.

![Chart of frequency against side](./resources/Count%20vs%20Side.png)

Amusingly or otherwise, 19 people went into the .arcpkg and manually changed the side to something other than the 3 mentioned.

## Packs

There are 193 difficulties in 21 unique packs.
