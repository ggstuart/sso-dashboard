[**intro**](readme.md) | [**development options**](development-options.md) | **completed features**

* auto-gen TOC:
{:toc}

# Completed features
{:.no_toc}


## Shorter competitions

These changes support the above option, enabling admins to optionally show and hide competitons from the public student view during testing and preparation, or when they are finished.

![competition manager before](images/competition-management-before.png)

Above: the competition manager *before* new features

![competition manager after](images/competition-management-after.png)

Above: the competition manager *showing the new controls*

- competitions can now be published/unpublished in the admin interface
- the main competition cannot be unpublished
- if an unpublished competition becomes main, it is automatically published
- unpublished competitons no longer appear on the public list of competitions
- the main competition icon 'tick' has been replaced by a white trophy icon

### Features pending

([see full details in "Development Options"](development-options.md#shorter-competitions-see-progress))

- Enable archiving of competitions (as well as publishing/unpublishing) and present archived competitions in a secondary list publicly viewable through an additional click.
- Competitions are (optionally) operated on a rolling basis, operating the leaderboard on recent savings (e.g. the latest 28 days) rather than total cumulative savings.

---

## Graphical display of data

Clicking/tapping a hall (that has valid data) in any competition now opens a screen where there's a "table" and "chart" option. The "chart" opens the graphical display, which show actual consumption in red, and the target for savings as a yellow line:

![graphical data display](images/graphical-data-display.png)

For the above hall, you can clearly see the finer resolution of the data in the red graph, and an apparent anomaly in late November.

For halls with a lower data resolution (e.g. weekly or monthly readings) the red graph will show in broader blocks:

![graphical data display, monthly](images/graphical-data-display-monthly.png)

Joanna commented:

> is there a way to rename the ‘target consumption’ as something else? As that is a bit misleading, as it is not a target per se – it is a baseline that we want students to beat. And if students are ‘underusing’ their energy (they are far off the target), it might make them increase it!

### Features pending

- A 'notification' system for stale data, first step: list latest available data for each dataset
- Data quality report triggered by anomalous readings

For original details of the requested feature see [Graphical display of data (priority)] (development-options.md#graphical-display-of-data-priority-see-progress).

---

## Integration with the campaign

Multiple features were suggested, as completed, each is covered below

### Wide-screen display

For each competition there is now a dedicated "full screen" link for showing the competition on large (e.g. plasma) screens. This addresses one of the points listed under this item:

> a wide-screen display with a thin leaderboard alongside a customisable area, possibly with scrolling, customisable messages 

![large screen iframe](images/large-screen-iframe.png)

Above: the iframe is unsuitable for wide screen sizes

![large screen page](images/large-screen-page.png)

Above: the "large screen" link is designed for wide screen sizes

![large screen link](images/iframe-and-full-screen-links.png)

- all competitions now have a dedicated "full screen" page (above)
- there is an automatic "maximum width" limit, in case displays exceed 2000 pixels wide
- the university logo and competition message is displayed alongside the competition
- on larger screens, hall images are no longer cropped into a "letterbox" view
- less cropped hall images mean the iFrame also looks better on wider screens

### Customisable energy-saving tips

> possibly with scrolling, customisable messages

Each university can now manage a series of encouraging energy-saving messages via "tips" in the admin screens. These are visible on the public competition page and the wide-screen display, but omitted from the iframe version as this is designed to show only the leaderboard itself.

![copmetition tips](images/tips.png)

Above: tips appear next to all competitions under the university logo

![large screen tips](images/tips-wide-screen.png)

Above: tips on the wide-screen display are in a larger font and cycle automatically

![tips admin](images/tips-admin.png)

Above: the new "tips" admin tab is highlighted here, above the university logo

![tips admin detail](images/tips-admin-detail.png)

Above: tips admin screen includes a brief "title" field for easier identification

- you can add, edit and delete any tip from the "tips" admin screen
- tip titles are for admins to help navigate the list of tips e.g. a tip with the admin title "Summer campaign 2018 tip 1" might have a public message encouraging students to "Stay cool - eat more ice-cream!"
- the "home" tab is gone—the university logo now opens the university home page
- the tips cycle through all available tips, and can be paused/played by the user
- tips on the wide-screen version play automatically and the controls are hidden

Feedback on tips:

> It looks really good and I love the tips currently on display. Personally, I like the bright colors. It seems easy to navigate to me.

### Automatically refresh the public screen

This is now happening behind the scenes—all league tables are now refreshed every hour. There aren't any per-uni admin options, although the interval can be adjusted globally by Ecovisum if necessary.

### Features yet to be prioritised

([see full details in "Integration with the campaign"](development-options.md#integration-with-the-campaign-priority-see-progress))

- A "podium" style widget showing only the top three
- A single competitor widget showing one hall in a competition
- Editable cross-links with SSO campaign websites and Facebook pages

---

## Aggregate data per university

![savings bubble](images/kittens-saving-bigscreen-jun2018.png)

![savings large screen](images/kittens-saving-jun2018.png)

Above: the savings "bubble" on wide-screen and normal sized displays

After [feedback on the earlier "CO2 badge" design ideas](co2.md) a savings badge now appears on every competition as soon as data has been calculated, fading in and out as previously shown.

There's an option per-competition to show or hide it in the admin screens:

![savings bubble admin off](images/kittens-saving-admin-off-jun2018.png)

![savings bubble admin on](images/kittens-saving-admin-on-jun2018.png)

Below: the savings "bubble" at mobile size

![savings mobile](images/kittens-saving-mob-jun2018.png)

For original details of the requested feature see [Aggregate data per university](development-options.md#aggregate-data-per-university-see-progress).

---

[top of page](#)
