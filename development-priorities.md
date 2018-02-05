# ECOVISUM development options

For the next six months or so ECOVISUM will be focussing on developing the dashboard interface and adding new features. In many cases these will be tweaks to existing features, others will be small additional features. We may also embark on significant new functionality. The balance between small improvements and large, experimental new features is yet to be decided.

This report introduces some of the small to medium-sized initial development options to be prioritised for the next few months. This is an initial attempt to elaborate on options raised in the Dublin meeting and summarised on the whiteboard after the "world café" exercise. The intention is to suggest the first baby-steps in each proposed direction and start a broader discussion about which options we want to push the furthest.

The list of potential features will be dynamic. We are always open to new ideas and adapting old ones. Potential features should be 'bite-size' so we can pick two or three features to develop at any one time. Together we will continuously prioritise the list so that the most valuable features are implemented first. In this way, some ideas may never be implemented and others may be continually developed. This is the core feature of an agile approach.

It is crucial that we don't "bite off more than we can chew" as this can allow progress to stagnate. Any proposed large feature can usually be broken down into several smaller features, and this is the approach we have taken in this document. Each feature may seem small alone, but in the right combinations they support each other. We plan to make slow but steady progress, always delivering the maximum possible value for our time.

So, for each area of potential development we have defined some concrete features. These need to be prioritised and added to the sprint schedule as part of the agile process. In the TAG meeting we will discuss the list and possibly refine it. Our next sprint will begin after the TAG meeting and will include a few ideas from this document. In the following TAG meeting we should expect to present the new features in the working dashboard.

The following categories were highlighted in Dublin:


## Shorter competitions

The implications of shorter competitions are mostly related to operational issues. However, there are aspects of the dashboard which would support shorter competitions.

Students are currently presented with a list of competitions on the university home page. e.g. Cyprus lists 13 competitions. Competitions from previous years appear alongside current ones and test competitions are also visible to students. There is no way to manage the order of competitions or to delete/hide/archive competitions.

A university's home page shows their current 'main' competition - the league table. There can only be one competition marked as 'main' at any one time.

Hall competitor savings/increases are calculated by dividing into individual days, each having a target and an actual consumption value. The competition presents the current total cumulative saving for each competitor.

**Potential solutions**

1. Students only see the main competition and cannot access older competitions. 
This solution removes the immediate problem in Cyprus (13 competitions listed) but does not add new functionality.

2. Students only see relevant competitions - older competitions are 'archived' by administrators. 
This introduces an element of more sophisticated competition management. Perhaps competitions can be published, archived or hidden? Students could view a list of archived competitions through an additional click.

3. Competitions are (optionally) operated on a rolling basis.
We provide an option in the competition editor to enable the leaderboard to operate on recent savings (e.g. the latest 28 days) by default rather than total cumulative savings. Total cumulative performance over the whole period is still available but only shown with an optional click. In this way students are always able to climb the leaderboard by making shorter term efforts and the overall winner is de-emphasised until the end of the competition period, when it will again become the default.

> Question: Will universities EVER need to run more than one competition simultaneously?

If parallel competitions are allowed then students must be able to browse available competitions.  
This makes it more difficult to set a 'main' competition.  
Students could select a 'default' competition of their choice - this can be remembered by their browser.


## Graphical display of data

Students are presented with a potentially confusing technical data table when they click a league table entry. The data table requires a significant effort to interpret.

In addition to this there are areas in the administration system where raw data are presented which need to be reviewed. Good quality data are crucial to the correct operation of the dashboard.

**Potential solutions**

- Displaying the same data in a graphical form would enable students to interpret their progress at a glance.
- an extra click could still open the (read-only for students) data table

**The data table**

With a graphical display, there's an opportunity to separate this functionality.

- The data table still needs a more user-friendly means to review and edit the data.
- Data gaps should be easily identified and filled with a few clicks.
- Erroneous data should be easily purged or overwritten.
- A dedicated interface for managing raw data could also enable monthly data manually to be entered by hand.


## Aggregate data per university

Displaying percentage savings hides the absolute contribution made by each hall. Large halls need to make larger savings to get the same percentage result.

Students cannot quantify the overall contribution of the competition. There is no summary view to quantify the value of the competition as a whole.

**Potential solutions**

1. Show absolute kWh, CO2 and possibly financial (currency?) savings figures against each competitor. 
This might be initially hidden but could be revealed on clicking the competitor.

2. Show a summary figure (kWh/CO2/currency) for the whole competition. Somewhere in the leaderboard it should be possible to display a total impact figure.

Both these features require a conversion factor for CO2 kg/kWh and for currency €/kWh or £/kWh. These would be additional configuration options at the competition level.


## Review leaderboard display

The leaderboard has a few visual problems in various sizes. The numbers highlighting the top three obscure the images and are not clearly highlighted. The mobile size leaderboard has a large header which requires the user to scroll down before actually seeing the top three. It needs a complete review to refine the existing interface and to make room for new features such as the aggregate data.

**Potential solutions**

1. redesign the top three to be more prominent, say as a 'podium'

2. reduce the size of competitors below the top three so more are immediately visible

3. move the position numbers away from the image, and show them on all competitors


## Integration with the campaign

This implies placing the dashboard in as many contexts as possible, sharing clickable and other visible links to a university's dashboard as widely as possible to maximise views. The implications for the dashboard are mostly regarding how the dashboard can be displayed and how it integrates with social media.

The dashboard is available on any device with a web browser: phones, tablets, laptops and desktop-sized screens. and above, such as public screens. However, the embeddable 'widgets' we have are currently pretty basic, so we could consider developing a suite of embeddable widgets.

- a wide-screen display with a thin leaderboard alongside a customisable area, possibly with scrolling, customisable messages.
- A top-three "podium" style widget
- A single competitor widget showing one hall in a competition
- A summary of the aggregate data for one competition

**NOTES TO DISCUSS:**

DAVE: I'm not sure about thlike buttons for halls? How about showing up/down as we once had or highlighting improved halls?

We could also consider gamification of dashboard visits. We could offer a 'like' button and record and present how many 'likes' a particular hall was getting. For example in a given competition, halls with a given number of 'likes' could be rewarded with a trophy or badge on the leaderboard (abuse?). We could set multiple levels and award e.g. bronze, silver and gold trophies for 10, 20 and 50 'likes'. These could then be set as tasks for students to visit the site and rack up the 'likes' to earn the trophies.


## Review baseline calculations

The data administration side of the dashboard is extremely demanding and time-consuming. When data are not perfect and halls are electrically heated or cooled the calculations are challenging and need constant attention. Since the user interface is not so sophisticated, this whole aspect of the dashboard could be usefully overhauled.

There are several tweaks and small improvements which could be made to the interface as well as major new approaches to the way baselines are created and managed. This area is an open territory but has unseen benefits for students in terms of reliability and trust in the dashboard.

**NOTES TO DISCUSS:**

The system currently allows a few simple methods for calculating target consumption. Although simple to use they prevent the dashboard administrators from using their local knowledge to determine suitable target values.

- review the user interface for developing baseline targets to give the administrator more control e.g. setting a baseline would then show the calculated targets.

- 'Degree day adjustments' are listed on the summary sheet from Dublin, how do we answer that?

- Electrically-heated halls need a method for administrators to make changes specific to actual heating energy use via the dashboard rather than an external spreadsheet, to produce more realistic figures on the leaderboard.


## Personalise the dashboard

Providing a personalised dashboard experience for each user is not simple, although enabling students to 'favourite' their uni and hall to load on their device by default, with the hall's position in the current competition, might be a step forward.

**NOTES TO DISCUSS:**

- students receive a fresh message or prompt each day to encourage them to participate, based on: weather (relevant tip), uni location, a rolling list of energy-saving tips.

- calls to action can capture student attention and encourage behaviour change
- hall-specific calls to action may be more effective
- students can receive encouraging messages about their hall's performance
- a rolling pool of tips would make the leaderboard appear fresh

Requiring log in is an extra barrier. Either showing up on a visit to the dashboard, or as a notification pushed to students. Students could 'save'.

