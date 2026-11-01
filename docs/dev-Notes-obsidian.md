https://logicalmodel.net/meet/?=021e69c9440c&view=calendar
D:/Obsidian/Simon/SIG-Stakeholder-Database-cursor-meet-scheduler-ca2b/meet

The following editing notes are recorded under to the page/ pane where I made them. Where appropriate, notes should be interpreted as generic rules to be applied on other pages/panes with similar wording or function. I have not necessarily spelt prompts correctly, nor added formatting or upper and lower case in these notes but onscreen render should use good practice. That should all be applied in a manner consistent with good presentation. 
Text to speech randomly inserts wording in uppercase. I'm not correcting it because it's so arduous to turn it all back into lowercase in this note - ignore it

Some clickable buttons have a square box with rounded corners, and some clickable buttons have semi-circular ends. All clickable buttons should be formatted the same way.  Some clickable buttons are grey with black text and others are blue with white text. If that distinction is going to hold throughout the user interface, then it ought to be meaningful and consistently applied otherwise remove INCONSISTENCIES

When considering this list of amendments, inconsistencies, suggestions or ambiguities should be questioned and resolved before any code generation.
Code generation requires an explicit instruction to say, yes, proceed. 

## Landing page
- amend "Places can be online (URL), physical, or hybrid. Times are shown in your local timezone and UTC. to   "Meeting locations can be online (URL) or physical. Times are shown in to attendees in local timezone and UTC" 
- add "Your local time zone is .... TIME and TIME_UTC UTC" substitute current time for TIME
- amend "Create meeting generates a private link with a random code. **Save it.**
  Or click/tap **Find my meetings** below to search by Attendee's registered
  ID AND PIN (Requires you have joined and set a personal pin when you joining)."
  to "The **Create Meeting Button** generates a private link with a random URL. **Save it.** 
- Make "Find my meetings" box, Create Meeting button & meeting title entry field full width of container window on wide screens - it is already on my mobile

# Footer
- Operations guide should be Installation, Operations and Maintenance Guide in the footer, and its content should contain all three sections with operations first, maintenance second if there is any, and installation third. 
  

#### Arriving at landing page for a meeting that is being scheduled when you havnt identified. 
- "What to do neat" needs to say Claim an id or Add yourself with Attendees then Add availability via MyAvailability, select or add preferred Location(s), View agenda and Decisions needed
  There's also the situation where somebody may not be invited as an attendee but is being shown the meeting link in order to view the records. So meeting status would have moved to the last state. (A refinement ask: claim your ID on attendees before viewing Records. )
# Dashboard 'sticky' panel
move  meeting link above Overview etc buttons
 move Your time zone: **Europe/London** to landing page
 move Calendar hours in **Europe/London** to places where times are shown
 then on those places allow a "show times for attendee" selection - means saving tz on entry and edit and only current TZ before any one added
 the "Scheduling" status  looks like a button label So should be reformatted to make it clear that it is a status display Distinct from a clickable button. 
  - The best slot next to scheduling should say earliest everyone can make or Most people (n) can make. 
 The overview button text should be Split into two. Getting Started and Overview Getting started should progress through a tick for each option. And now we don't need any fancy logic to determine when to turn off the getting started display.  
 amend to Status: and make format distinct and have values "Enter Organiser details --> Enter Attendee Details --> Scheduled --> ReSceduled --> Past --> Summarised
  - Enter Organiser Details displays before any attendees are entered. Enter Attendee Details is displayed until the organiser selects a time.&location, Rescheduled is if the organiser updates the time or location. Past is if the current date is past the scheduled start time. SUMMARIZED IS IF THE CURRENT DATE IS PAST THE SCHEDULED START TIME AND THERE ARE Records on the Records Pane 
  -  location of attachments to be with agenda and actions required, decisions required. Both for setting and for display. That is to say, where agenda is set and displayed, attachments should be set and displayed. 
# "How To Use This" guide 
- Opens text between buttons and "Calendar hours in...." - it should be above the buttons so the show when its fully read
- add a collapse action button at the end of the text - its long on mobile so this will avoid having to scroll up
   - ## Attendee
   - Amend. "You can also propose a new location." to You can also propose new locations.
   - amend "Check the top status badge for the current agreed time and location." to "Current meeting status is shown on the top of every page."
   - Amend "The **Copy link** button at the top copies the meeting URL. Save it — the random code in the link is the only way back to this meeting unless you set a PIN. The _Find my meetings_ option on the home page lets you look up meetings by name and PIN." to "The **Copy link** button at the top copies the meeting URL. The _Find my meetings_ option on the home page lets you look up meetings by Attendee name AND PIN if meeting URL is forgotten - Registered name AND PIN is required"
   - # Organiser
   - amend "**Share the link** — press _Copy link_ at the top of the page and send it to your attendees. Anyone with the link can join." to "**Share the link** — press _Copy link_ at the top of the page and send it to your attendees. Anyone with the link can record availability and locations and agenda and attachments."
   - add (and renumber rest) 2.2 Optional Add other proposed attendees and optionally grant Organiser rights. Anyone with the link who you don't pre-add can add themselves. Any identity without a PIN can be claimed by anyone. 
   - TO clarify before code amendments - the text "Calendar hours in **Europe/London** · Your timezone: **Europe/London**" seems wrong. Isnt it "Calendar slots are set initially as TIME using  this TZ but always displayed in local time.
# on pane Getting Started
- amend "**Set meeting options** — set the title, meeting length, calendar hours, and time zone" to "**Set meeting options** — Edit the title and Description, meeting length, Time Slot length, Allow Weekends and Reoccurrence"
- 
 
 
### Add new attendee sub block of Attendees pane 

You are signed in as **simon@logicalmodel.net (S)**. Use this form to add **someone else**.
change to "Use this form to add attendees. Anyone may add proposed attendees. Someone MUST send them the meeting link for them to add there availability."
if emails are added check well formed and warn if not looking correct - don't block entry
Change pin badge to PIN-Set PIN: Not Set
Force pin to be at least 2 characters to 20 - allow alphanumeric - add tool tip "Alphanumeric 2 to 20 Characters. Protects your meeting, REQUIRED to find meeting if you don't have the link "

if slots is 0 add "use my availability to enter acceptable times , use Locations to add/ select meeting location - online or physical"
### Getting started pane
 
 **Meeting is currently in setup mode.** Follow these steps to make it ready for attendees.
1. **✓ Set meeting options** — set the title, meeting length, calendar hours, and timezone.  
2. **✓ Add yourself as an attendee** — you will become the default organiser.      
3. **Mark your availability** — open My availability and click the slots when you are free. Optionally propose a location on Locations.      
4. **Share the link** — Copy meeting link and send it to all attendees so they can open this meeting and enter availability.   
The checklist stays visible until all four steps are complete.

The set meeting options text was amended In these notes before this line,  it should be amended consistently here too. 

# Overview when not Getting Started
- When meeting status is any of the statuses of before the meeting's been held, then the  Agenda and Decisions Required section default to expanded and Records default to contracted. when the meeting status is after the meeting date, records default to expanded. 
- Make the prompt "Attendees(n)" to "Attendees registered(n) Availability entered(n)". 
- amend "Best overlap times" to "Start Times With Best Attendance". When expanded, Use the same colour coding as is used on Set confirmed meeting details - All attendees for the full meeting, Selected time slot. Add a note to say, Colour key See Confirmed Meeting Details 
# Meeting Options Pane
Change the heading "grid step minutes" to "calendar slot duration (Minutes)
Move the description for attendees section Between title and meeting length. 
Move the calendar hours time zone section before earliest start time and have it collapsed by default. 
Amend the calendar hours time zone text from "each person also sees times in their local time zone" to These times will be displayed for each person's in their local time zone and UTC
Remove "availability is stored in UTC. " It's a design detail that the user does not need to be aware of. But it should be in the operations manual. "

# My Availability pane
The opening text, change, "press save my ability. When done", to "save your availability at any time, clicking/ Tapping a Previously selected slot deselects it - Don't forget to save again. 
There are no tool tips on a mobile. So the one-off no occurrences tool tip on a mobile doesn't show, but it could have a note next to it that says, "Use meeting options to change." 

In a previous revision, we did away with a meeting start date and said they can run from today. But if as a meeting organiser I want my meeting to be anywhere in a range, say a month hence, I need as the meeting organiser to say earliest and latest possible date and time. So the meeting options where we have not before, not after, ought to accept a date as well as a time. And the time is then taken as the beginning of availability slots for every day, and the end of availability slots for every day, and the date is taken as the availability first date and the availability last date. If we default the meeting start date to 8am on the day that the meeting is being set up, and we default the last time as 18:00 without a date, that would allow calendar to run for as long as anybody wanted it to. And allow 8am and 1800 to be overwritten with 0:00 and 24:00-meet to allow the whole calendar, the whole day to be booked. 

# Records & notes and Agenda
- Merge the functionality on records and notes and agenda to be two panes within the same windowed display, with notes and agenda first, and attachments second, and records third as sections. Update navigation buttons and navigational text to be consistent with the merging. 
- Amend "After the meeting: recordings, transcripts, attachments, and summaries. Pre-meeting agenda and notes are on **Notes & agenda**." to "Attach meeting: recordings, transcripts, attachments, and summaries. Meeting agenda and notes are on added/Viewed via **Notes & agenda**."
- Make the URL / Text summary radio buttons, and only show the HTTPS entry window or the summary text window entry boxes dependent on the selected radio button. 
- Since full web address has to start HTTP, I actually put it in as a prototype initial entry. 
- When there are no records, transcripts or summaries, give a dummy entry that says no attachments yet. 
- Change the composite pane name to Agenda, Attachments and Records 
- amend "Agenda items, decisions needed before the meeting, and preparatory notes. After the meeting, use **Records** for transcripts and attachments. to "Agenda items and preparatory notes, Decisions needed at the meeting. Add  transcripts and Summaries below."

# Set Confirmed Meeting Details pane 
- I can click on things because I have the link, even if I'm not logged in as a recognised user - That may be the symptom for why I didn't see the meeting status change. 
- Change "Viewed by anyone that's set changed by Organizer" to "Selecting a confirmed meeting time requires Organizer status". 
- Delete current status From this pane because it's shown on the sticky dashboard. 
- amend "Below is a visual analysis of full and partial availability. Mark your own slots on **My availability**, then choose a start slot here." to "Meeting slots show initials of attendees Who have marked availability with my availability . "
- Change the colour scheme so that all attendees and full duration is green. All attendees for part of the duration is the current colour for all attendees for all of the meeting.   
- The logic and labels should be Light green: all attendees full duration, second, all attendees for part duration - I think the label on this button is misleading. The third button should be some attendees available.  Dark green border and a different button shape should be Currently. Selected Meeting start. 
- **Proposed start:** Should read: Currently Selected, Meeting Start. 
- As well as empty time slots being suppressed, empty days should be suppressed, and the "show all hours" should show all days. 
- Where a display bridges a weekend that is not displayed, or bridges days that are not displayed, then a solid black line should split the day before and the day after that it's displayed. The same on MyAvailability: a solid black line between weeks when the weekend is not displayed. The black line should start between the date labels. 
- On the set confirmed meeting details, clicking a slot selects it. On that page, it is  then displayed as the proposed meeting time. But when then viewing the overview or looking at the sticky header, there is no change. It still says scheduling and best slot is another time. It's currently possible to select the meeting start as a day time slot when nobody is available - any selection without all attendees should ask Are You Sure Initials, Initials,.. unavailable
- I can't see a way to clear proposed meeting time. You can't unselect a slot by clicking it again.

And if that becomes the meeting status change to schedule, I can't see how you get from scheduling to scheduled. 
- ### Proposed Locations
  - Change proposed locations to Currently selected location. Then display Either "none. Selected yet. Choose a location below." or the Currently selection As the first component of this subsection of the pain. 
  - amend "Organisers can click a location to set it as the confirmed location candidate. Attendees can see who marked each location as workable." to "Select a location to set it as the Currently confirmed location." Then list the locations proposed with the initials of those who have marked locations as acceptable. Use the same colour coding as set confirmed meetings as far as possible Everybody OK, not everybody OK. Mark the selected either with an outline or an underline in the colour as explained against set confirmed meeting details. 
  - Add a note to say locations can be set and voted for with the locations button. 
    If we've duplicated so much of the logic on the locations form in the set confirmed meeting details, then propose a merger of the functionality. 
