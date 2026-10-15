# ITAM landing page — audit log

Rule for mobile: each section should say one thing within about one phone screen (375×812). Anything longer becomes a swipe row.

## Round 1 — baseline: 16.2 screens on a phone

| # | Area | Problem found | Fix |
|---|------|---------------|-----|
| 1 | Page | 16.2 screens long on a phone | Make each section fit about one screen |
| 2 | Hero | Headline fades in too slowly; looks blank in the first frame | Faster entrance that starts mostly visible |
| 3 | Hero | Pill wraps to two lines on phones | Shorter pill text on phones |
| 4 | Demo | 7 rows make the hero 2.4 screens | Show 4 rows on phones, with a "Show all" button |
| 5 | Demo | KPI tiles take a 2×2 block | Single compact row of 4 |
| 6 | Demo | Country chips cut off with no hint | Fade on the right edge |
| 7 | Problems | 6 stacked cards = 3 screens | Swipe row with dots |
| 8 | Services | Picker = 2 screens | Hide descriptions until switched on; hide the diagram on phones |
| 9 | Lifecycle | Vertical story = 4.5 screens | Swipe row of 5 cards, progress bar follows the swipe |
| 10 | Coverage | 1.4 screens | Swipe row |
| 11 | More services | 4 stacked cards | Compact 2×2 grid |
| 12 | Section heads | Long intro text on phones | Shorter spacing, intro limited to ~2 lines |
| 13 | Section padding | 72px top and bottom on phones | 52px |
| 14 | CTA | Book button out of reach after the hero | Sticky bottom "Book a demo" bar on phones |
| 15 | Swipe rows | No sign there is more to swipe | Peek of the next card plus dots |
| 16 | Toast | Would sit under the sticky bar | Raise it above the bar |
| 17 | Rows | Text and tag squeezed on narrow screens (your screenshot) | Rows wrap; tag moves to its own line |
| 18 | Nav | Full site menu on a campaign page | Logo + Book a demo only |
| 19 | Booking | Old popup is a plain 5-field form | 2-step popup: needs → contact; spring animation; validation; success state |
| 20 | Comparison | No answer to "why you over X?" | Comparison table; on phones, compare one competitor at a time |

**Result:** 16.2 → 10.3 screens on a phone, with the comparison section added. No horizontal overflow. No script errors.

## Round 2: interaction polish

| # | Area | Problem found | Fix |
|---|------|---------------|-----|
| 1 | Demo sheet (phone) | No backdrop; the page behind stays live | Dimmed backdrop; tap it to close |
| 2 | Demo sheet | No sign it can be dismissed | Drag handle + swipe down to close |
| 3 | Toast | Covers the return steps inside the sheet | Toast moves to the top while the sheet is open |
| 4 | "Try it" label | Bold word and sentence wrap as two columns | Single inline sentence |
| 5 | Hero (desktop) | Demo starts below the fold | Less top padding, headline max 72px |
| 6 | Comparison | ZenAdmin column doesn't stand out enough | Shadow on the table, row hover |
| 7 | Comparison (phone) | 5 columns can't fit | Segmented switch, ZenAdmin vs one option |
| 8 | Booking | Asks again for things the visitor already picked | Pre-ticks needs from the services picker |
| 9 | Booking | Enter key doesn't advance step 1 | Enter continues when ready |
| 10 | Booking | Chip selection feels flat | Spring pop on select |
| 11 | Services picker | Diagram change is easy to miss | Node pops when switched on |
| 12 | Demo KPIs | Numbers change silently | Number bumps when it changes |
| 13 | Demo rows | Status change is easy to miss | Row flashes on each step |
| 14 | Demo rows | No keyboard focus ring | Visible focus outline |
| 15 | Sticky CTA | Covers the sheet | Hidden while the sheet is open |
| 16 | Problems swipe | Cards could differ in height | Stretch to equal height |
| 17 | Closing CTA | No reassurance near the button | "Works with laptops you already own · No commitment" |
| 18 | Demo copy | Status messages long on phones | Shorter messages |
| 19 | Hero (phone) | Extra top padding | 44px |
| 20 | Eyebrow | "30-minute call" lacks the free signal | "30-minute call · free" |

## Round 3: one screen per idea, more paths to book

| # | Area | Problem found | Fix |
|---|------|---------------|-----|
| 1 | Lifecycle (phone) | Each step card taller than a screen | Show only the main window in each card |
| 2 | Lifecycle copy | Says "Scroll" where phones swipe | "Swipe" on phones, "Scroll" on desktop |
| 3 | Comparison switch | Labels wrap to 2 lines | Shorter labels: Spreadsheets / HR add-on / Shipping only |
| 4 | Comparison | Ends at a decision point with no action | "Compare my setup" CTA under the table |
| 5 | Pricing card | No action after the pricing promise | "Get a quote →" opens the booking popup |
| 6 | Header (phone) | Two "Book a demo" buttons visible at once | Header button fades while the bottom bar shows |
| 7 | Swipe rows | Easy to miss that they swipe | One-time nudge when first seen |
| 8 | Lifecycle row | Same discoverability issue | Same nudge |
| 9 | Integrations (phone) | Wall of 14 chips | Single swipe row with fade |
| 10 | Country chips | Tap targets under 40px tall | Taller chips |
| 11 | Lifecycle cards | Uneven heights while swiping | Stretch to equal height |
| 12 | Lifecycle text | Body copy long on phones | Slightly smaller size |
| 13 | Scene padding (phone) | Wasted space inside cards | Tighter padding |
| 14 | Comparison CTA (phone) | Button squeezed beside text | Stacked, full width |
| 15 | Bottom bar | Covers the closing CTA | Hidden once the closing CTA is on screen |
| 16 | Demo sheet | Bottom bar appears over it | Hidden while the sheet is open |
| 17 | Entrance animation | Page could look faded in the first frame | Movement only; text is always fully visible |
| 18 | Booking popup | Needs a quick way in from mid-page | All "#demo" links open the popup |
| 19 | Comparison claims | Competitors named with claims we can't verify | Compare by type of solution, not brand |
| 20 | Script | Needs a check after each round | Inline script syntax-checked after each patch |

**Result:** 10.4 screens; every section ≤1.4 screens except the hero (1.8, because it holds the live demo). No overflow. Tap targets ≥32px.

## Round 4: booking flow and final trims

| # | Area | Problem found | Fix |
|---|------|---------------|-----|
| 1 | Booking success | "You're booked in" promises a meeting that doesn't exist yet | "Thanks, Jane. Request sent." + when we'll reply |
| 2 | Booking | Size chips wrap to 2 rows on phones | 4-column grid |
| 3 | Booking | Empty name/company shows only a red border | "Fill in the highlighted fields." + aria-invalid |
| 4 | Booking | Country code typed by hand | Pre-filled from the browser's region |
| 5 | Booking sheet | Can't swipe it away on phones | Drag handle + swipe down to close |
| 6 | Hero (phone) | Intro is 5 lines | Cut to 3 short sentences |
| 7 | Pricing link | 19px tap target | Padded to a usable size |
| 8 | Comparison legend | Wraps awkwardly on phones | Smaller, tighter |
| 9 | Booking | Personal emails slip through | Gmail/Outlook/Yahoo/iCloud flagged with a clear message |
| 10 | Booking | Focus escapes the popup with Tab | Focus trapped inside; Esc closes and returns focus |
| 11 | Booking | Height jumps between steps | Height animates between steps |
| 12 | Booking | Step change feels abrupt | Slide in from the right, back slides from the left |
| 13 | Booking | Progress unclear | Progress bar 50% → 100% |
| 14 | Booking | Already-known needs asked again | Pre-ticked from the services picker (from round 2, verified) |
| 15 | Demo | Return flow untested on phone | Tested: tap → sheet → start return → steps → assign |
| 16 | Comparison | Untested on phone | Tested: switch shows ZenAdmin vs one option, fits one screen |
| 17 | Overflow | Your screenshot: text squeezed beside tags | Rows wrap; verified no element wider than the screen |
| 18 | Nav | Menu removed | Verified: logo + Book a demo only |
| 19 | Sticky CTA | Duplicate CTAs | Verified: header button fades when the bar shows |
| 20 | Motion | Reduced-motion users | All animation off under prefers-reduced-motion |

## Still to confirm with ZenAdmin before launch
- Per-device pricing with no ticket caps, and what retrieval, wipe and storage cost
- Certified wipe standard (the demo says NIST 800-88)
- Countries covered for pickup and storage (the demo lists 12, including BR, UY, IN)
- Leasing availability and the bring-your-own-device policy
- Named integrations (Workday, Rippling, HiBob, Intune, Jamf, Kandji, Snipe-IT, NetSuite)
- The six problem quotes are paraphrased from client calls: get approval or keep them anonymous
- Wire the booking popup to the real form endpoint (it currently only shows the success state)

---

# Second pass: mobile-first rebuild and conversion (after your phone screenshots)

Checked at 390×844 and 1280×860.

## Round A1: things that looked broken on phones
1. The demo wrapper shared the `.app` class with the lifecycle app tiles, so it inherited a white card, a border and centered layout. That was the junky box. Renamed it `.demo-app`.
2. Removed the fake browser bar and "app.zenadmin.ai" URL. It now reads "Interactive demo · sample fleet", so nobody thinks they're leaving the page.
3. Added a Reset button so visitors can replay the demo.
4. The demo list now has a fixed height (272px on phones, 300px on desktop). Before, it jumped from 450px to 96px when you picked a country.
5. Added an end-of-list note ("That's every device in BR") so a short list looks intentional.
6. Removed the 4-row cap and "Show more" button. The list scrolls inside its box instead.
7. Flags are drawn as SVG (15 countries), because Windows doesn't show emoji flags.
8. Flags added to the country filter chips.
9. Flags added to every device row and to the lifecycle windows.
10. Flags added to the coverage tiles.
11. Hid the demo search box on phones to save height. The country chips do the filtering.
12. Lifecycle on phones changed from nested swipe cards to tap-to-open steps, one open at a time.
13. Added a "Next: …" link inside each open step. The last step links to booking.
14. Removed the nested card-inside-card shadow from the lifecycle windows on phones.
15. Lifecycle cards no longer misalign. Older tablet rules were overriding them, so the phone rules now use the section's id.
16. On phones the comparison stacks one card per need, with ZenAdmin and the chosen option side by side.
17. Added a sticky "ZenAdmin | Spreadsheets" header that follows the switch, instead of repeating labels in every cell.
18. Closing CTA reassurance lines turned into ✓ chips.
19. Bottom bar shortened to "Free 30-min demo" plus the button.
20. "Try the product" became "Try the demo".

## Round A2: copy and conversion (based on the research)
1. Hero headline is pain-led and direct: "Get every laptop back from leavers, in any country". No competitor leads with a pain.
2. Hero intro states what ZenAdmin does in 3 sentences and ends with "Use the laptops you already own."
3. Pill names the audience: "For IT & People teams".
4. Work-email field plus "Book a demo" in the hero. Short forms that ask for email first convert best.
5. The email carries into the booking popup, so it isn't asked twice.
6. A badly formatted email shakes the form instead of opening the popup.
7. "Free 30-min demo · No commitment" sits under the field.
8. Problems eyebrow changed to "Sound familiar?". Headline: "Where company laptops get lost today".
9. Added a pain stat: 71% of HR teams had a leaver who didn't return equipment; remote staff 17% more likely (Capterra).
10. Problems intro now says where the quotes came from.
11. Added a customer section with three quotes from ZenAdmin's own site. It swipes on phones.
12. Added an FAQ with 6 objections: buying is optional, countries, wipe, pricing, time to start, MDM and Snipe-IT.
13. New order: problem → how it works → services → compare → proof → coverage → integrations → more services → FAQ → book.
14. The services picker moved after "how it works", so people see the process before choosing.
15. Closing headline now states the outcome: "See where your laptops are, in 30 minutes".
16. The closing CTA also takes a work email.
17. FAQ answers open and close with a smooth chevron.
18. Customer quotes sized down for phones.
19. The pain stat stacks vertically on phones.
20. Every new form is labelled for screen readers.

## Round A3: polish
1. The hero pill wrapped to 4 lines on phones. It now shows only "For IT & People teams" there.
2. The email placeholder was centered. It's now left-aligned.
3. The note under the form is shorter on phones, without the line break.
4. The header "Book a demo" hides while the hero form is on screen, so there's one button at a time.
5. Coverage tiles flashed solid blue over the flags. They now get a soft ring.
6. Coverage tiles show the flag above the country code.
7. The first FAQ ("Do we have to buy laptops?") is open by default, because it's the biggest objection.
8. When an email comes from the hero, the popup intro reads "Booking for jane@company.com".
9. Added a meta description for link previews and search.
10. Fixed a broken apostrophe in the script.
11. Lifecycle: the open step's window now comes before the "Next" link.
12. Lifecycle: closed steps lost a phantom second row.
13. Every swipe row nudges once when first seen, except the lifecycle, which no longer swipes.
14. Checked the bottom bar never covers the open demo sheet.
15. Checked the sticky comparison header stays under the site header.
16. Checked the demo list height doesn't change across all 8 country filters.
17. Checked the Reset button restores Diego's laptop and the new-hire list.
18. Checked the booking popup on phones: pre-ticked needs, email carried over, success state.
19. Checked no element is wider than the screen at 390px.
20. Checked the inline script parses after every patch.

## Round A4: desktop check after the reorder
1. Section labels (e.g. "SOUND FAMILIAR?") sat right-aligned on desktop. Current Chrome now applies `justify-self:end` to ordinary blocks, so the rule now targets only the section intro paragraph.
2. Checked the comparison table on desktop with the new "Compare my setup" bar.
3. Checked the hero email form on desktop is one row and centered.
4. Checked the FAQ on desktop at max 820px wide.
5. Checked the pain stat band on desktop.
6. Lifecycle phone heights measured: 90px closed, 368px open. Desktop keeps the pinned screen.
7. Phone page length is 11.2 screens with three new sections (customers, FAQ, stat). No section is longer than 1.5 screens.

---

# Visual audit: spacing, hierarchy, brand (checked at 1280×860 and 390×844)

| # | Found | Fix |
|---|-------|-----|
| 1 | Hero headline wrapped to 3 lines on desktop | Line break after "asset,"; size 44–68px. Desktop is now 2 lines. Phones stay 3, because 2 would need unreadably small text |
| 2 | Three section headings wrapped to 3 lines | Shortened: "Every asset, from order to resale", "Delivery and pickup, anywhere", "Works with your HR, MDM and asset tools". All 10 headings are now 2 lines |
| 3 | FAQ heading 48px, every other section 50px | One size for all |
| 4 | Closing banner label grey 17px, every other label blue 13px | Matches the others |
| 5 | Five corner sizes in use (16/18/20/22/32) | Scale: controls 12, cards 20, demo window 24, banner 28 |
| 6 | "Next" buttons, problem tabs and nav fell back to Arial | Every button and input uses Instrument Sans (0 Arial elements left) |
| 7 | Country dropdown was a native select with codes | Custom animated dropdown: flag + full name, keyboard support, staggered options |
| 8 | Flags shown with codes (BR, DE…) next to them | Flags only; codes kept for screen readers |
| 9 | Phone tab-bar badges overlapped icons | Badges sit 2px off the icon's corner |
| 10 | Services picker redrew on every tap, so switches jumped | Updates in place: knob slides, "ZenAdmin does this / Your team does this" rolls, summary height eases |
| 11 | Spring animations overshot (chips, nodes, guide, period, popup, bottom bar) | Calm ease-out curve everywhere, no bounce |
| 12 | Phone side gutter | 20px everywhere; sections ≤1.6 screens; no horizontal scroll |
