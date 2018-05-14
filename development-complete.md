[**intro**](readme.md) | [**development options**](development-options.md) | **completed features**

* auto-gen TOC:
{:toc}
{:toc_levels: 2..3}

# Completed features

## Shorter competitions

These changes support the above option, enabling admins to optionally show and hide competitons from the public student view during testing and preparation, or when they are finished.

![competition manager before](images/competition-management-before.png)

Above: the competition manager *before* new features

![competition manager after](images/competition-management-after.png)

Above: the competition manager *showing the new controls*

### Summary of changes

- competitions can now be published/unpublished in the admin interface
- the main competition cannot be unpublished
- if an unpublished competition becomes main, it is automatically published
- unpublished competitons no longer appear on the public list of competitions
- the main competition icon 'tick' has been replaced by a white trophy icon

### Features pending

([see full details in "Development Options"](development-options.md#shorter-competitions))

- Enable archiving of competitions (as well as publishing/unpublishing) and present archived competitions in a secondary list publicly viewable through an additional click.
- Competitions are (optionally) operated on a rolling basis, operating the leaderboard on recent savings (e.g. the latest 28 days) rather than total cumulative savings.

---

## Integration with the campaign

For each competition there is now a dedicated "full screen" link for showing the competition on large (e.g. plasma) screens. This addresses one of the points listed under this item:

> a wide-screen display with a thin leaderboard alongside a customisable area, possibly with scrolling, customisable messages 

![large screen iframe](images/large-screen-iframe.png)

Above: the iframe is unsuitable for wide screen sizes

![large screen page](images/large-screen-page.png)

Above: the "large screen" link is designed for wide screen sizes

### Summary of changes

![large screen link](images/iframe-and-full-screen-links.png)

- all competitions now have a dedicated "full screen" page (above)
- there is an automatic "maximum width" limit, in case displays exceed 2000 pixels wide
- the university logo and competition message is displayed alongside the competition
- on larger screens, hall images are no longer cropped into a "letterbox" view
- less cropped hall images mean the iFrame also looks better on wider screens

### Features pending

([see full details in "Integration with the campaign"](development-options.md#integration-with-the-campaign))

- possible scrolling, customisable messages
- other leaderboard display suggestions yet to be prioritised

---

[top of page](#)
