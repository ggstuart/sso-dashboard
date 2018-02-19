**[intro](readme.md) | development options | [completed features](development-complete.md)**

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

- Displaying the same data in a graphical form would enable students to interpret their progress at a glance
- an extra click could still open the (read-only for students) data table
- a graphical display of raw data would help administrators to identify data issues more easily


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

4. highlight halls who have improved their savings (technical challenge)


## Integration with the campaign

This implies placing the dashboard in as many contexts as possible, sharing clickable and other visible links to a university's dashboard as widely as possible to maximise views. The implications for the dashboard are mostly regarding how the dashboard can be displayed and how it integrates with social media.

### Embeddable 'widgets'
The dashboard is available on any device with a web browser: phones, tablets, laptops and desktop-sized screens. and above, such as public screens. However, the embeddable 'widgets' we have are currently pretty basic, so we could consider developing a suite of embeddable widgets, for example:

- a wide-screen display with a thin leaderboard alongside a customisable area, possibly with scrolling, customisable messages.
- A top-three "podium" style widget
- A single competitor widget showing one hall in a competition
- A summary of the aggregate data for one competition

### Gamification of visits

We could also consider gamification of dashboard visits. We could offer a 'follow' button and record and present how many 'follows' a particular hall was getting. For example in a given competition, halls with a given number of 'follows' could be rewarded with a trophy or badge on the leaderboard. Admins could set multiple levels and award e.g. bronze, silver and gold trophies for 10, 20 and 50 'follows'. These could then be set as tasks for students to visit the site and rack up the 'follows' to earn the trophies.


## Review baseline calculations

The underlying calculations which are continuously happening on the dashboard server are fairly simple, being based on an average daily consumption value. These calculations are appropriate in most cases but in a significant proportion of halls they require administrative users to 'adjust' the calculated baselines. This is needed when e.g. halls are electrically heated, where changes have been made to energy systems or when the raw data are problematic.

There are two areas where improvements could be made:

1. Review and update the calculation procedure to may make it apply more widely, for example by adding degree day correction into the calculation. This would be fairly difficult and needs work to elaborate into clear features.

2. The user interface for baseline calculations is currently fairly opaque and restrictive. We could think about how to make the baseline setting functionality more flexible and transparent, giving more control to the administrator. For example, when specifying a competitor baseline the user may be able to freely edit the daily targets which are suggested by the automated calculation.

3. Raw data are visible in the dashboard but there is limited functionality to manage and edit the raw data. When data are not perfect there is often a use-case for editing. Since the user interface is not so sophisticated, this whole aspect of the dashboard could be usefully overhauled. This links with graphical presentation of the data also.


## Personalise the dashboard

A personalised dashboard experience implies that we provide different information depending on the user and their preferences/behaviour. This can have a number of benefits, a personalised experience is more engaging, hall-specific calls to action will be more relevant to the user and rewarding users for their commitment can be reinforcing.

Providing such an experience can be done in two ways. We can either:

 - store preferences in the browser
 - require a formal login process on the server

The benefits of storing preferences in the browser are that the user need not create a username and password. Browser based storage can provide a significantly more personal experience than we currently have. For example:

 - Enabling students to 'favourite/follow' their university or hall
 - Loading their favourite/followed university/halls by default
 - Providing different advice/tips depending on their position in a competition
 - recording the number of visits and rewarding the student with hidden features
 - Providing a different experience for regular users

Without logins we can still collect anonymous data. This might include university and hall-level data. Requiring student login is an extra barrier but would give us the ability to collect individual data and validate student emails for example.


# Conclusions

There are many areas where we can add new features. Some of the features described above are very clearly defined and can be actioned immediately. Other ideas are less well-defined and need more thought to tease out the concrete features lurking beneath the surface.

ECOVISUM are only able to implement features when they are clearly developed and when they are small enough to be implemented in a short time-frame. That is not to say that larger features cannot be implemented, it means larger features need to be broken down into collections of smaller features. This lends clarity to the process and helps to reveal where the real value is to users.

The task ahead is to set up an ongoing process of generating and prioritising features. ECOVISUM will do the hard work but the TAG will need to engage in the process and help steer us towards the best value. There are two main processes:

1. Every month we need to pick a small number (about 2-4) of clearly-defined features which ECOVISUM will work on. We will aim to add the new functionality between TAG meetings. This is the 'sprint' schedule. Every month we will take on new features, the decision of which features we will implement will be made in the TAG meeting.

2. We also need to make sure we have a long-list of concrete, well-defined features from which to draw from in each 'sprint'. ECOVISUM will continuously work to generate new concrete, actionable items for the list as long as there is enthusiasm for an area of development. We need to identify which of the less well-defined features we should focus on and how we might convert them into concrete features.

We will maintain these lists on our github page [here](https://ggstuart.github.io/sso-dashboard/)