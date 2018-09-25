[**intro**](readme.md) | **development options** | [**completed features**](development-complete.md)

<!-- 
  https://kramdown.gettalong.org/converter/html.html#toc
-->
<!--
  https://github.com/shd101wyy/markdown-preview-enhanced/blob/master/docs/toc.md
  Markdown Preview Enhanced: cmd-shift-p -> Markdown Preview Enhanced: Create Toc.
  To exclude a heading from the TOC, append {ignore=true} after your heading.
-->

* auto-gen TOC:
{:toc}

# ECOVISUM development options
{:.no_toc}

From February—September 2018 ECOVISUM is focussing on developing the dashboard interface as agreed at Dublin (and summarised on the whiteboard after the "world café" exercise). As well as adaptations to existing features, there are new features and possible significant new functionality. The balance between small improvements and large experimental/new features is under periodic review with input from the TAG.

The list below is open to feedback. Potential features should be 'bite-size' so we can pick two or three for development at any one time. Together, we will continuously prioritise features so the most valuable are implemented first. Some ideas may be shelved while others may be continually developed. This is the core feature of an agile approach.

The first baby-steps for each proposed direction are suggested as a basis for a broader discussion about options we want to push the furthest. If we "bite off more than we can chew", progress will stagnate, so our approach is to break down large features into several smaller ones. Although each feature may seem small alone, in the right combinations they support each other. We aim for slow but steady progress, always delivering the maximum possible value for our time.

[All feature progress is updated on this page](development-complete.md).

---


## Shorter competitions: [see progress](development-complete.md#shorter-competitions)

The implications of shorter competitions are mostly related to operational issues. However, there are aspects of the dashboard which would support shorter competitions.

Students are currently presented with a list of competitions on the university home page. e.g. Cyprus lists 13 competitions. Competitions from previous years appear alongside current ones and test competitions are also visible to students. There is no way to manage the order of competitions or to delete/hide/archive competitions.

A university's home page shows their current 'main' competition - the league table. There can only be one competition marked as 'main' at any one time.

Hall competitor savings/increases are calculated by dividing into individual days, each having a target and an actual consumption value. The competition presents the current total cumulative saving for each competitor.

### Potential solutions

1. ~~Students only see the main competition and cannot access older competitions.~~  
This solution removes the immediate problem in Cyprus (13 competitions listed) but does not add new functionality. **[CLOSED: will not be implemented]**

2. Students only see relevant competitions - older competitions are 'archived' by administrators.  
This introduces an element of more sophisticated competition management. Perhaps competitions can be published, archived or hidden? Students could view a list of archived competitions through an additional click. **[OPEN: mostly implemented]**

3. Competitions are (optionally) operated on a rolling basis.  
We provide an option in the competition editor to enable the leaderboard to operate on recent savings (e.g. the latest 28 days) by default rather than total cumulative savings. Total cumulative performance over the whole period is still available but only shown with an optional click. In this way students are always able to climb the leaderboard by making shorter term efforts and the overall winner is de-emphasised until the end of the competition period, when it will again become the default. **[OPEN: could be implemented]**

### Further issues and options

> Question: Will universities EVER need to run more than one competition simultaneously?

- If parallel competitions are allowed then students must be able to browse available competitions.  
- This makes it more difficult to set a 'main' competition.
- Students could select a 'default' competition of their choice to be remembered by their browser.



## Graphical display of data: [Priority, DONE](development-complete.md#graphical-display-of-data)

Students are presented with a potentially confusing technical data table when they click a league table entry. The data table requires a significant effort to interpret.

In addition to this there are areas in the administration system where raw data are presented which need to be reviewed. Good quality data are crucial to the correct operation of the dashboard.

### Potential solutions

- Displaying the same data in a graphical form would enable students to interpret their progress at a glance **DONE**
- An extra click could still open the (read-only for students) data table **DONE**
- A graphical display of raw data would help administrators to identify data issues more easily **DONE**
- Highlight data anomalies at-a-glance somewhere in the admin screens **DONE**
- A 'notification' system for stale data, first step: list latest available data for each dataset
- Data quality report triggered by anomalous readings



## Aggregate data per university: [see progress](development-complete.md#aggregate-data-per-university)

Displaying percentage savings hides the absolute contribution made by each hall. Large halls need to make larger savings to get the same percentage result.

Students cannot quantify the overall contribution of the competition. There is no summary view to quantify the value of the competition as a whole.

### Potential solutions

1. Show absolute kWh, CO2 and possibly financial (currency?) savings figures against each competitor.
This might be initially hidden but could be revealed on clicking the competitor. This requires a conversion factor for CO2 kg/kWh and for currency €/kWh or £/kWh, and additional configuration options at the competition level.

2. Show a summary figure (kWh/CO2/currency) for the whole competition by displaying a total impact figure somewhere in the leaderboard. Following feedback from the [two possible display options](co2.md) a [per-competition "savings" badge is now live](development-complete.md#aggregate-data-per-university).



## Review leaderboard display

The leaderboard has a few visual problems in various sizes. The numbers highlighting the top three obscure the images and are not clearly highlighted. The mobile size leaderboard has a large header which requires the user to scroll down before actually seeing the top three. It needs a complete review to refine the existing interface and to make room for new features such as the aggregate data.

### Potential solutions

1. redesign the top three to be more prominent, say as a 'podium' ([also see "Embeddable widgets" below](#potential-solution-embeddable-widgets))
2. reduce the size of competitors below the top three so more are immediately visible
3. move the position numbers away from the image, and show them on all competitors
4. highlight halls who have improved their savings (technical challenge)



## Integration with the campaign: Priority, [see progress](development-complete.md#integration-with-the-campaign)

This implies placing the dashboard in as many contexts as possible, sharing clickable and other visible links to a university's dashboard as widely as possible to maximise views. The implications for the dashboard are mostly regarding how it can be displayed and also integrated with social media.

<!--
Further items from Bucharest could be added here: "ability to personalise the rolling images" which I think refers to tips:

1. add URLs to SSO websites, requested for the tips, but might be better more prominently displayed per-uni, so G and I will talk this through and bring it up in the next TAG;
2. make the dashboard "more flashy and visual", this is too vague and needs pinning down, e.g. enable unis to add images of their campaign, although this is a significant feature so we'd need to ensure it doesn't compete with other priorities
-->

### Added at Bucharest and September TAG meeting

Add links to the rolling tips, so they can be clicked on to go to (say) more information on that tip from e.g. other SAVES websites. [DONE](development-complete.md#links-on-tips)

### Potential solutions 1: embeddable 'widgets'

The dashboard is built for any device with a web browser: phones, tablets, laptop and desktop-sized screens and larger public screens. However, the embeddable 'widgets' we have are currently pretty basic, so we could consider developing a suite of embeddable widgets, for example:

1. A wide–screen display with a thin leaderboard alongside a customisable area [DONE](development-complete.md#wide-screen-display)
2. Possibly with scrolling, customisable messages [DONE](development-complete.md#customisable-energy-saving-tips)
3. A "podium" style widget showing only the top three
4. A single competitor widget showing one hall in a competition
5. A summary of the aggregate data for one competition
6. Automatically refresh the public screen daily [DONE](development-complete.md#automatically-refresh-the-public-screen)
7. Add social media links to SSO campaign websites (per country) and Facebook pages (per competition)
8. Retain existing NUS SwitchOff social media links on the home page only

### Potential solutions 2: gamification of visits

We could also consider gamification of dashboard visits. For instance, a 'follow' button to record and present how many 'follows' a particular hall was getting. For example in a given competition, halls with a given number of 'follows' could be rewarded with a trophy or badge on the leaderboard. Admins could set multiple levels and award e.g. bronze, silver and gold trophies for 10, 20 and 50 'follows'. These could then be set as tasks for students to visit the site and rack up the 'follows' to earn the trophies.



## Review baseline calculations

The underlying calculations which are continuously happening on the dashboard server are fairly simple, being based on an average daily consumption value. While these calculations are appropriate in most cases, in a significant proportion of halls they require administrative users to 'adjust' the calculated baselines e.g. when halls are electrically heated, where changes have been made to energy systems or when the raw data are problematic.

### Potential solutions

1. **Review and update the calculation procedure** to make it apply more widely, for example by adding *degree day correction* into the calculation. This would be fairly difficult and needs work to elaborate into clear features.

2. **Make the baseline setting functionality more flexible and transparent**, giving more control to the administrator. The user interface for baseline calculations is currently fairly opaque and restrictive and could be improved. For example, when specifying a competitor baseline the user may be able to freely edit the daily targets which are suggested by the automated calculation.

3. **Improve management and editing of raw data**. Raw data are visible in the dashboard but when data are not perfect there is often a use-case for editing. The user interface is not so sophisticated and this whole aspect of the dashboard could be usefully overhauled. This links with graphical presentation of the data also.



## Personalise the dashboard

A personalised dashboard experience implies that we provide different information depending on the user and their preferences/behaviour. This can have a number of benefits, a personalised experience is more engaging, hall-specific calls to action will be more relevant to the user and rewarding users for their commitment can be reinforcing.

### Potential solutions

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

---

# Conclusions

Many new features could be added, so those described here are clearly defined and can be actioned immediately. Other ideas are less well-defined and need more thought to tease out the concrete features lurking beneath the surface.

ECOVISUM are only able to implement features once they are clearly defined and broken into small enough tasks to be realised in short time-frames. Larger features can be implemented only after being broken into collections of smaller features. This lends clarity to the process and helps locate the real value to users.

The process of generating and prioritising features is ongoing. ECOVISUM will do the hard work but the TAG needs to engage in this process alongside ECOVISUM to help steer us towards the best value. There are two main processes:

1. Every month we pick a small number of clearly-defined features for ECOVISUM to work on. We aim to add the chosen new functionality between TAG meetings. This is the 'sprint' schedule. The features to be implemented each month will be decided in the TAG meeting.

2. We also need to maintain a long-list of concrete, well-defined features to draw from in each 'sprint'. ECOVISUM will continuously work towards generating new concrete, actionable items for the list as long as there is enthusiasm for a feature or group of features. We must also identify which less well-defined features need focus, and how to break them into concrete features.

---

These web pages are generated from Markdown text files and maintained on the [SSO Dashboard GitHub page](https://ggstuart.github.io/sso-dashboard/)

---

[top of page](#)
