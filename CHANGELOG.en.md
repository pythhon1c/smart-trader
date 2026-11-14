[English](CHANGELOG.en.md) · [Українська](CHANGELOG.uk.md) · [Русский](CHANGELOG.ru.md)

# Smart Trader changelog

The list follows the versions published on the [Chrome Web Store](https://chromewebstore.google.com/detail/smart-trader-trading-tool/cikfmbllbfiplfpllhbomapngmcedglo): each store version holds the notes of every version released since the previous store version, the newest first.

## 1.24.0 (Chrome Web Store, 2026-11-14)

### 1.24.0 (2026-11-13)

- Trade window: a backpack.tf link that puts the partner's item into the offer (for_item) or loads the partner's TF2 inventory for a buy listing now works on a new offer only; an offer already sent always shows exactly the items it holds.
- Trade window: a big offer whose items are not all loaded yet no longer slows the page down while prices are asked.
- On an item's market page, relisting your own listings no longer takes one listing's quantity for another (a listing of 5 relisted as 1); a listing whose item the page does not show is not relisted there and says to relist it from My listings.
- The relist of My listings reads your inventory page by page at the inventory's own pace and stops once the items it needs are found, so a big inventory no longer leaves listings off the market; Steam's "too many requests" now pauses it at once.
- Before it takes the first listing off, the relist checks that your inventory can be read; when Steam does not answer, nothing is taken off and the listings stay on the market for Retry.
- Telegram bot: a message whose partner or item name ends in a word such as "Secret" or "Token" before a colon is no longer dropped silently with the rest of its batch; the bot token, your API keys and values shaped like Steam tokens are still never sent.
- Texts corrected: the uk / ru notes of the cs2.sh prices, a fallback note in ru, the help of the sign-out warning, the age of a KEYS.LAND Telegram post (10 days) on the options page, and in the privacy policy the order of the factory Preset 1 and how long the cs2.sh list is kept (60 minutes).
- The header shows the pending part of your wallet balance on the same line as the balance.
- The "check at cs2.sh" button is hidden until cs2.sh supports inventory links; an item's "View in cs2.sh" links stay.

## 1.23.9 (Chrome Web Store, 2026-11-13)

### 1.23.9 (2026-11-13)

- The License Agreement has a new version, 2026-11-13: section 3 now says plainly what may not be done with Smart Trader (copying or changing it to use it elsewhere, publishing or sharing it, taking its code, texts or pictures into other products, removing its notices) and that it holds no code of other authors any more; section 8 also names what our price server hands over and your own Telegram bot. Smart Trader asks you once to accept it again.
- Extension: the data notice is shown again once, with the agreement (version 19): it now names the copy of My listings and the listings total for Steam's wallet limit kept on your computer, and the privacy policy (effective 2026-11-13) also says that "Load all" next to the inventory's sort can go through steamapis.com. Your choice of the third-party services, the KEYS.LAND switch, the automation consent and every setting are kept; one click on "I agree to the License Agreement and the data notice" and nothing else changes.

### 1.23.8 (2026-11-12)

- The minimum listing price ("Do not list items at or below this price" under Settings → Selling & market → Price calculation) is now 0 by default: no such limit. Before, it was 0.03, which on a hryvnia wallet is ₴3, the lowest price Steam takes there, so the cheapest items were never listed, even with the minimum prices of the cards and the other items set to 0. If you kept 0.03, it becomes 0 once; another value you chose stays.
- This setting is now a normal row of Price calculation, no longer hidden among the advanced ones, and every message about it (quick sell's note, the review's list of items left out, the summary after a sale) has a button that opens it, with its value now beside it.

### 1.23.7 (2026-11-12)

- Relisting many listings no longer leaves items off the market at Steam's limit of 250 listings awaiting confirmation: it takes off only as many as Steam can take back, pauses with Continue / Stop at the limit (confirm in the Steam mobile app, then Continue), lists the waiting ones first, and the summary says plainly which items are in your inventory.
- Relisting also pauses when Steam refuses new listings several times in a row for any other reason, before it takes more off the market: the items already taken off wait and are listed first after Continue, Stop leaves them for Retry.

### 1.23.6 (2026-11-12)

- Selling from the inventory, with "Review first" or "Sell as prices come in": the summary at the end now says why every item it left out was left out, so the numbers add up to "left out". Before, items that are not marketable (or sealed, or the other variants and renamed copies of a selected stack) were counted in "left out" but never named; after "Review first" the summary named only a few reasons (the items whose earlier listing waits for your confirmation, the wallet limit), not the minimum and maximum prices, no market price or the order book not read.
- Selling from the inventory: a sale now counts items the same way from start to end. A stack that Steam itself makes (gems, or a game's items shown as one tile with a count) counts as its number of items, as the review's title, its "Sell" button and the warning already did; before, the summary, the progress line, the pause and the review's list of what was left out counted such a stack as one, so a sale of 115 items in 90 listings ended with "Listed 90 of 90". Now it says "Listed 115 items (90 listings) of 115", and the listings waiting for your confirmation are said as listings.

### 1.23.5 (2026-11-11)

- Selling from the inventory ("Sell selected", "Sell everything" and the other sale buttons, with "Review first" or "Sell as prices come in"): when Steam stops taking new listings because about 250 of your listings wait for your confirmation (the Steam mobile app or e-mail), the sale now pauses instead of stopping with "Steam failed several times in a row". Nothing is lost: the selection, the stacks and the prices already read stay. The panel says how many listings wait; confirm them (or cancel some), then press "Continue". The sale also pauses by itself just before that limit, so Steam does not have to refuse a listing first. That count is the script's own estimate: if the panel still says full after one "Continue", the next "Continue" sends one listing to try, so a sale is never held by the estimate alone.
- Selling from the inventory: the summary at the end of a sale now stays on screen, with its "Retry", until you close it or start the next sale. Before, it disappeared after a few seconds, so a sale that ended while you were in another tab said nothing. With "Sell as prices come in" the summary also says what was not listed and why: for example how many items were left out because their market price is below your minimum price for their kind (with "Review first" they are listed at your minimum), and after a stop how many items the sale never reached.
- Selling from the inventory, "Sell as prices come in": each line of the summary about a limit of yours (the minimum or maximum sale price for normal cards, foil cards or other items, the minimum listing price) now has a link to that setting, one for each kind the sale left out, with its value now (in US dollars and, on a wallet in another currency, what that is in your wallet's currency). A click opens the settings on that row, so you can change the limit at once.
- Quick sell (the prices in the item card) and the copies of Steam's own sell dialog: when Steam refuses a listing at the same limit, they now say plainly that too many of your listings wait for your confirmation, and send nothing more.
- Selling from the inventory, "Review first": each row of the review now has a field with how many to sell, all by default. Type a smaller number (or 0 to leave that item out): the title, the "Sell" button and the sum follow at once. The first copies in your inventory's order go; the rest stay in the inventory, unlisted. A stack that Steam itself makes (gems, or a game's items shown as one tile with a count) can be listed in part, as one listing of that many units; reload the page to see and sell the rest. When you choose more listings than Steam takes while your listings wait for confirmation (about 250), the review says that the sale will pause there.
- "Sell as prices come in" of one item (its copies, or one stack): the warning now asks how many to sell, all by default. For several different items it says how to choose a count for each: press "Cancel" and pick "Review first".
- Quick sell (the prices in the item card): for a stack that Steam itself makes, a "Qty" field next to your own price sets how many units to list, the whole stack by default. With "Stacks: one tile per item, with the count" on, the stack's tile has the same field: how many of its copies to list at the price you click, 1 (the selected copy, as before) by default; the selected copy goes first, then the others of the stack, one listing each.
- Steam's own sell dialog, "Copies of this stack": the count may now be written with commas or other thousands separators too, such as "1,000".
- My listings, "Relist overpriced": the summary at the end now says why the listings were left as they are, by reason: your own listings are already at the lowest price on the market (then Steam's price for them is your own price, so they stay; a link next to it opens the setting "Price to list at"), the lowest listing on the market has a tiny quantity and is passed over, so Steam's price is the next price up (a link opens the setting "Ignore a lowest listing with a tiny quantity"), the average sale price for the hours you set is not below their price, or Steam's own prices do not call them overpriced for another reason. Listings already on their way (waiting for "Retry", being relisted or removed, or their sale sent) are counted too instead of being passed by silently. Every listing left gets a grey outline on its price, and its hint says the reason. Prices are not changed by this: the rule stays the same.
- Selling from the inventory, quick sell and the copies of Steam's own sell dialog: Steam does not take a listing when your wallet balance (pending funds included) plus your listings would go over its wallet limit. The sale now checks this before each listing: an item that does not fit is left out and cheaper ones are still listed, an item priced above Steam's maximum for one listing is left out too; when nothing fits any more the sale pauses with "Continue" and "Stop" and says the limit and the room left; if Steam itself refuses at this limit, that is a pause, not an error. The summary says how many items were left out and why. Quick sell and the copies say it plainly and send nothing more. For the check the script counts your listings in My listings (one request per 100 listings) and keeps only their total in this browser; your balance is read from the page and is never kept or sent.
- My listings, "Relist": a listing whose higher price would not fit under Steam's wallet limit now stays on the market as it is, with a note on its row, and the summary counts it. Quick sell: when Steam refuses a listing, Steam's own words now follow "Not listed".
- My listings, "Relist overpriced": the summary at the end now says why the listings were left as they are, by reason: your own listings are already at the lowest price on the market (then Steam's price for them is your own price, so they stay; a link next to it opens the setting "Price to list at"), the lowest listing on the market has a tiny quantity and is passed over, so Steam's price is the next price up (a link opens the setting "Ignore a lowest listing with a tiny quantity"), the average sale price for the hours you set is not below their price, or Steam's own prices do not call them overpriced for another reason. Listings already on their way (waiting for "Retry", being relisted or removed, or their sale sent) are counted too instead of being passed by silently. Every listing left gets a grey outline on its price, and its hint says the reason. These reasons change no price; the one change of a price is in the next line.
- My listings, the price check and "Relist overpriced", with "Ignore a lowest listing with a tiny quantity" on: a cheaper listing of another seller is no longer passed over because your own listings sit right after it. Before, when another seller listed one copy cheaper and your own listings stood at the next price, that cheaper copy was passed over and your listings were not called overpriced, so they were never relisted. Now only other sellers' copies at the next price count: in that case the cheaper price is Steam's price, your listings are marked overpriced and "Relist overpriced" relists them at it, even when other sellers list many copies above your listings. When other sellers list many copies at the next price up, the cheap one is still passed over, as before. Listings you have just removed, or that a relist has just taken off the market, still count as yours while Steam's prices still show them, so a second press soon after the first relists the rest the same way; and a listing that would go back up at the very price it stands at is not taken off at all. Selling from the inventory is not changed.

### 1.23.4 (2026-11-11)

- Telegram bot: the settings, the extension's options page and the guide name Telegram's BotFather by its link, https://t.me/Botfather.
- "Sell as prices come in": the line "Reading market prices: … · putting up for sale: …" now counts an item's price as read as soon as it is known and shows how many items are still to be put up for sale. Before, it could show 0 prices read for a long time while the first items were already being put up for sale, as if the sale were waiting for every price. With a long delay between listings in the settings (more than 15 seconds), the sale reads fewer prices ahead, so it usually reads an item's price only once and keeps the delay you set between listings.
- Trade offers and trade history: the partner check buttons (Rep.tf, backpack.tf, CSGO-Rep, SteamTrades) are now off by default, on the trade offers pages (incoming, sent and their history) and on the trade history, and they were turned off once with this update. To bring them back: Settings → Profiles & reputation → Reputation, tick "Trade offers pages: partner check buttons on every offer (links only)" and "Trade history: backpack.tf link next to the trade partner". The reputation on Steam profiles and in the trade offer window stays as it was. Steam's own "Report" flag on the trade offers pages stays hidden, with the buttons on or off; its own switch "Trade offers: Steam’s own “Report” button (the flag)" shows it.
- Settings, the card "What's new in v…": the link "Older changes: the full changelog (opens the project page)" now opens the public history of changes on GitHub, grouped by the versions published on the Chrome Web Store, in your language. Before, it led to a page that was not open to users.
- Settings: the CS-2, TF-2 and Dota-2 tabs show the games' own icons from Steam, and the Steam tab (trading cards, gems, backgrounds) shows Steam's own icon, once you have opened an inventory page or a trade window with that game or with your Steam items (until then, and on backpack.tf, our drawn icons).
- Settings: the game tabs are now called CS-2, TF-2 and Dota-2.
- Settings, the Dota-2 tab: under "Dota 2 item marks" a new list explains what each mark on a Dota 2 item tile means and shows it as it looks on the tile: the quality and an Inscribed gem's count at the top left, the Unusual effect and the number of gems at the bottom, the bar in the rarity's colour, the collector items' words and the trade lock at the top right, as the TF-2 and CS-2 tabs already do.
- Inventory: with the box "Stacks: one tile per item, with the count" unticked and the items sorted by price (or by count, or by name), every item on the page you see now shows its picture, after "Load all" and on the next pages too. Before, many tiles stood empty, with only their price and marks.
- Dota 2: "Add the value of the gems inside to the price" now works on real items. Before, the gems in Steam's item descriptions were not recognised, so no gem, no gem price and no sum were shown anywhere. Now the item card lists each gem with its price, or says why it has none (an Inscribed gem is not sold on its own; a gem the price lists do not have), and the inventory worth and the trade sums add the gems. On a page in another language the card says while the gems wait for the item's English description. Dota 2 items kept in the item cache by earlier versions are read again from Steam.

### 1.23.3 (2026-11-10)

- Inventory: with an order of the items other than Steam's order (by price, by count, by name), a game tab that fits on one page no longer disappears once its items are put in order, and the last page of a bigger inventory keeps its items.
- Inventory: Shift + click now selects every item between two items on different pages too (before, only within one page), in the order you see them: with a search or a filter, the stacks, the sort and the rows per page. "Sell selected: N" counts the whole range.
- Your own inventory: a game with a big logo (Bongo Cat) no longer shows it over half the screen above the selling buttons; the logo keeps Steam's own height.
- My listings: "Relist overpriced" and "Relist selected" now say what they are doing from the first second: a line with Stop shows how many listings have had Steam's own prices read, and at the end how many were relisted and how many were left and why (not overpriced by Steam's own prices, already at the calculated price, no price to relist at, an error from Steam, not started). Before, with red marks from a provider's prices, the button read prices for a long time with nothing on the screen, relisted only the few listings Steam also calls overpriced and said nothing about the rest. The question before the start now says how many items' prices will be read and about how long it takes.
- My listings: Stop now also ends the price reads a relist started. Before, they went on, and a later press of a relist button could take off and relist the listings of the press you had stopped.
- My listings: a listing that already stands at the calculated price is no longer taken off and listed again at the same price by "Relist selected" or "Relist overpriced"; it stays on the market and is counted in the line.
- My listings: with a long list of several games, the overpriced marks of the dimmed copies (pages not opened yet) of the later games are no longer lost when Steam's page arrives in the middle of the price check.
- My listings: when a listing awaits confirmation (its small table stands on top of the page), "Relist selected", "Relist overpriced", "Select overpriced" and the other buttons of the whole row, the relist line and the loading mark now stand at your sell listings and work on them. Before, the whole row stood at the small table on top, and "Relist overpriced" pressed there relisted nothing of your sell listings.
- My listings: "Relist overpriced" or "Relist selected" pressed while the list is still loading takes only the listings that are already here, and now says so: the question before the start shows how many of your listings are here, the dimmed rows of your last visit are passed by and counted in the line as still loading (before, as rows with no price), and the line says to press again once the whole list is here.
- My listings: a relist started right after Stop now counts only its own listings in the line; before, the listings of the stopped relist could be added to it.

### 1.23.2 (2026-11-10)

- Steam Market: listings and removals now go no faster than the delay in Selling & market → Selling safety, a random time between the shortest and the longest delay, 2–3 seconds by default, in every tab together. It holds for the bulk sale, the quick sell buttons, the copies of the sell dialog, the My listings tools and relisting, so these are about twice slower than before; relisting takes off 12 listings at a time at the default instead of 25, so every price is still fresh when its item is listed again. With 0 in both fields the script works with no delay, very fast, but this may be dangerous for the account.
- My listings: the page number bars above and below the list stand on a line of their own again; before, on some pages the bar stood beside the first listing and squeezed it.

### 1.23.1 (2026-11-10)

- My listings: the page's tools (search, sort, select, remove, relist, the price check and its colours, the totals), the market history's page jump and the trade window's "Select all from page" are now written entirely in Smart Trader's own code; they work as before. In the trade window, "Select all from page" now also skips items the page hides. The price check on a single item's market page follows the "Full set: mark overpriced / underpriced / fair listings" setting there too.
- Selling at "Steam Market price from a provider": a CS2 Doppler or Gamma Doppler is priced by the first provider of your preset that knows its phase (cs2.sh), even when marketdb.info, which has one price for all phases, stands before it; with no such provider it is priced from the Steam Market's order book, as before.
- Sorting a big inventory ("Sorted n of m items." with "Load all", the stacks off): on a very large inventory the prompt itself now says how many items are left and about how long their load takes, and "Load all" starts at once, with no second question; while it loads, the panel has a "Stop" button. With your own steamapis.com key (the source in Items & inventory; in the browser extension the key is set on its options page) this load goes through steamapis.com like the stacks' load, and the prompt names it and its requests; without a key it uses Steam's own loading, as before.
- Settings: the games' tabs stand in a row, CS2, TF2, Dota 2, then Steam (the Dota 2 tab is now before the Steam tab).
- Selling & market: every row of Bulk actions, Selling safety, Quick selling, Price calculation and My listings now says on hover what it does and in what unit, with an example where the row has details. The offset is your wallet's currency as written; the price check and the relists of My listings keep the same minimums and maximums by item kind. The sell dialog's offset is named as what it is: steps of your currency.
- Ukrainian and Russian: the security alerts are now called "security warnings" there instead of "security alarms", everywhere in the script (the alerts, the settings, the hints and What's new).
- Selling at "Steam Market price from a provider" on a CS2 inventory: the line that says where the sale's prices come from now also names the provider that prices Dopplers and Gamma Dopplers by their phase (cs2.sh) when the first one does not, or says they are priced from the order book.
- Dota 2 item prices (new, off by default): "Price Dota 2 items by their base version" prices a copy of a junk quality (Autographed, Frozen, Cursed, Corrupted and the like; Inscribed only when far from the base or on few sales) by the same item without the quality, from the price lists only; "Add the value of the gems inside to the price" adds the gems less the hammer's charge, and for Prismatic and Ethereal the item card shows "keep the item" and "break it", the totals taking the higher. Selling and listing prices do not change.
- Dota 2: "Split stacks by unlocked styles" (new, on) keeps copies with different styles unlocked in separate stacks.
- My listings: "Relist selected" and "Relist overpriced" now work in batches of up to 25 listings of one game with one read of your inventory per batch instead of one per listing, so a large relist is much faster and stays within Steam's inventory limit; each listing still goes back up at a price at most 3 minutes old (read again when needed). A line above the list of your listings shows the step and the count, with Stop and, for listings taken off the market but not yet put back, Retry. The price check remembers Steam's prices for 10 minutes across reloads and tabs and checks the page you are looking at first. Selling many items reuses the price histories read in the last 15 minutes, and "Sell as prices come in" lists the items with the most copies first.
- Dota 2, "Sell spare copies": copies with different unlocked styles are never counted as spare copies of one another, whether "Split stacks by unlocked styles" is on or off (as with gems).
- Dota 2, "Add the value of the gems inside to the price": the autograph gem is added only to a copy priced by its base version; on top of the Autographed item's own price, which already includes the autograph, it adds nothing (it was counted twice), and the item card says so.
- My listings: the automatic relist setting now says what it does: "Automatically relist listings the price check finds overpriced".
- Selling & market: the minimum sale prices, the minimum listing price and "Do not check listings priced at or below" are now US dollars, like the maximums: counted by Steam's smallest market amount in your wallet's currency, not by an exchange rate. A value you had set yourself was converted once, on the first Steam page that shows your wallet, so nothing changes for it (rounded up to a whole cent: never lower than before); the default values are dollars now, so on a wallet in another currency they now mean more (for example $0.05 is ₴5 on a hryvnia wallet whose smallest amount is ₴1).
- Settings backup: restoring a file made by a version before 1.23.1 converts its selling minimums from your wallet's currency to US dollars by the page's wallet, rounded up to a whole cent, so they stay the same or a little higher (the preview marks them); on a page that does not show your wallet they are saved as written and converted once on the first Steam page that does.
- My listings: with "Compare with the Steam Market before acting" ticked, or when no provider of your preset prices them, the price check marks Steam items (trading cards, backgrounds, emoticons and the like) from the Steam Market's search, up to ten names a request, by the lowest listing in your wallet's currency (the price's hint says "Steam Market lowest listing"), so a big list is marked many times faster; a listing at the lowest listing itself (it may be your own) and the names the search does not find are read one by one, as before. Such a mark is never a sale price: a relist still reads the item's order book first.
- My listings (new, on): with 300 listings or more, the list of your last visit shows at once while Steam's pages load, dimmed and with its price marks, so the whole list is there in seconds instead of about a minute for 10,000 listings; a row can be ticked, removed or relisted only once Steam's own page has confirmed it, and the listings sold meanwhile disappear. The copy is kept in this browser and shown only if under 24 hours old; an older or unused one is deleted at the next visit to the market's page, and "Clear price cache" deletes it at once (to turn it off: Selling & market → My listings).
- My listings, relisting: an item that comes back to your inventory under a new number (CS2 and some other games do this) is put back up only after a second look at your inventory 30–45 seconds later, at the cost of one more inventory read, so a copy of the same item you kept is never sold in its place. A listing Steam refuses to take off the market stays on sale and is left for "Retry", which first checks your inventory; "Remove selected" frees a listing Steam refused twice, and pressing it again tries once more. When Steam does not give your inventory, no more listings are taken off the market until you press "Retry", and the line above the list says how many are still waiting. While Steam has asked to slow down, the line says the automatic relist is paused; "Relist selected" and "Relist overpriced" still work.

### 1.23.0 (2026-11-09)

- Telegram bot (new, off by default): your own Telegram bot can send you the notifications you choose: new incoming offers, a sent offer accepted, the results of Quick accept and auto accept, security alerts, "Steam signed this browser out" and your listings sold on the Steam Market. The notifications of a minute come as one message; during quiet hours they wait, except security alerts (a setting). Make the bot with https://t.me/Botfather, then turn it on in Settings → Notifications → Telegram bot and tick its own consent there; in the extension also turn on its card on the options page (Optional services → Telegram Bot API), where the browser asks for api.telegram.org only. Nothing goes to Telegram before that.
- Extension: the data notice is shown again once after this update (version 18): it now names the Telegram bot, an optional recipient with its own switch and its own consent, and the privacy policy describes it (sections 3, 5 and 9). Your choice of the third-party services, the KEYS.LAND switch, the automation consent and every setting are kept; the Telegram bot stays off until you turn it on.
- The trade window's Σ and the copied "Total:" count KEYS.LAND's keys, tickets and Sacks of Gems at the BUY or SELL their own rows show (the "I'm" setting), not always at BUY.
- The trade window's Keys, Metal and Tickets cards say when their Add put in fewer than you asked, and the "check at cs2.sh" button shows on the partner's CS2 tab again.
- CS2 Doppler and Gamma Doppler: copies of different phases are separate stacks with their own prices in the inventory, the trade history, the history totals and the inventory's Prices panel.
- Price times in tile tooltips, summary cells and the provider lines follow the script's time zone and time format (General), the same everywhere.
- Gems: a provider price older than a day counts as unknown for the maximum price check, so nothing is ground on stale data; the dialog shows how many such items there are. The header's inventory worth now counts items that are off the market only for a time.
- Selling: Quick sell, the sell dialog's Lowest price button and the low price check never use an order book in another currency than your wallet; the multisell price moves by whole steps of your currency and is filled in only for the item it was prepared for.
- My listings (relist of overpriced items): only the copy that was taken off the market goes back up, with its full quantity; when Steam shows two copies alike, nothing is listed and the row says why. A sale Steam answered with an error is not tried again.
- Trade offers: "Decline All Active..." declines only the offers you saw when you opened it, never one that Quick accept or auto accept is accepting, and waits while another tab is accepting.
- Protection: the automatic cancel of foreign offers never touches an offer made before the check was turned on, checks each offer's state before cancelling, and your own offers sent from a window opened while the check was off are known as yours.
- Blurring nicknames for streams: a nickname that looks like a sum of money is blurred too, and short names are hidden in the tab title wherever they stand as a word.
- Card sets: an emptied "Craft [N] sets" field plans nothing (the button waits for a number) instead of all craftable sets. A settings file can no longer quietly turn off the gems' price check or raise their maximum: those rows come in unticked as protection settings.
- Extension: the privacy policy now names the partner links of the "Buy sets" menu and every request to the price server; a refused steamapis.com or pricempire call no longer counts against your daily cap.
- backpack.tf listings priced in a fraction of a key (2.5 keys) pay the fraction in metal at the key's price in refined that the page shows, rounded down to a whole scrap; without such a price the trade window adds the whole keys and says the fraction was not added.
- A foreign-offer warning answered "Yes, it was me" also stops a cancel of that offer already waiting its turn, in every tab.
- Card sets in the trade window: "Take sets…" and "Card sets" count a big Steam inventory once per change instead of at every badge read and every price, so the window no longer freezes while the badges are read; "Take sets…" draws up to 300 rows, the rest with "Show all".
- In the trade window both windows take your badge levels kept up to 7 days (shown faded as old) and read only the games they lack; "Refresh" reads them all again.
- Extension: marketdb.info prices of Steam items (cards, backgrounds, emoticons) over 30 days now work: the list of about 190,000 items no longer exceeds the size the extension accepted; "Refresh now" asks marketdb.info at most every 15 minutes, as often as the site updates its lists.
- CS2 item card: "View in cs2.sh" and "View in Pricempire" are buttons like "3D View" (on the listing page too, without the green outline) and wrap neatly on a narrow card; the line "Prices: cs2.sh" under the cs2.sh price table is gone ("cs2.sh" in the table's title links to the site); the table, the 3D View row and the buttons line up with Steam's own text instead of touching the card's frame.
- Big inventories: filters no longer freeze the page. A filter's next letters, a tag of another category and the click after a search now go over the items on show only (100,000 cards: 100 instead of 100,000). With the stacks on, every filter step goes over the stacks' tiles, not every copy. The items shown are the same as before.
- My listings with 10,000+ listings: the tools work at once on the rows Steam shows, and each page Steam gives joins the list as it comes (with a count), instead of everything at the end in one long freeze. The list shows 100 rows at a time with its own pages; select, Remove selected, Remove all, relist, search and the price marks work on every row, also on other pages (a Shift-click range stays within one page). Removals and relists asked while the list loads start once it is whole, so no listing is skipped. Steam's pace is the same: one page of 100 every 0.6 s (10,000 listings in about a minute).
- Inventory: sorting by price (highest or lowest first), count or name now works with the Stacks box off too: every tile over all the loaded pages, items without a price last, Steam's order one click away in the new Sort list next to Stacks; only prices already known are used, nothing is asked of Steam; big inventories are sorted in the background without freezing the page, and the order comes back right after a window resize.
- Store: bundle boxes show their BundleID (SteamDB link, copy button); free games' boxes show the SubID when the page names it; package and bundle pages show their SubID / BundleID under the title.
- Behind the scenes: the trade window, the trade offers pages and the backpack.tf helpers are now entirely our own code. Nothing changes in how they look or work.
- My listings: the price check and the automatic relist no longer use a Steam order book in another currency than your wallet's (such a row shows "not checked"); a relist Steam refuses shows "Not relisted" instead of a success; a listing Steam sent no item data for is marked "not checked" instead of stopping the check and the totals for the rest of the page.
- My listings: after Steam refuses several requests within a few minutes, removals and relists wait 5 minutes and then go on, with a note in the list's header, instead of stopping until a page reload; they also keep Steam's "too many requests" pause from any open tab and set it for the other tabs.
- My listings: the relist buttons and the automatic relist read the price from Steam again when it is older than 3 minutes; Steam prices saved in the tab are reused for 10 minutes at most, not for the whole session.
- Selling at a provider's price (Pricing strategy "Steam Market price from a provider"): a Doppler or Gamma Doppler is now listed at the price of its own phase, not at the name's price, which is the cheapest phase; when the phase is unknown, the list has no price for it, or the provider has no phase prices (marketdb.info), the sale falls back to Steam's order book.
- Prices shown as cash: the automatic cash-out fee is now taken off even when KEYS.LAND is not first in the preset, or when KEYS.LAND prices are off while a KEYS.LAND copy saved within the last day is at hand; new KEYS.LAND prices for it are asked only while KEYS.LAND prices are on, never with manual KEYS.LAND prices; Smart Trader also stops asking the relay every 5 minutes for figures it does not have.
- Trade window: clicking a row of the item summary no longer freezes the page when thousands of copies of one item are in the offer. Quick and auto accept: the result shows the real count of a big gem gift instead of 1 when the item summary was not ready.
- Inventory: sorting a very large inventory by price no longer re-sorts the whole page every few seconds while prices are still loading; the order updates about every 10 seconds at most.
- Protection (browser extension, with "Warn before opening outside links…" on): a link to a raw IP address (for example https://185.1.2.3/, also in hex or decimal form) now gets the "This address is unusual" warning, and skipping Steam's warning page no longer skips it. When more than ten security alerts arrive at once, an offer waiting for its automatic cancel is no longer lost silently: the next read of sent offers warns about it again and queues its cancel.
- Price providers: a preset containing "Marketplaces (cs2.sh)" now greys out "Show prices in" and shows the locked note, as it already did for KEYS.LAND and marketplaces.
- Store: the "Prices in other countries" button now also hides the list ("Hide prices in other countries"); on a package or bundle page the SubID / BundleID is shown only under the title.
- Inventory: when you sort without stacks and Steam has not loaded the whole inventory yet, "Sorted N of M items." with a "Load all" button appears next to Sort; it loads the rest at Steam's pace, so the sort covers every item.
- My listings: copies of one item now share a single Steam price check, and every copy gets the result at once, also on relist (1 request instead of 1 per row). Relisting in very long lists no longer redraws the page or goes through the whole list for every row.
- Market: when Steam shows its new market page although the classic one was asked for, the note now names the Smart Trader tools that are off on that page and says that prices, the quick-sell buttons and selling from the inventory keep working.
- Market: if Steam's classic price history fails, it is taken from the new Community Market, only when it comes in your wallet's currency (never mixed or converted). When Steam refuses the order book (code 104), it is no longer read as an empty book: the item page takes your wallet's book from the new market, and Steam rates keep using the last known rate for up to a week, with its age shown.
- Selling: a listing whose answer comes in an unknown shape is not sent again; a removal answered with a page is not counted as removed.
- Dota 2: gems, runes, Unusual effects and autographs are now read from Steam's item descriptions. Copies with different gems are separate stacks (a setting, on by default). Treasures count as cases for "Sell all cases". Dota 2 tiles show the quality, the Inscribed counter, the Unusual effect, the number of gems and the rarity colour. There is a new Dota 2 settings tab.
- Steam pages start a little faster: less work when the script loads, and profile pages without TF2 showcase items skip a large stylesheet.
- Big trades: the trade window counts its keys, metal and gems without searching the whole page (quicker after each change to an offer and while it sits open); on trade history pages with trades of thousands of items, KEYS.LAND prices no longer freeze the page: they now appear a few boxes at a time.
- CS2 prices from cs2.sh load about twice as fast on every page and use less than half the memory.
- Dota 2: a new "Dota 2 item prices" section on the Dota 2 tab. Collector items (a Legacy Prismatic colour, bugged items, emblems) get a mark on the tile and the words "its price by name may be far off". An Unusual Effect Gem's effect is named, with a note that the page price is an average over all effects. Legacy, bugged and Kinetic items get links to steamprice.com in the item card and the trade item menu (on your click, nothing about you in the address). Prices do not change.
- Dota 2: a "check at steamprice.com" button on the Dota 2 tab of an inventory and on the partner's Dota 2 tab in the trade window opens that inventory on steamprice.com in a new tab, only when you click it.

## 1.22.19 (Chrome Web Store, 2026-11-05)

### 1.22.19 (2026-11-04)

- CS2 Doppler and Gamma Doppler: the prices now follow the item's own phase. A name's price on the marketplaces is the lowest of all its phases, so a Phase 1 knife read at the price of Phase 4 and an Emerald like the cheapest. Where the script knows the phase from Steam's data and your preset holds a cs2.sh provider, the tile's price, the trade window's summary and sums, the offers, the histories and the inventory's worth in the header use that phase's price.
- The table "Prices on marketplaces (cs2.sh)" in the trade window's card and the inventory's card, and the cs2.sh rows of the price card, show the item's phase and name it. Where the phase is not known they say the price is the lowest of all phases.
- A market listing page of such an item shows a name, not one item: its table has a button per phase, "All phases" by default.
- Selling is unchanged: a listing on the Steam Market goes by the name.

### 1.22.18 (2026-11-04)

- Price checks now read your preset's providers (marketdb.info, cs2.sh) when they stand before the Steam Market: one list, no waiting. A new setting, "Compare with the Steam Market before acting" (General, off by default), reads Steam's live prices too.
- Turning items into gems: the price check can be switched off in the question, and with it on the prices come from the preset's providers without a request per item name.
- Listing at "Steam Market price from a provider" no longer reads the Steam Market for those items, so a big sale goes much faster. Small print under the sale's buttons says how to turn it on, with a button that opens the setting.
- My listings on long lists: much faster, the page freezes far less, Steam's rows stay on show with a count while the list loads, and every row shows (a list over 10,000 lost the rest). The price check marks every listing from the provider's list in seconds; a relist still reads Steam's price first.
- The inventory's page counter no longer jumps every second after "Show advanced filters" on a huge inventory.
- The last page of the tour takes a trade URL however it was copied, and says what Steam answered when the trade window does not open.
- The price panel no longer stops working when the game changes in the inventory.
- The skill for AI agents (Settings → AI) lists the new settings: its version is now 1.22.18.

### 1.22.17 (2026-11-04)

- New button on the Steam inventory: "All items into gems".
- "All items into gems" and "Gems from spare copies" now ask first for the maximum price of one item (US $0.05 by default, Settings → Steam inventory): items priced above it are not turned into gems. Items with no known price are left out too, unless you tick the box. Prices come from the marketdb.info list, and from the Steam Market for items it lacks; the table shows them.
- Turning items into gems is several times faster: the requests go out a few at a time, and the values in gems are read in small groups. After Steam's first "too many requests" the rest goes one at a time.
- The skill for AI agents (Settings → AI) lists the new settings: its version is now 1.22.17.

### 1.22.16 (2026-11-04)

- Accepted offers no longer show items "without a description": Steam gives no descriptions for an accepted offer through the request used so far, so one more request now takes them from the trade itself. The keys that showed as 2,693 + 1 are one stack of 2,694, and the sum counts them all.

### 1.22.15 (2026-11-04)

- The script's header names only Smart Trader as its author. The notices and licences of the other authors' components stay: the end of the script and THIRD-PARTY-NOTICES.md.
- Badge sets are crafted much faster: all the sets a badge can take now go in one request, so a run makes a request per badge instead of one per set. Crafting only a part of a badge still goes one set at a time.
- The craft plan opens faster: your badges are read in small groups instead of one after another. The card sets windows read them the same way.
- The "Craft sets…" button counts ready badges, not sets: "ready badges: 25".
- When Steam marks badges as ready but its answer holds no complete set (for example while Steam restarts), the plan says so, and the next plan asks Steam again instead of using the kept answer.
- The skill for AI agents (Settings → AI) describes this: its version is now 1.22.15.

### 1.22.14 (2026-11-03)

- The cash-out fee works again: since 1.22.10 it was unknown ("relay unreachable") because the new price server has no such figures. Now, when the server gives none, Smart Trader works the fee out in your browser from KEYS.LAND's price and the Steam Market's order book of the item you cash out with.
- Prices panel: the line at its bottom names where the shown prices really came from: a key at KEYS.LAND's price says KEYS.LAND, not the preset's first provider, and the panel is titled so when all its prices are KEYS.LAND's.
- Prices panel: the price sources are plain words, no longer links.
- A KEYS.LAND price no longer shows the cash-out fee's state in its tooltip: that fee is not part of it.
- The "Buy sets" menu says again that these are partner links.

### 1.22.13 (2026-11-03)

- Level UP is now a regular item of the settings menu, with its icon, right before Steam store.
- The note in the "Buy sets" menu now says: these are independent sites, not Steam.

### 1.22.12 (2026-11-03)

- Level UP in the settings menu: it opens the Steam level calculator, at once on your badges page, in a new tab from any other page.
- The level calculator shows your uncrafted sets: "at least N", the exact number is in the crafting plan. With several badges pages it reads them with pauses, and closing it stops the reads.
- The calculator has a "Buy sets" menu of sites that sell card sets. They are partner links to independent sites. Before each site a warning asks you to craft the sets you already have, with a button to the crafting plan.
- Trade window summary: a sort choice in the header of each summary: as picked, by count, by lot price or by name. It is saved at once, the same for both sides, and orders the list with prices.
- The summary tiles now stay in the order the items were added. The new setting "Sort the summary tiles too, by the same order" on the Trade window tab sorts them as well; turn it on if you had chosen an order before and want your tiles sorted.

### 1.22.11 (2026-11-03)

- Sacks of Gems and other stacks on a tile: the price of one and Σ of them all, as with keys: "$0.472" and "Σ $128.86", in trades, the inventory and the histories (until now the sum alone).
- KEYS.LAND prices in the selected offers' summary are written as KEYS.LAND writes them, up to 3 decimals: "$1.625", "$0.472", no longer rounded to "$1.63", "$0.47"; loose gems read "$0.472 / 1000".
- Trade window summary: a new column with the price of one item on every line, between the count and the name, and the figures lined up.
- Currencies of which a thousand units are worth less than a dollar (Rp, ₫, ₩, COL$ and the like): prices and sums in whole units, without decimals. Selling forms keep Steam's exact amounts.
- Rounding checked across the script: a Steam Market price kept in another wallet currency no longer drifts on its way through dollars (the same key read 68,39₴ and 68,45₴), and a copied sum no longer carries group separators.

### 1.22.10 (2026-11-02)

- KEYS.LAND and CS2 prices now come from a separate price server, so the machine that serves updates no longer stands behind them.
- KEYS.LAND prices from its Telegram channel: a price post now counts for up to 10 days (it was 7).
- Auto accept: no more "new incoming trade offer" sound for gifts auto accept is already taking, when Steam answers the list of offers late during an accept.

### 1.22.9 (2026-11-02)

- Inventory value next to the wallet: the amount shows again after a click on the sum button under the factory price presets. Since 1.22.0 it was counted but not kept, so the button stayed as it was; a reading that cannot be kept now says so in the tooltip.
- Every TF2 key and Tour of Duty Ticket now counts at once and at one price, whatever Steam says of the copy: another item instance, no description yet, craftable or not, marketable or not. An accepted trade of 291 keys no longer shows 289 in its sum and in "Selected offers", and the panel takes in a description that comes later without a reload.

### 1.22.8 (2026-11-02)

- A level calculator on your badges page: the "Level calculator" button, left of "Craft sets…", counts from your level and your real XP to a dream level the XP, the card sets to craft and what they bring (emoticons, profile backgrounds, showcases, the friend limit, the booster pack drop rate), live and without a request; its "Craft sets…" opens the plan up to that level.
- Steam Market page, "My listings": a "Remove all" button right after "Remove selected" takes every row of that list, on all its pages, after one question, at the same pace.
- Selling a whole TF2 stack: "Sell selected" and the sell dialog's "how many copies?" now take every copy of the stack at its market name's one price, not only the copies of one paint or class; the dialogs say what the stack holds, and renamed copies are still never sold with it.
- An experimental choice on the Selling & market tab, row "Price to list at": the Steam Market price from a provider (marketdb.info, cs2.sh), never the default. Steam's live order book checks every price first: one below the highest buy order or further from the lowest listing than the allowed difference (25 % by default) is left out, and the review says why with both prices; an item with no usable provider price is priced from the book as usual, and its row says so. Quick sell gets one more button with that price.
- TF2 full stack: each Unusual effect is its own stack, chosen and sold on its own.
- A market name Steam refuses no longer ends a sale: its other copies are skipped, with Steam's message in the result and a button to retry them. Three names refused in a row still stop it.

### 1.22.7 (2026-11-02)

- Offers, history and trade summaries name only the sources whose prices are in that sum: 233 keys at KEYS.LAND's price read "KEYS.LAND", without marketdb.info; a sum with a marketdb.info item reads "KEYS.LAND + marketdb.info". In the trade window a list of KEYS.LAND's items only is captioned "KEYS.LAND", without the "(keys.land)" on each row.
- An item whose description came after an offer was read no longer stays out of the sums: an offer of 969 keys is summed as 969, without "without a description: 1".

### 1.22.6 (2026-11-01)

- The extension packages and the tester's copy of the userscript ship without code comments, apart from the third-party licence notices (smaller downloads, the code itself unchanged); the internal build keeps them.

### 1.22.5 (2026-11-01)

- Selected trades' panel (offers pages, trade and inventory history): "My items (n)", "Partner's items (n)", "I give (n)" and "I get (n)" now count items — a stack of 3992 keys is "(3992)", two offers of 3992 and 1036 keys make "My items (5028)" — not the kinds or the parts of a stack.
- Selected trades' panel: an arrow before "My items" and "Partner's items" opens that side's totals by item — every selected trade's items merged by name ("700× $1.00 Tour of Duty Ticket $700.00"), the largest sum first, with the side's total; closed by default, it stays as you left it while the page is open.
- Offers pages: one rounding everywhere — the totals beside each offer's sides, the offer value, the selected trades' panel and its lines add the items' exact values and round once (190 gems and three cards no longer read $0.17 in one place and $0.16 in another); the unit price of an item worth under a cent, such as a gem, shows per 1000 ("$0.47 / 1000") instead of an empty column.
- Trade window summaries: KEYS.LAND's prices no longer have a column of their own; the list has one price column, a row KEYS.LAND prices (keys, tickets, gems) shows its KEYS.LAND price there with a small "(keys.land)" after the item's name ("(manual price)" for the manual price table), the other rows their price preset's price; the column's one caption names the preset's source, with "+ KEYS.LAND" in its tooltip. The sort by price and the totals are unchanged.

### 1.22.4 (2026-11-01)

- Sums of the offers and of the trade and inventory histories (the offer value, the summary and the sort, the selected-trades panel, the totals under the history's lists): KEYS.LAND's keys, tickets and gems are priced at KEYS.LAND's price again — BUY or SELL by the side, as in the trade window and in KEYS.LAND's own tags — not at marketdb.info's; every other item goes by the price preset's chain. The caption names both sources ("KEYS.LAND + marketdb.info").
- Offers pages: Steam's item pages (one request per kind of item) are asked only on a click of "Prices", whatever the switches — KEYS.LAND's tags and totals beside the offers read the items from the cache, else one request to Steam per offer, the same single reading the offer value uses; an item Steam does not describe there stays without a tag until that click (the total's tooltip says how many).
- Trade history and inventory history: while the totals count every item, the price tags beside the items ask the Steam Market nothing themselves — they show the prices already kept and the ones the totals bring, and are drawn again as those come; KEYS.LAND's prices and the providers' lists work as before.
- Trade history and inventory history: the totals of every item no longer ask the Steam Market by themselves — the prices the providers' lists give (marketdb.info, cs2.sh, KEYS.LAND) and the kept ones are summed at once, the rest reads "+N by the Steam Market", and one "Load Steam Market prices" button above the history asks the Steam Market for them (then "Load next N").
- A new Steam settings tab, right after TF2, gathers every setting for the Steam inventory's own items: the badges and trading cards, the "Card sets" window and crafting, the cards', gems' and booster packs' buttons, "Take sets…" and the card swap check; an "Open the badges page" button leads to Steam's badges page. The settings keep their values.
- TF2 → Stacks of TF2 items → "Full stack: one stack per Steam Market listing" (on by default): TF2 items with the same market name now stack together whatever their modifications — killstreak, sheen, paint, spells, strange parts, Unusual effect, a custom name — in the inventory, the trade window's summaries, the offers and the trade history (15 Max's Severed Heads of five paints are one "15×" row); the stack's tooltip lists the kinds inside with their counts. The non-tradable and uncraftable splits still apply; selling and the trade window's amount dialog never take a copy of another kind as a spare. Off: the stacks split by modifications as before.

### 1.22.3 (2026-10-31)

- Offers pages: the offer value on each offer, the summary of the active offers, the sort by profit and the panel of the selected offers now count every item, priced as the trade window's summary prices it (the price presets: the providers first, the Steam Market within its limits, one budget for the whole page) — not only KEYS.LAND's keys, tickets and gems.
- The items' descriptions come from the cache, else one request to Steam per offer (the offers in view first; Steam's item pages still only on a click of "Prices"); while Steam Inventory Helper is on the page the Steam Market is asked only on a click. Trade offers → Offers list → "Sum every item of offers and history by the price presets", on by default; off: KEYS.LAND's items only, as before.
- Trade history and inventory history: the total under each list of items and the panel of the selected trades count every item the same way ("Σ ≈… · priced: i of n", the source before it; the rows on screen first, one budget a page). The history pages already hold the items' descriptions: nothing more is asked for them.

### 1.22.2 (2026-10-31)

- CS2 "View in Pricempire" links (the button was "View in Pricempire.com"; the name is shorter now) cover many more items: weapon and knife skins with StatTrak™ and Souvenir, Doppler and Gamma Doppler with the phase read from the item's data (the Ruby, Emerald and Black Pearl pages are verified; Sapphire and Phase 1-4 follow the same pattern and are still to be checked live), gloves and hand wraps, charms, stickers (tournament ones too) with their finish and weapon cases.
- Pricempire links also for agents, music kits (StatTrak™ too), patches, sealed graffiti with their colour, pins, case keys, souvenir packages (the map and the event), viewer passes, autograph capsules and team sticker capsules. Other items (viewer passes with souvenir tokens, other keys, operation passes and more) get no Pricempire link yet, nor does a Doppler's Steam Market page (one page lists every phase).

### 1.22.1 (2026-10-31)

- Trade window: the summary's price column caption is short again (the source's name, e.g. "marketdb.info"), the whole provider chain only in its tooltip; the long caption of 1.22.0 squeezed item names into a narrow column and read as "prices from the Steam Market" (TF2 trades with a key).
- A TF2 settings tab after CS2 gathers the TF2 tile marks, the Unusual effect pictures and the backpack.tf page tools; the keys, the game switch lock and the stored values stay as they were.
- In the item card, the hover card and the listing page the Buff, Youpin and C5GAME names link to the item's page by the ids from the cs2.sh catalogue (one file once a day through our server, nothing about you); a row without an id keeps the plain name.
- On a CS2 item's Steam Market page a "View in cs2.sh" button sits right of the "Listings" title, just left of the Fear & Greed index; on each CS2 listing Steam's "Inspect in Game..." moved into the 3D View ▾ menu as its first entry.
- Extension: the cs2.sh price list of all six sources (about 6 MB) now passes the service worker (1.22.0 refused it as "answer too large"); "Refresh now" in the cs2.sh row tries again at once, past a failure's pause.
- Tiles of every game show how much trade hold is left beside the lock (⏳3d; a stack whose copies differ shows the range, e.g. 3-7d); TF2 tiles read Steam's "Tradable After" line too. A CS2 item Steam still flags tradable with a dated end is in its trade protection (the shield 🛡), not locked: such an item can go into an offer.
- On a CS2 item's listing page a "View in Pricempire.com" button opens the skin's Pricempire page, first in the row before "View in cs2.sh"; for now only weapon and knife skins with a wear get the link (StatTrak, Souvenir, Doppler phases, gloves, stickers and cases wait until their page addresses are verified). The "Show the whole order book" button moved right after the "as of" text of the currency row.
- The TF2 settings tab lists every mark the script draws on TF2 tiles (45 swatches painted by the tiles' own styles), greyed when its switch, the game switch or the pictures are off.
- CS2 item card in the inventory: the 3D View ▾ button takes the place of Steam's "Inspect in Game..." button (Steam's action is the first entry of its ▾ list), with "View in cs2.sh" and the new "View in Pricempire.com" in the same row; under the "View in Community Market" block the cs2.sh prices table, as the trade window's hover card shows it. In the trade window's item menu "Inspect in Game..." moved into the 3D View ▾ list and "View in Pricempire.com" stands before "View in cs2.sh".

### 1.22.0 (2026-10-31)

- The data notice is shown again once after this update (version 17): it now names the market history read behind the sales notifications and describes the stored records more exactly. Your choice of the third-party services, the KEYS.LAND switch, the automation consent and every setting are kept; one click on "I agree" and nothing else changes.
- Quick accept and auto accept measure Steam's own pace: the median time per item of your last clean accepts of 20 or more items (per game, 100 to 1000 ms per item) drives the row's countdown and the queue's remaining time, so a fast Steam no longer shows a wait 2 to 3 times too long; every limit (the request's own, the hold, the wait after an unclear answer) is never shorter than before and grows when Steam is slow (up to three times the measured estimate for an unclear answer); while Steam commits at twice the expected time or slower the row says "Steam is slow now: about N s per item". The setting "expected speed of Steam" stays the floor of every wait.
- Header item counts (keys, tickets, gems and the items you added) refresh after every way a trade goes through: a held trade's items when Steam ends the hold, trades seen only on your trade history, inventory history or trade offers pages (each counted once), an offer's own inventories when its items are not described; an inventory the header does not show is never counted, and a trade of only the default items does not count when you removed them from the header.
- Trade history page: a pass or a redo with nothing new writes nothing (the stacks were taken apart and stacked again on every redo on non-English pages, the tab's title rewritten on every pass), so the stack counts and the layout no longer jump; if a hover still flickers it is Steam's own hover or another extension.
- Settings, Price source: "Use KEYS.LAND prices" and "Show prices in" are the first two rows of the section (Steam's rate row right after the currency).
- Settings: a Notifications tab (right after General) holds every notification setting — desktop notifications and sound (the header bell's switches), a new incoming offer, an accepted sent offer, the results of Quick accept and auto accept, the security alerts' sound and the "Steam signed me out" warning; the keys and your choices are unchanged; each of them has its own switch.
- Settings, General → Games: a switch per game (Team Fortress 2, Counter-Strike 2, Dota 2, Steam cards / gems / boosters, every other game), all on by default; a game switched off gets nothing from Smart Trader — no requests, no price lists, no marks, stacks, original names, price card, 3D or CS2 data for its items, its own tools' settings locked with your choices kept, the pages of that game (its listings, badges) left to Steam; switching a game in another tab reaches an open inventory page at once.
- Notifications → "Sales on the Steam Market" (off unless you turn it on): one tab reads your own market history once per the period you set (15 minutes by default) and tells you what sold and for how much — one sale as "&lt;name>: &lt;price> (you receive &lt;sum>)", several sales in one period as one message with the count and the totals and up to five names; a sale at or above the amount you set is told at once; the record belongs to the signed-in account and starts over when another account signs in; nothing is sent anywhere.
- Extension: a failed read of the extension's storage (a browser profile that starts slowly) is read again a moment later and is never taken for "nothing stored": the consent page, the third-party services' switches, the KEYS.LAND switch and auto accept keep their saved state, and "I agree" writes nothing it did not read first. The options page shows a line under the consents: the data notice's version and date, the state of the third-party services and the extension id the data is stored under.
- Trade window: the control row's buttons and boxes speak the interface's language — "Add items", "Add recent", "Add listing", the four currency cards (Keys, Metal, Tickets, Gems: "Add", "Take all"), "Clear my items", "Clear their items", the ids row and the three input hints — and so do the market name search box and the page box of the inventory tools and the "My listings" tools of the market (the select, remove and relist buttons, their confirmations, the fee note); the KEYS.LAND words BUY / SELL / AVG stay as the site writes them.
- Settings, help texts and tips name every button by the label it really shows — "Sell everything", "Sell selected: N", "Sell on Steam's page", "Gems from selected: N", "Gems from spare copies", "Open all booster packs", "Reload", "Lowest price", "Decline All Active...", "Take sets…", "3D View", "Show N more", the profile's link names, the navigation panel's tabs — in English, Ukrainian and Russian alike; the buttons themselves did not change.
- Fixes from an independent audit of 1.21.24: "Sell on Steam's page" now prepares the sale with the whole stack's quantity (a selected stack of 3 gave a quantity of 1); a trade history row of a stack whose copies hold different amounts shows one unit's price and the sum of all units, equal to the box total (it priced 74 units of 87 before).
- More fixes from that audit: the trade history's search keeps non-matching rows hidden after Steam's own "Load More History" (they came back as if they matched); the market "My listings" search finds a name with a hyphen or other punctuation typed as shown; Card sets in the trade window no longer stays "loading" forever after a side switch; a Steam Market request that waited for its turn now honours a pause Steam asked for meanwhile; a price file refused as too large is not fetched again for two hours, as intended; "Clear price cache" in one tab no longer lets another tab's pending badge data come back; the extension's "Delete all Smart Trader data" and "Forget the key" say so when a key could not be deleted instead of reporting success.
- Smaller: "What's new" keeps the entries of the last 30 days (never fewer than 10; the older ones stay in the CHANGELOG), and the extension reads the AI document (Settings → AI) from its own files only when that tab opens, with a "Reading…" line and a retry on failure, instead of carrying it on every Steam page; the extension's page script is about 110 KB smaller.
- Settings: the rarely changed rows of every tab (retry and refresh intervals, list and cache lifetimes, floors, budgets, fine-tuning of sales and tools — 54 rows) sit in a folded "Advanced settings" block at the end of the tab; a search hit or a direct link unfolds it; your values are unchanged.
- Settings tabs no longer have their own on/off switches: each function has its own switch, and anything a tab switch kept off stays off after the update (your settings are carried over, nothing changes on your pages). Phishing and scam protection (experimental): on a new installation each check is off by default; turn on the ones you want.
- Trade window: the Quick button says "Quick Accept" or "Quick Offer" by the page itself (a new offer, an incoming offer, an incoming offer you changed) in every Steam language; the English text of Steam's button is only the last fallback. The click always did what Steam's own button does.
- TF2 marks (tester #3): every footprints and paint spell has its own colour (Team Spirit left red, right blue), the killstreak chevrons are replaced by thematic icons — basic claw marks, a gem in the sheen's colour for specialized, the gem plus the killstreaker's own sign (horns, bolt, tornado, flame, singularity, fireball, eye) for professional; the hover still names the tier, sheen, killstreaker and spells.
- Trade offers, inventory and trade history pages: a sort setting per page ("Order of the stacks" in each page's group) — as grouped / Steam's order (the default, as before), by count, by price (the price the page already shows; unpriced last) or by name; the inventory sorts with its Stacks box on; no extra price requests.
- Prices on all marketplaces (off by default; the switch "Prices on all marketplaces in the item card" in the Price source section): a click on an item in your inventory, the "Prices" entry of a tile's menu in the trade window or a click on a tile on the trade offers pages opens a table — KEYS.LAND buy and sell for keys, tickets and gems; marketdb.info medians for 24 hours, 7 and 30 days with the sales counts; the Steam Market's lowest listing and highest buy order, sales in 7 and 30 days, the 30-day range and a small graph of the daily averages; every marketplace file of the game and pricempire; a cash-out column after fees in your display currency; a provider you have not enabled shows "off" and is never asked; Steam is asked only on the click (the order book and the history), Refresh asks them again; nothing else is sent anywhere.
- Auto accept: when several gifts vanish together, the incoming offers list is read once for the whole queue run (about 10 seconds; an own accept reads it anew) instead of once per vanished offer; the KEYS.LAND prices' copy shown at once while keys.land is asked again may be up to 60 minutes old (was 15; the 5-minute cache is unchanged).
- Settings, "Price calculation (bulk sale and quick sell)": every row is named plainly with its currency in the name ("Minimum sale price, other items (wallet currency)", "Maximum sale price, other items (US $)", "Price to list at", "Do not list items at or below this price"), a one-sentence help under the field, and the details with a worked example in figures behind the "i" mark next to the name (hover or focus); the line "On this page's wallet: about …" under the three maximums shows on every wallet.
- Reputation panel: a 403 or 503 answer without Cloudflare markers shows "open the site" at once instead of "Could not read the page" for two minutes.
- Trade window: a click on a row of the summary list shows that item in the item picker of that side — the first copy, each next click the next copy (back to the first after the last; a copy in the offer is shown in its slot), switching the side's tab, the game and the picker's pages through Steam's own controls; the tile lights up for a moment; an item more than 25 pages away gets a note instead of a long flip.
- Trade window: setting "Order of the summaries (tiles and list)" — as picked in the trade window (the default, as before), by count, by price (the stack's total as its row shows it, unpriced last) or by name; one choice for both sides, re-applied live when a price arrives later (never while the pointer is over the summary).
- Own inventory: the button "Select items to sell" first in the selling row turns on a selection mode — a plain click adds or removes an item (no Ctrl; Steam's item description does not open), a check mark sits on every selected tile, the button counts "Selected: N · Done" (or "Cancel" when nothing is selected), Escape leaves the mode and clears, turning the page keeps both; Ctrl, Shift and the drag box work as before; "Sell selected" uses the same selection.
- Renamed items: setting "Show the original name of renamed items everywhere" (Items & inventory, off by default) shows the market name in Steam's item card and hover cards with the custom name as a line "Renamed: '…'" and stacks renamed copies with the plain ones; with or without it, a renamed TF2 item or a CS2 item with a Name Tag carries an "R" mark on its tile and in the trade summaries (the custom names and counts in the mark's tooltip), and summary rows of one name no longer look like duplicates; duplicates for the bulk sale always keep renamed copies apart, so a name-tagged item is never sold as a spare copy.
- Speed on the biggest trades: one price lookup per kind of item instead of one per item — a trade window with 8,192 cards does 1,200 price lookups per change instead of 33,000, adding a batch of items takes a quarter of the time, and the trade history page's price pass takes half; nothing changes in what is asked of Steam or when.
- The extension loads its backpack.tf page tools only while they ("backpack.tf pages") and Team Fortress 2 are switched on; the service worker reads one local flag the page code writes, never your settings.
- The script is named Smart Trader in Tampermonkey too (1.22.0 is a clean installation), its links point to the public repository github.com/pythhon1c/smart-trader, and the diagnostic log and accept log files carry the new name (smart-trader-devlog-…, smart-trader-accept-log-…); an update that would rename the script again shows a hint instead of opening the install page.
- The data notice now says exactly what happens before you agree: nothing runs on Steam's pages and no request is sent; only the installation's own service state is stored, with no personal data.
- The order-book depth hint on a listing page marks an estimated quantity with "≤" and says that the orders beyond Steam's graph are taken as an upper bound.
- The CS2 item card shows cs2.sh prices per marketplace: the Steam Market, Buff, Youpin, CSFloat, Skinport and C5GAME, each with the lowest listing, the highest buy order, their counts and the data's age; links to the item by name; the attribution "Prices: cs2.sh".
- The same prices appear in the trade window's hover card and under the item header of the classic listing page (CS2 tab: separate switches; the list is loaded only when CS2 items are on the page, and a hover asks nothing).
- Two new price providers through our own price server: "Steam Market (cs2.sh)" and "Marketplaces (cs2.sh)" (CS2 only; the server collects the lists from cs2.sh every 15 minutes, the extension asks it for nothing about you or your items). Preset 1 is now "Steam Market (cash) + marketplaces for the missing items": KEYS.LAND → marketdb.info → Steam Market (cs2.sh) → Marketplaces (cs2.sh) → Waxpeer → Steam Market; Preset 2: Steam Market (cs2.sh) → marketdb.info → Steam Market; Preset 3: KEYS.LAND → Marketplaces (cs2.sh) → Waxpeer. Stored factory presets are updated once; your own presets are untouched.
- A new "CS2" settings tab holds everything about CS2: tiles, float and phase, the 3D view, the listing pages, the prices on the marketplaces (cs2.sh) and the cs2.sh section.
- A "check at cs2.sh" button in the inventory (CS2 tab, your own and other accounts, right of the stacks box) and in the trade window (the partner's CS2 tab) opens that inventory on cs2.sh in a new tab, only on your click; nothing is sent before it.
- "View in cs2.sh" in a CS2 item's menu under "View in Community Market" (inventory, trade window) opens the item's page on cs2.sh.
- Auto accept notifications: a gift its sender withdrew while the script was about to take it no longer brings the desktop notification "A gift auto accept could not take: look at it on the Incoming Offers page" with its sound (the offer's row already says it is no longer active), and a gift auto accept took before the offer watch saw it no longer brings a "New incoming trade offer — pending now: 1" notification right before the "accepted" one — both found in the diagnostic logs of three testers of 2026-10-29 (112 gifts taken, no other fault of the script found).
- The row of a gift Steam did not take after an unclear answer says "tried again later" instead of "in 3 minutes": the wait is 3 minutes for the first two tries, then 5 to 30 minutes, and the day's end after eight tries in a row (since 1.12.9); the README says the same. The diagnostic log's spec names the hinv.refresh status "left" and the notification of a held-back gift, and the log summary tool no longer marks two consecutive pages of one tab as a duplicated tab when their clocks differ by a fraction of a second.
- CS2 tiles: a new "vivid" look of the tile colours (CS2 tab → "Colours of the CS2 tiles: vivid or contrast"), on by default for everyone, the previous look stays as "contrast": a flat colour of its own for every rarity and Doppler phase, so the rarities read apart at a glance; where a colour is too light for the texts they stand on a dark pill. A legend under that row shows every colour of the chosen look.
- Settings dialog: the × and Close buttons now warn about unsaved changes like Escape and a click outside: the first click says how many, the second closes without saving.

## 1.21.25 (Chrome Web Store, 2026-10-27)

### 1.21.25 (2026-10-27)

- Trade offers page: a stack of gems (or of any item Steam shows with an amount) whose tile key carries no amount is now counted by the amount Steam writes on the tile — an accepted offer of 2,828,203 gems read as one gem ($0.000465) in the side's KEYS.LAND total, on the tile's price strip and in the selected offers panel; the inventory, the trade window and the trade history were right

## 1.21.24 (Chrome Web Store, 2026-10-27)

### 1.21.24 (2026-10-26)

- CS2: each skin tile is filled with its rarity's colour (a Doppler with its phase's), with the wear top right, the float bottom left and the Doppler phase or pattern top left — in your inventory, in public inventories and in both inventories and the slots of the trade window, which now reads each item's own float, seed and phase from Steam; a float scale (the five wear ranges, a marker at the float, the value above it) sits under the picture of the selected item and of the trade window's item hover; the trade summary keeps Doppler phases apart; long prices shrink to fit their tile; the 3D button is now "3D View"
- Extension: one box for every optional third-party service and site — empty on a first run ("I agree" then asks the browser nothing), ticked as you left it when the data notice is shown again; while it is not ticked, the settings show a red notice with a button to the extension's options and the Smart Trader button in Steam's header blinks red
- Extension: "Delete all Smart Trader data" now also deletes the script's caches in the Steam sites' own storage (item descriptions, prices, card sets, the items of sent offers, partner history, the quick-accept log, the index history) through an open Steam tab or one it opens for a moment; removing the extension alone does not reach them
- The data notice (version 16) and the License Agreement (edition 2026-10-25: section 8 describes the one box) are shown again once; the automation consent given with the 2026-10-17 and 2026-10-24 editions is kept
- After a review of everything new since 1.21.20: Steam's exchange-rate read stops retrying after a lasting failure, the sent-offers button keeps an awaiting offer until Steam shows it accepted or cancelled, CS2 sticker lines no longer spend the English-description budget, stacks regroup once after the last English copy, the trade window's marks pass runs in slices, the light theme's item card picks its text colour from its real background; faster redraws and fewer cache writes

### 1.21.23 (2026-10-25)

- Market: Steam now serves its market as a new React page without the classic data; where a classic page exists (home, search, an item page) the script brings it back as before, and an item page at a group address with no listings opens the classic search of that skin's group instead of an empty page; the display currency's Steam rate reads its reference items by built-in ids, so no listing page is loaded for it
- Header item counts: after every trade the script sees (accepted, confirmed, reversed, a sent offer accepted, or an offer accepted in its own trade window), the counts of the moved items, your own added items too, are refreshed once, about 20 s later (several trades together: one refresh), by a tab you are looking at and never faster than Steam allows; the tooltip says when they are being updated
- Header: while a sent offer awaits your confirmation in the Steam Mobile app (or by e-mail), a phone button glows in Steam's header with the count in its tooltip; a click opens your sent offers. No requests of its own (the state comes from the background watch, the trade window and Steam's answer when you send). Trade offers → "Blink the header button while sent offers await confirmation", on by default
- Offers page: a stack is painted once — no more "537 + 1" frame for half a second before "538" on every reload (the first pass waited for nothing and grouped by Steam's class id until the item cache had loaded; a box now waits for its descriptions, up to 1.5 s, and the waiting boxes' classes are asked first)
- Price providers → Show prices in: every price, total, tooltip and copied total on Steam's pages in the currency of your choice — any of Steam's 39 market currencies — at Steam's own rate (read from the Steam Market's order book about once a day; until then marketdb.info's rate stands in, marked ≈). The default is as before: "As Steam", your wallet's currency. Selling and the order book's own currency list are not affected
- Prices: item tile labels, totals, the selected offers' lines and the "&lt; $0.01" / "≤ $0.03" notes now use your wallet's currency too (they were in US dollars), converted at Steam's rate; the bounds are rounded up
- Every feature now reads Steam's item text the same way in every Steam page language: TF2 spells, killstreaks, paints, strange parts, medals, uncraftable notes and the stat clock are recognised on Ukrainian and Russian pages from Steam's own wordings, and on any other language from the English description of the item (one request per item class, cached). Stacks, the trade window's summaries, the history lines and the duplicate checks keep painted, spelled and killstreak copies apart as they did on English pages
- Stack keys use the English names of paints, sheens, spells and parts in every language: on a non-English Steam your stacks regroup once after this update (nothing is lost; the same items form the same stacks everywhere, the offers page included)
- Trade history: dates and times are read in Ukrainian, Russian and 20 more Steam languages (local time, the held-trade estimate, the tab's date range and the partner history work there now); a held offer is told by Steam's own state, never by the banner's words
- Unusual effect pictures (Items & inventory → "Show Unusual effect pictures") are on by default and turned on once for every installation; on a Steam page in another language the effect's English name is learned from Steam once per translated name, so the pictures show in every language
- Extension: one consent step — the button "I agree to the License Agreement and the data notice" accepts both (License Agreement 2026-10-24) and asks the browser, in one prompt, to allow the sites for prices and pictures (no box of their own: they receive nothing about you); the only box left is for the reputation checks and services that receive Steam IDs, pre-ticked on a re-ask from your earlier answer; auto accept asks for the automation consent when you turn it on. The data notice is shown again (version 15)
- Settings: a new section "Extension options" at the top of General (extension only) with the button that opens the extension's options page; the red notice above the tabs now says "Not all features work" whenever the browser has not allowed the sites for prices and pictures, and names what is off
- TF2 marks: the killstreak icon shows the tier (one to three chevrons) and the sheen colour; each spell kind has its own glyph (footprints, paint, voices, exorcism, fire, pumpkin bombs; "+n" for more); a crate's series "#N" sits where the craft number goes (from the English name, in every page language); the trade window's slot and summary tiles and the classic market rows carry the same marks; hover for the names
- Settings backups made before this version keep the effect pictures on; the learned effect names are kept up to 600 per browser

### 1.21.22 (2026-10-24)

- Trade window: a double click or a drag that Steam refuses now shows a note at the tile saying why — Steam does not mix trade-protected items (for example CS2) with items without trade protection in one offer, so after such items are in the offer a double click on another game's tab adds nothing. The script's own add tools (Add items, keys, metal, tickets, gems, Select all from page, Take sets, the quantity dialog) follow the same rule now and say how many items were left out
- Trade window: the summary is back below the item picker; inside it the item tiles come first, 7 per row by default (Trade window → "Summary tiles per row": off, 4 … 8), the tiles fold with the ▾ button (kept per side), and the list of items with prices is always shown; the KEYS.LAND strips under the tiles fit 6–8 per row
- Trade window: the "Keys · Add / Take all" card shows for TF2 only
- Settings backups made before this version keep their "large tiles off" choice as 8 tiles per row

### 1.21.21 (2026-10-24)

- Prices: a price that rests on too few sales is final and counted in the totals, shown in yellow (the total too, with a tooltip); it no longer sends the item on to the next provider by default. A new switch in a preset of your own, "Too few sales: ask the next provider" (off), restores the old fall-through
- Price providers → Price floors: marketdb.info floor $0.03 (a price at or under it shows as "≤ $0.03", stays out of the totals and asks no other provider), Steam Market floor $0.05 and marketplaces floor $0.10 (an item already known to cost that much or less is not asked of that provider again); 0 = off
- The "not in the sum" notes say why: older than a day, under a cent, at most the floor; a side whose prices all stay out shows the note alone
- Steam Market: nothing is queued while Steam has paused us or the market is halted; queued automatic names are dropped at a halt and the page is priced again when the pause ends
- Trade window: each side is priced for its open inventory tab and the offer only; a tab switch prices that game then. marketdb.info's lists of the other games present in both inventories load later, from idle time (new setting "marketdb.info: load the lists of": open tabs / every game present (default) / every game this browser has lists of; replaces "lazy")
- Trade window: an empty side shows "No items" instead of a provider line; the summaries start folded (the arrow unfolds them, the choice is kept per side)
- Item tiles: the price label is one line — no fee line and no "≈" (both stay in the tile's tooltip and in the summaries) — on a see-through background
- TF2 marks: the key icon (installed strange parts) no longer shows on Strange War Paints and on war-painted strange weapons without parts: their own counter line is not a part; parts of war-painted weapons still count
- Trade history: totals redraw only what changed
- Header inventory value: few-sales prices count; floored, sub-cent and day-old items are named apart in the tooltip
- Extension: when "Third-party services and sites" is off or the browser has not granted the sites, the settings show a red notice above the tabs with a button that opens the extension's options on that switch

### 1.21.20 (2026-10-20)

- Trade window: each side's summary folds to its totals with the arrow beside its copy button, and unfolds again; the choice is kept for each side

## 1.21.19 (Chrome Web Store, October 2026)

### 1.21.19 (2026-10-19)

- Fear & greed index: its own order-book history keeps one row an hour for the last 7 days and one row a day (that day's medians) before them, for at most 500 items — at most a few MB in the browser instead of up to about 100 MB; the index reads the same

### 1.21.18 (2026-10-19)

- Market item pages: a fear & greed index for items with enough data — a gauge and its 30-day line beside "Listings"; hover or focus it for the components (momentum, buy pressure, scarcity, Steam volume, spread, volatility) with their numbers. It reads only what the page and its order book already have (no extra requests) and keeps a small history of the order book as you open the item. An indicator, not advice
- The classic Steam market (not the Beta) is on by default
- Order book: "Show the whole order book" sits in the middle of its row

### 1.21.17 (2026-10-19)

- Trade window: a copy button on each side's summary copies the whole list with the totals; rows without a price are red; KEYS.LAND's keys, tickets and gems get KEYS.LAND's price in the summary and count in its total (it matches the side's total now)
- Trade window: the side note splits "without a price" (red) from "not in the sum" (too few sales, old or under a cent) and wraps to its own line instead of running past the panel
- New trade offer: the inventory opened first is "As Steam chooses" by default (new installs and reset settings)
- Order book: "Show the whole order book" next to the currency shows every row of both sides at once

### 1.21.16 (2026-10-19)

- Classic market: the first visit to a case's, a key's or a capsule's listing opens that listing (it could land on a search with the "… Key" beside it)
- Selling tools: the line "Prices on this page come from marketdb.info" no longer shows on inventories of games marketdb.info does not cover

### 1.21.15 (2026-10-19)

- Market item pages (classic layout): an order book in place of Steam's 5-row tables — any of 39 currencies (Steam converts), "Seller gets" after the fees for each listing, "You get" for each buy order, the step from the price before (amount and %), and "Show 10 more" / "Show all" / "Show fewer" (the number is a setting; 0 = all). Each column has its own switch in Selling & market

### 1.21.14 (2026-10-19)

- Prices: for games marketdb.info does not cover (such as Bongo Cat and Banana) and for Steam items its lists lack (emoticons, backgrounds), Steam Market prices now come from the market's search, many items per request — about twice as fast; such a price is the lowest listing now and says how many are on sale ("?" and out of totals with fewer listings than the minimum)
- The Steam inventory's marketdb.info prices are read back about twice as fast on every page

### 1.21.13 (2026-10-19)

- Trade window: stacked items of other games (such as Bongo Cat and Banana) now go in — "Add items" takes the number of items asked for from stacks (part of a stack as Steam's own amount dialog does), "Select all from page" puts whole stacks in; a stack that cannot be traded is left out and the note says so. Steam's gem stacks still go through the Gems card

### 1.21.12 (2026-10-19)

- Prices: an item with no or few sales in marketdb.info's chosen period (rare knives and skins, emoticons, backgrounds) takes marketdb.info's 30-day price instead of none (the tooltip says so)
- Prices: while the Steam Market cannot answer (limits, errors), the next provider of the active preset prices the items meanwhile; Steam's own price replaces it when it comes
- New setting, on by default: "Too few sales (marketdb.info, Steam Market): ask the next provider" — a price of too few sales no longer ends the chain; it stays the last resort with "?"
- Items off the market only for a time (CS2's trade protection, a dated trade lock) are priced like the others

### 1.21.11 (2026-10-18)

- The extension's start page (data notice): every box with its heading is now together at the bottom, right above "I agree"; the texts are unchanged

### 1.21.10 (2026-10-18)

- Trade offers: the partner check buttons are full-size again on offers without Steam's report button (the history, sent offers) — they were squeezed into a thin strip
- Trade history: Rep.tf, CSGO-Rep and SteamTrades beside backpack.tf after the partner's name, by the same switches as on the offers

### 1.21.9 (2026-10-18)

- API keys in one place: in the extension both the pricempire and the steamapis.com key are entered on the extension's options page and kept by its background part — Steam's pages never see them (a pricempire key entered before moves there by itself); in the userscript both are fields of the settings dialog

### 1.21.8 (2026-10-18)

- Trade offers: the partner check buttons now include CSGO-Rep and SteamTrades beside Rep.tf and backpack.tf, on sent offers and in the history too; each button can be turned off (Settings → Profiles & reputation); Steam's own "Report" flag is hidden by default (a setting brings it back)

### 1.21.7 (2026-10-18)

- KEYS.LAND: when keys.land does not answer, the prices come from its Telegram channel right away — no longer only when the kept copy is over 6 hours old; with no KEYS.LAND prices at all the channel is read at once (at most once a minute), otherwise at most once in 30 minutes, and its post is used when it is newer than the kept copy

### 1.21.6 (2026-10-18)

- Offers pages: "Select all" moved out of the offer value bar into its own row right under it (it belongs to the selection of trades, not to the value)

### 1.21.5 (2026-10-18)

- KEYS.LAND and provider prices (trade summaries, the trade window, history, the selection panel) no longer carry "+" or "-": the colour says BUY or SELL. The offer value chips keep their sign (profit or loss)

### 1.21.4 (2026-10-18)

- Trade lines: a line of one item shows its unit price too ("1× -$0.67 Tour of Duty Ticket -$0.67")
- The data notice and the license dialog: the box of third-party services and sites, and the automation box, say what does not work without them instead of calling them optional
- Texts: the header's auto accept switch is called AA everywhere

### 1.21.3 (2026-10-18)

- KEYS.LAND: "Fill from keys.land" works only while "Manual price" is ticked (without it the table is not used)

### 1.21.2 (2026-10-18)

- Phishing and scam protection: with its tab off everything in it is off, the check of a gift against Steam's record before auto accept takes it included (the help of auto accept says so); the side menu of the settings no longer shows the "Experimental" mark (the tab's page and its switch still do)
- Header: the auto accept button shows the letters AA instead of a lightning bolt

### 1.21.1 (2026-10-18)

- Big inventories: filtering is much faster — the first click after typing a filter takes about a tenth of a second instead of over a second, and clearing the filter under one second; tiles of pages out of sight are kept aside and put back in one go

### 1.21.0 (2026-10-18)

- Faster pages on big profiles: item descriptions, prices, card sets, kept item names, partner history and sent offers now live in the browser's database and are saved one record at a time, instead of large values rewritten whole; your existing data moves over by itself, and old entries are cleaned once a day
- In a private window (no browser database) partner history and sent offers are still kept as before
- Under the hood: background jobs share one scheduler and most of them pause in hidden tabs; trade modules talk through events; the diagnostic log counts the script's own errors; settings of very old versions are taken over once and no longer synced

### 1.20.0 (2026-10-18)

- A lighter script: the Ukrainian and Russian texts are stored compactly and only your language is unpacked, so the download is about 1.5 MB smaller and it starts faster
- Under the hood: one place for the rules and the list of third-party sites, for the pauses between requests and for the storage keys; the settings and the texts split into smaller parts. Nothing changes in what you see or in what is sent
- Settings: the "Experimental" mark of the Phishing and scam protection tab stands under its name in the side menu (it squeezed the name before)

### 1.19.2 (2026-10-17)

- Phishing and scam protection is now an experimental feature, off by default. It was switched off once where its settings were never changed; to use it, turn its tab on in the settings
- Auto accept and Quick accept still check the items of an offer against Steam's record with the protection off: a gift is taken only once Steam confirms it, and an offer found wrong is never accepted
- Narrow windows: the price graph's dates no longer draw over the navigation panel, and the CS2 line of a listing (wear, float, phase, seed) wraps instead of being cut off

### 1.19.1 (2026-10-17)

- Narrow windows: in Steam's small-screen layout the navigation panel has its own Smart Trader button, and a #ct-settings link opens the settings on an open page too
- Trade window: "Add multiple items" no longer skips stacks silently and says when fewer items went in; the summary shows gems, keys and tickets priced by KEYS.LAND apart from the market and names the currency of each price column
- Big inventories: one total everywhere (header, pages, sets window); item marks reach every page after a late start
- Fixes: CS2 lines and the listing tooltip in your language, an empty highest buy order shows "-", clearer messages in the extension's options and 3D viewer, the data notice after install opens with the first window

### 1.19.0 (2026-10-17)

- What's new: after an update this card lists every change since the version you had, newest first; when the script leaves older entries out (it keeps the last 60 days), a link opens the full history

### 1.18.1 (2026-10-17)

- Big inventories: with "Rows per inventory page" at 5×100 or 5×200, the pictures of items that arrived in a later portion of a whole-inventory load now load too (some of them stayed empty before)

### 1.18.0 (2026-10-17)

- Big inventories in minutes: with your own steamapis.com key, a whole inventory of hundreds of thousands of items loads through steamapis.com in a few minutes instead of hours behind Steam's limit (about 8 requests of 2,000 items every 10 minutes). Items & inventory → "Big inventories: a service with your own key" → "Load big inventories through" (off by default). It is used only when you ask for a whole load and Steam's own limit would stop it; the cost (requests) is shown before the first call, another person's inventory needs your confirmation, a daily cap (150) protects your balance, Stop ends the paid calls at once, and any failure falls back to Steam's own loading. The key is set only in the extension's options (or your script manager's storage) and is sent only to steamapis.com
- Extension: one box for all optional third-party services and sites on the data notice (instead of a box per service), with the full list of who gets what and when; with the default settings ticking it starts the partner reputation lookups, marketdb.info prices, Waxpeer's price file and the Telegram fallback at once. The data notice and the License Agreement are shown once more

### 1.17.3 (2026-10-17)

- Tips wait for you: they and the tour offers no longer appear by themselves. A softly blinking "?" next to the ⚡ auto accept button asks first — "Show tips" starts them as before, "Not now" keeps them off (the "?" stays and asks again when clicked; after a yes it opens the tips settings and the tours). Settings → General → Tips has the same "Show tips" / "Ask me again"

### 1.17.2 (2026-10-17)

- The header in your language: the navigation panel's buttons now have Ukrainian and Russian words, and the whole header follows the Smart Trader language as soon as it is known (and when you change it) without a reload. When Steam shows its own header in English (it follows your account's language), its menu words are said in the Smart Trader language too — Header & navigation → "Steam header: say Steam's own menu words in the Smart Trader language…" (on); names and logins are never touched
- Trade window: in "My summary" the Sack of Gems (and other Steam community items) no longer looks blown up next to keys and tickets

### 1.17.1 (2026-10-17)

- AI tab: "How to use with AI agents" — drag SKILL.md into your agent's chat or add it to its workspace; the ChatGPT desktop app (Work or Codex) with the ChatGPT browser extension; or save it where Claude Code (.claude/skills/smart-trader/SKILL.md), OpenAI Codex (.agents/skills/smart-trader/SKILL.md) or other agents load skills by themselves, each path with a copy button. One download, "Download SKILL.md" (the second button saved the same text under another name)
- The skill has its own version (Settings → AI: "Skill version for this script"): it changes only when the skill's text does, so bug-fix and performance releases keep it; an agent whose saved SKILL.md has another skill version than the script in the browser takes that script's own

### 1.17.0 (2026-10-17)

- KEYS.LAND prices keep working when keys.land cannot be reached: they are taken from the latest price post of its public Telegram channel (t.me/s/keysland), and if that post cannot be read, from the one before it. Such prices are marked "KEYS.LAND (Telegram channel)" with the post's time, posts older than a week are not used, the channel is asked at most once in 30 minutes, and keys.land itself is tried again every 10 minutes. KEYS.LAND → "When keys.land cannot be reached, take its prices from its public Telegram channel" (on); in the extension the channel has its own box on the data notice page (unticked until you tick it), so the extension shows its data notice once more
- Settings: a switch with a help now sits on its name's line and the help runs across the whole row below it, as the other fields since 1.16.2 — most tabs got shorter

### 1.16.2 (2026-10-17)

- Settings: a list, number, text or key field now sits on its name's line and the help text runs across the whole row below it, so long explanations take far fewer lines (Price providers → "pricempire API key": the field at the top right, its help shortened); switches look as before
- Price providers → "Steam money is cashed out with": the choices read "TF-2 Keys", "TF-2 Tickets" and "Steam Gem Sacks", each with its Steam picture, in a list you can also use with the keyboard

### 1.16.1 (2026-10-17)

- Partner history: Smart Trader counts your completed trades with each partner (from the trade history pages you open and the offers you accept here) and shows it on every offer and in the trade window — "7 trades · last 3 days ago", or "No trade since &lt;date>" for someone you never traded with (a hint, nothing acts on it). Only one-way codes of the partners, counts and days are kept, on this computer. Phishing and scam protection → Trade offers → "Count my trades with each partner…" (on) and "Forget partner history"; the extension shows its data notice once more for this
- Session alert: a warning when Steam no longer accepts this browser's sign-in (the offer watch, auto accept and the checks pause until you sign in). Phishing and scam protection → Account and devices → "Warn when Steam signs me out in this browser" (on)
- Settings backup: General → Settings backup → "Export to a file" and "Restore from a file…". The file holds your settings only — never keys, trade links, consents or the licence. A restore shows every change first; the protections (phishing and scam protection, auto accept, selling safety, auto relisting, link warnings) stay as they are unless you tick them

### 1.16.0 (2026-10-16)

- CS2 items: each skin tile in inventories gets a strip with its wear, float and Doppler phase (for example "FT 0.2345 · P2"), read from Steam's own item data first; the trade window and trade offers show the wear only. Items & inventory → CS2 float, wear and phase → "What the CS2 strip shows" (wear; wear and float; with the Doppler phase — the default; all of it and the pattern seed) and "Float digits on the strip". While "Blur nicknames and logins…" is on (for streams), the float and seed are hidden
- Steam's classic listing pages of CS2 skins get a line under each item with the wear, float, phase, seed and stickers ("CS2 listings…", on); Steam's new Market pages are left as they are
- Trade locks on item tiles (every game): "⏳4d" until an item can be traded, 🔒 not tradable, 🛡 CS2 trade protection, with a line in the item card. Items & inventory → Item marks → "Trade locks on item tiles…" (on)
- Next to CS2 Trader or CSFloat: when one of them draws its own floats on the page, Smart Trader removes its strips and listing line there and moves its «3D» row out of their way

### 1.15.3 (2026-10-16)

- Big inventories: while the whole inventory loads, the stacks panel says how many items the stacks already cover and that the rest is loading at the script's own pace (only a real pause from Steam is called Steam's wait); it no longer says "0 items loaded" before the first part arrives; page turns at 5×200 rows and the "Card sets" window on a big inventory are quicker

### 1.15.2 (2026-10-16)

- 3D view of CS2 items: skinflow.gg is no longer offered — it shows the same as CS2 Inspects. The 3D button opens 3dview.cs2inspects.com (the default, in a Smart Trader window), csmarketcap.com or swap.gg; if you had chosen skinflow.gg, Items & inventory → 3D view of CS2 items → "Viewer the 3D button opens" is now CS2 Inspects. The License Agreement and the privacy policy no longer name it

### 1.15.1 (2026-10-16)

- Privacy: the License Agreement (version 2026-10-16) and the privacy policy (effective 2026-10-16) now say exactly when each price service is asked (with presets: only while it is in the active preset and an item reaches it) and what the diagnostic file holds; the extension shows its data notice once more for this. The diagnostic log now starts only after the License Agreement is accepted
- Speed: saving item info, market prices and settings no longer copies the whole store each time, other tabs read only what changed, the price panel and the trade window checks do less work, and the background part of the extension no longer wakes up on every save
- Texts and look: one word for each thing in Ukrainian and Russian («трейд», «офер», «провайдер цін»); the extension has its own first tip (the toolbar icon instead of the Tampermonkey menu); Quick accept status lines are translated; settings tab names wrap instead of being cut, a disabled button says why under it, better contrast in the light theme (market page numbers, header switch icons); anonymous visitors of the new Steam Market get the signed-out buttons
- Security: one shared table of hidden and direction-changing characters cleans every name and notification text; notifications keep their line breaks; the 3D window of the extension opens on screen even when its last place is off screen

### 1.15.0 (2026-10-16)

- Trade offers: each offer shows its value for you — what you get minus what you give, by the active price source: "+$x" in green, "−$x" in red, "±0" when even, "≈" while some item has no price yet ("≈?" when a whole side has none), and the warning colour when your own side is not fully priced (check it before accepting); the tooltip gives both sums and how many items are priced. A line over the list sums up the active offers. Settings → Trade offers → "Offer value: profit or loss on each offer" (on)
- "Sort the offers": "As Steam lists them" (default), "Profit for me: highest first", "Profit for me: lowest first (losses first)", "What I get: most valuable first" — offers never move under the pointer or while you work in the list; when new prices change the order, an "Order changed — re-sort" button shows instead. Auto accept and Quick accept never use these values

### 1.14.1 (2026-10-16)

- Big inventories: with a filter on (the stacks are one) Steam keeps every page of the inventory hidden in the page, so each click on a large inventory cost seconds; now the hidden pages are kept out of the page and each is put back right before Steam shows it — page turns, tile clicks and the "Card sets" window are many times faster. Settings → Items & inventory → "Big inventories: keep Steam's hidden pages out of the page" (on): turn it off if another extension misses items on the page
- Loading a whole inventory: estimates count the 2,000 items Steam really gives per request and a pause that is still running, and say that Steam often stops a large load for 10 minutes after about 8 requests; during such a pause the stacks already cover what is loaded and the wait shown is the real one from the first second; Steam's red "not available" box no longer appears for our own paced load; "Rows per inventory page" at 5×200 turns pages without the growing freezes
- Steam's empty page (an answer with nothing in it, which Steam sends after many quick page loads) is now recognised like its error pages: a note and the usual automatic retries instead of a white page

### 1.14.0 (2026-10-16)

- Prices: several price providers at once — Settings → Price providers → "Several price providers" (on) and "Active price preset": the providers of a preset price an item in order, the next one only when the one above has no price of it (or it is off, without its key or a day old). Three factory presets: "Preset 1 · cash" (KEYS.LAND → marketdb.info → Steam Market → Waxpeer), "Preset 2 · Steam Market" (marketdb.info → Steam Market), "Preset 3 · KEYS.LAND + marketplace" (KEYS.LAND → Waxpeer)
- "Price presets": add, duplicate, rename, delete and reorder presets and their providers (▲ ▼ ✕, "Add provider…"); a provider that needs a key is offered only once its key is saved; "Reset presets to defaults" resets only the presets. Your 1.13 choice carries over: the factory defaults move to Preset 1, a changed choice stays as "My settings before presets". Selling always uses Steam's own listings, never a preset

### 1.13.0 (2026-10-16)

- Look: one set of buttons, labels, fields and panels across the script (the navigation panel, header controls, settings, panels, tips, toasts), visible keyboard focus, readable hovered buttons and the same colours in the dark and light themes; «3D» and its ▾ menu form one split button
- Prices: when a price provider is unavailable, rate-limited or turned off, every price surface says so — which provider, since when, how old the cached prices are and when the next try is; prices older than a day are marked and left out of sums

### 1.12.14 (2026-10-16)

- 3D view of CS2 items: in the extension the 3D button now shows CS2 Inspects' viewer inside a Smart Trader window (one window, reused for the next item) with the item's name, Details and the other viewers — no jump to their site; the userscript opens it in a pop-up window. Settings → Items & inventory → "Where the 3D button shows the viewer": a separate viewer window (default) or a new browser tab. The viewer still gets only the item's inspect link.

### 1.12.13 (2026-10-16)

- Prices: with marketdb.info, the Steam Market or a marketplace next to KEYS.LAND (the factory defaults), your own keys, tickets and gems are now valued at KEYS.LAND SELL as with KEYS.LAND alone (they showed BUY); "I'm" (Settings → KEYS.LAND) decides it in every price source
- Every price now shows the trade side as KEYS.LAND alone did: in "operator" mode what you give is green "+", what you get is blue "−" — marketdb.info, Steam Market and marketplace prices included (their amounts do not change); "average" stays neutral. "I'm" works with KEYS.LAND off too. The inventory value in the header still counts keys, tickets and gems at BUY, and its tooltip says so

### 1.12.12 (2026-10-16)

- Auto accept: a gift is now checked against Steam's record of that ONE offer (its own page, read by the extension out of the page's reach), not the whole Incoming Offers page — gifts of thousands of items (up to 8192 cards) are taken however many big offers wait on the page; the same single read also gives the partner and the trade hold, so each gift costs one request

### 1.12.11 (2026-10-16)

- Extension: the options page's Optional services section says when part of Smart Trader is unavailable because an optional service is off or the browser has not allowed its site; everything else keeps working.

### 1.12.10 (2026-10-16)

- Selected offers panel (offers and history pages): every line shows the price of one item between the count and the name — "68× -$1.66 Mann Co. Supply Crate Key … -$112.88" — in the colour of its total; "≈" where a rounded price would not add up exactly, and the side's Σ also says "≈" (and "?" for a price with few sales) when it holds estimated prices. The trade window's item list writes its prices the same way.

### 1.12.9 (2026-10-16)

- Auto accept: a gift is no longer stuck at "Waiting for Steam's record of this offer" when big offers sit on your Incoming Offers page — the extension now reads pages up to 8 MB (2 MB before) to check the gift's items against Steam's record; a page still too big says so, and Quick accept always works
- Auto accept retries every error by itself with a growing pause — 30 s, 1, 2, 5, 10, 20, then every 30 min — a busy Steam, a failed list read, an unsure accept or a gift Steam did not take; a success starts the steps over, and a reload keeps them (for an hour at most). A gift whose accept Steam keeps answering unclearly is tried at most 8 times a day

### 1.12.8 (2026-10-15)

- 3D view of CS2 items: 3dview.cs2inspects.com (CS2 Inspects) is the new default viewer of the 3D button, with its owner's permission; your click opens it in a new tab with only the item's inspect link. If you had skinflow.gg (the old default), it switches once; another viewer you chose stays. skinflow.gg, csmarketcap.com and swap.gg stay in the ▾ menu and in Settings → Items & inventory.

### 1.12.7 (2026-10-15)

- Trade window: "Card sets" and "Take sets…" are shown only while a Steam inventory is open, no longer on a game's inventory (CS2, TF2 …); "Card sets" stays there only when the offer itself holds trading cards.

## 1.12.6 (Chrome Web Store, 2026-10-15)

### 1.12.6 (2026-10-11)

- Prices: in the totals (trade window, offers and history pages, the panel of selected offers) the fee words ("Steam's fee, −24.1% cash-out") go on a line of their own under the sum, so the sum fits narrow panels; sums with marketdb.info, Steam Market or marketplace prices are shown in whole cents, as the tiles.

### 1.12.5 (2026-10-11)

- Prices: marketdb.info, Steam Market and marketplace prices on item tiles are shown in whole cents ("≈ $0.68", not "≈ $0.678"); a value under half a cent reads "&lt; $0.01" and still counts in the totals. KEYS.LAND's own prices keep their decimals.

### 1.12.4 (2026-10-10)

- Prices: Settings → Price providers → "Steam Market / marketdb.info prices as" replaces "Show Steam Market prices as cash" with three choices: "Market price (what a buyer pays)", "Cash after the cash-out fee" (now also with KEYS.LAND off — keys, tickets and gems are then valued like every other item) and "Steam balance received (after Steam's fee)"
- While KEYS.LAND is on that choice is set to cash and locked: KEYS.LAND's prices are cash prices, so a total never mixes cash with market or Steam balance prices; your own choice comes back when KEYS.LAND is turned off. The old checkbox carries over: ticked (its default) → cash, unticked → market price
- Price providers follow one table: one main source — marketdb.info, Steam Market, a marketplace or none — and KEYS.LAND as a switch of its own that goes with any of them (the source's choice "KEYS.LAND" is gone: it is now none with KEYS.LAND on). marketdb.info and the Steam Market are never used together; a marketplace uses one of them only as cash and only for the items it does not price. The marketplaces' "Keys, tickets and gems at the KEYS.LAND cash price" is now that same KEYS.LAND switch (ticked with a marketplace → KEYS.LAND on)

### 1.12.3 (2026-10-10)

- Inventory value next to the wallet: a click that cannot count now says exactly why and when, and counts by itself once it can
- Inventory value next to the wallet: with auto accept on, a click is no longer refused (it waits only while auto accept takes a gift); on your own inventory page a click counts as soon as Steam's page has loaded its items, and a "loading" sign of Steam's that never goes away holds it a minute at most
- Inventory value next to the wallet: while KEYS.LAND's prices have not come, the tooltip says so (keys, tickets and gems are priced by KEYS.LAND only) and the count goes again by itself once they come; a tab that could not load them once asks again at the next count instead of keeping that until "Clear price cache" or a reload
- Phishing and scam protection: with auto accept on, the checks (devices, offers not sent from this browser and their cancel, hidden offers, trade items, inventory) no longer wait for as long as it is on — they wait only while it accepts a gift or reads its list
- Prices as cash: Steam Market and marketdb.info prices now also take off Steam's own market fee (≈ 13 %) before the cash-out fee — what selling the item on the Market and cashing out would really give; keys, tickets and gems stay at the KEYS.LAND price

### 1.12.2 (2026-10-10)

- Phishing and scam protection → Trade offers → "Warn when a trade offer shows items that are not in it, or hides items that are…" (on by default): malware in your browser can paint items into a trade or hide items from it, so that a scam offer looks favourable. On the Incoming and Sent offers pages and in the window of an offer, the items shown are compared with Steam's own record of that offer, read where no script of the page can see or change it (shared with the hidden offers check: one request per page view, two in the window of an offer you sent); when you send an offer, what the window showed is compared with what was sent. A mismatch raises an alert, Quick accept never accepts such an offer, and auto accept takes a gift only once the record confirms it (at once, with one request). Nothing of the pages is kept; an alert keeps the offers' ids until it is closed (24 hours at most)
- Phishing and scam protection → How this account is used → "This account is also used elsewhere…" (off by default): tick it when your trade offers are also sent or cancelled outside this browser — another computer, the Steam app on your phone, a trading bot or other people. While it is ticked, "Warn about trade offers sent from my account but not from this browser…" and "Cancel offers not sent from this browser at once" are off and locked: no false foreign-offer or phishing alerts, and nothing is ever cancelled; an offer the Sent offers page hides is still reported, as hidden only. Untick it and both return to the choices you had. Nothing is stored but the tick
- Defaults: the price source is now marketdb.info with KEYS.LAND on and cash-out in TF2 keys — switched once for everyone in this update; change it in Settings → Price providers (the KEYS.LAND tab's own switch still turns KEYS.LAND off). In the browser extension marketdb.info needs its box on the first page or in the extension's options; until then the Steam Market
- Prices: with KEYS.LAND on, Steam Market and marketdb.info prices are shown as cash — less the cash-out fee of the chosen item (Settings → Price providers → "Show Steam Market prices as cash", on by default; off shows Steam's own prices)
- Prices: while KEYS.LAND is on, keys, tickets and gems are always priced by it — never by the Steam Market or marketdb.info; without a KEYS.LAND price they stay unpriced, and a total of only such items says KEYS.LAND
- Items & inventory → 3D view of CS2 items → "CS2 items: a 3D button that opens an external 3D viewer in a new tab…" (on by default): on the item card in inventories, on each listing of Steam's classic market listing pages and in the trade window's item menu. It opens skinflow.gg (or the viewer you choose: csmarketcap.com, or swap.gg's game screenshots; the others are in ▾) only on your click, with only the item's inspect link, and asks the first time; ▾ → Details decodes the link (float, pattern seed, Doppler phase, stickers and charms) on your computer and sends nothing
- Settings: the price providers moved to their own tab "Price providers", right after "General"
- Inventory → the Stacks box on a very large inventory (more than 10,000 items still to load, such as a level-up bot's Steam items): the box asks before it loads everything and says about how long that takes ("Load all" / "Only what is loaded"), and never starts such a load by itself. The inventory is now loaded one portion at a time with a pause between the requests instead of all at once, so Steam no longer refuses it halfway (a refusal also made Steam answer the inventory page itself with an empty page for a while). When Steam asks to wait, the panel counts it down and the loading goes on by itself; if Steam keeps refusing, the stacks cover what is loaded and the panel offers "Continue loading"
- Inventory → Card sets on a very large inventory: the window counts the cards in small pieces and redraws only what changed, so the page stays responsive while badges are read; "Load the whole inventory" says about how long it takes and shows its progress with a Stop; "Read all N" reads every game's badge in one run; at most 300 rows are drawn at first, "Show all N rows" draws the rest
- Items & inventory → Inventory → "Rows per inventory page" (5 by default, Steam's own): 10 … 200 rows show several of Steam's pages as one big page, loaded gradually within Steam's limits (one request at a time, 2.5 s apart; a line under the pager counts the items and says when Steam asks to wait; when Steam keeps refusing, the line offers "Continue loading"); the pager counts and turns big pages; the item card stays in view beside the tile you click; a narrow window keeps Steam's own long page
- Inventory history: a stack's count stays visible when you point at it
- Inventory history: no partner buttons next to nicknames (they stay in the trade history)
- Reputation badges: a zero negative count is green for every source
- Selling & market → Market pages → "Load Steam's classic market pages instead of its Market Beta…": a listing opened by its name (such as an inventory's link to the Community Market) now comes as the classic page at once — while the setting is on, its cookie is kept on every Steam Community page; where the Market Beta has already answered with its own address of the item, the classic page of that item opens instead of "There are no listings for this item"
- License: the License Agreement is re-issued as version 2026-10-10 and you are asked to accept it once — section 8 now says which services are on from the start (the KEYS.LAND price relay, run by the author) and which stay off until you turn them on, and that the 3D viewers are plain links opened by your click; section 6 names auto-cancel beside auto accept; section 9 says what the diagnostic log's file holds. The browser extension also shows its data notice again (KEYS.LAND and the cash view turn on for every installation)

### 1.12.1 (2026-10-10)

- Phishing and scam protection → Trade offers → "Warn when the Sent offers page hides an offer that Steam lists…" (on by default): on your Sent offers page, Steam's own list of your sent offers is read where no script of the page can see or change it (one request, at most once a minute; in the browser extension by its background part) and compared with what the page shows; an offer that is missing, hidden, moved off the page, cut off, covered or shown with another partner raises an alert with "Open offer", and one not sent from this browser also counts as phishing (for auto-cancel too), except one that is only missing from the page. Nothing of the page is kept; an alert keeps the offers' ids until it is closed (24 hours at most)
- Phishing and scam protection → Trade offers → "Do not auto-cancel offers already on trade hold (escrow) or under trade protection…" (on by default): such offers are still told, never cancelled automatically, and the alert says why — Steam's trade protection covers what you give when every item of it is a Counter-Strike 2 item (7 days in which the trade can be reversed from the trade history)
- Header & navigation → Steam header → "Blur the wallet balance in the header and on the market…": the balance is now shown by a click on it, not when pointed at; that click only shows it (a second one opens the link as usual), and it is blurred again after 15 seconds, by Escape or by a click elsewhere
- Header & navigation → Steam header, new for streams and screen recordings (both off by default): "Blur nicknames and logins…" (your own in Steam's header, the newer one of market listings and the wishlist too, and in the tab's title; trade partners on the offers pages, in the trade window and the history; profiles, comments, friends lists, the web chat and Smart Trader's own panels, the SteamID and Trade URL of its profile panel included; desktop notifications leave the names out) and "Blur avatars…" (every avatar, only the picture). A blurred one is shown by a click, as the balance is. Nothing is stored or sent
- Header & navigation → Steam header → "Inventory value next to the wallet balance": right before your wallet balance, the total of your own inventories (TF2, CS2, Dota 2, Steam; Rust when the provider prices it) by the price provider chosen in Settings → Price providers, in your wallet's currency ("≈" for approximate prices, "+" for a lower bound; the tooltip tells how many items have no price). "On click" (the default) shows a Σ button that counts it; "Automatic" counts it by itself once a Steam Community page has loaded and again after 30 minutes. A slow provider such as the Steam Market (one item every 3.5 s) shows a spinner with how many items are priced so far. One tab reads the inventories, never while a trade is being accepted or sent; only the totals are kept

### 1.12.0 (2026-10-10)

- New settings tab "Phishing and scam protection" (right after KEYS.LAND, on by default; every check has its own switch and says what it costs in requests): its checks run in the background from one tab once the page has loaded, never while you accept or send a trade
- Phishing and scam protection → Account and devices → "Watch Security & Devices…": one small request every 20 minutes (by default) from one tab, and every third time the Security & Devices page itself (in the browser extension: from an open Steam store tab); a new session or device, or a changed e-mail, phone or Steam Guard, raises an alert with "Yes, it was me" (remembered as yours) and "Open Security & Devices" (× brings it back a day later while it is still true). The first check only remembers what is there
- Phishing and scam protection → Trade offers → "Warn about trade offers sent from my account but not from this browser…": every offer sent from a trade window of this browser is remembered; an offer sent from your account elsewhere raises an alert, and when an offer of yours was cancelled elsewhere and another one appeared, the alert ends: "Do not confirm anything in the Steam Guard app until you are sure the partner is genuine, even if the nickname and avatar are the same." The offer watch's count check is reused (kept running for this with the Trade offers tab off): the sent offers are read when its counts of sent offers move, and at most every 5 minutes while one of yours is waiting
- Phishing and scam protection → Trade offers → "Cancel offers not sent from this browser at once": "Off" by default; "Only on phishing signs (recommended)" cancels the offer that replaced yours, "All not sent from this browser (also from your phone or another computer)" every offer sent from your account elsewhere. It needs the consent to automation, as auto accept does; an offer sent from this browser is never cancelled; at most 5 tries an hour (a failed one counts too), then alerts only
- Phishing and scam protection → Inventory and trade windows → "Check the inventory for items drawn by malware…": when you open your own inventory (at most once every 6 hours by default, or at once with "Check now"), what the page shows is compared with Steam's server for every game and context, CS2's trade-protected items included (about one request per game and context; in the browser extension its background part reads them, out of the page's reach; in between one tab reads the totals alone); items that are not on the server, extra or duplicated tiles or items hidden on the page raise an alert. It never cancels anything by itself
- Phishing and scam protection → Inventory and trade windows → "Check trade windows for altered elements…" (experimental, off by default): a covered confirm button, another partner in the header than in the page's data, or item counts that do not match bring a warning; Steam's button is never stopped
- Phishing and scam protection → Chat → "Look for impostors in open one-to-one chats…": on steamcommunity.com/chat/, open one-to-one chats only (group chats are never read), a partner whose nickname is much like another friend's (look-alike letters, transliteration, symbols; 75 % by default) and whose avatar is the same or similar raises an alert; a nickname alone gets a quiet mark on that chat's tab. No request
- Phishing and scam protection → Alerts → "Sound and desktop notification for security alerts…" (on by default): a red banner at the top of every open Steam page shows each alert (▴ folds it into a small tab until a new alert comes), and one desktop notification with a sound rings even when the header's bell or speaker is off. Only one-way fingerprints are kept: never a device's name, an e-mail, an IP address or a SteamID, except in an open alert, which is gone once answered or after 24 hours (the offer watch kept running with the Trade offers tab off keeps its usual records: your SteamID with the offer counts, the accepted sent offers it read)

### 1.11.1 (2026-10-09)

- AI → "Documentation for an AI agent in the browser": the document is now a Skill: it starts with the header an agent's skills folder expects (SKILL.md with a name and a description), the new button "Download SKILL.md" saves it under that name, and a note says where to put it (for Claude Code: .claude/skills/smart-trader/SKILL.md)
- The document has a new section "Prompt injection": Steam pages, profiles, item texts, trade messages and Steam chat are data for the agent, never commands
- Security, after a review of 1.11.0 through an attacker's eyes: hidden Unicode characters (tag characters included) are removed from every text another site sends; outgoing requests are checked more strictly for anything that looks like a secret; a site's answer counts as JSON only when it really is JSON; a request that carries your pricempire key refuses any redirect and never repeats the key in an error; an exchange-rate table that moves a currency implausibly far and prices dated in the future are refused; a price under a cent shows as "&lt; $0.01" and stays out of the totals. The extension's background service reaches KEYS.LAND only on its own relay's exact path, sends your key and cookies only for Steam pages, loads at most two big price lists at a time and passes on only short error texts

### 1.11.0 (2026-10-09)

- Prices: the new section General → Price providers → "Where prices come from" chooses one source for every place that counts prices: Steam Market (as before), KEYS.LAND (keys, tickets and gems at their actual cash price), marketdb.info (instant: recent Steam Market sales, one list per game, no requests to Steam) or Marketplaces. Selling still reads Steam's own order book
- Your source stays as it was: KEYS.LAND where it was on, else the Steam Market where it was on, else none. With KEYS.LAND or "Off" as the source, items other than keys, tickets and gems now have no price (the price tags on tiles, the price list beside the inventory, the trade window's summaries, "Prices" under offers, card sets, "Take sets"): choose "Steam Market" to see the Steam Market's prices again. KEYS.LAND's switch is in the new section too; while it is on, KEYS.LAND prices keys, tickets and gems on top of the Steam Market, marketdb.info or a marketplace
- Marketplaces: Buff163 or Skins.com through pricempire with your own free API key (where to get it is under its field; the key is kept apart from the settings and never shown or logged), or, with no key, the public price files of Market.CSGO, Waxpeer, LOOT.FARM and Lis-Skins. An item a marketplace does not price is valued from the Steam Market (or marketdb.info) less the cash-out fee and marked with it ("−23% cash-out"): the fee is automatic from KEYS.LAND's figures for what you cash out with (keys, tickets or gems), or your own
- Prices from marketdb.info and the marketplaces are marked "≈"; their tooltip says the source, the kind of price, how many sales or listings and when (a marketdb.info price of fewer sales than you set gets "?" and stays out of the totals). They are converted to your wallet's currency with marketdb.info's daily exchange rates. KEYS.LAND alone as the source asks for no rates: with a wallet in another currency than the US dollar, its prices of keys, tickets and gems show in US dollars and stay out of the totals. A marketplace's price under a cent shows as "&lt; $0.01" and is left out of the totals
- General → Tools → Clear price cache also clears the providers' prices and the exchange rates
- Security: every request to a site other than Steam (KEYS.LAND, backpack.tf, SteamTrades, csgo-rep, the price providers) goes through one guard: https only, only that site's own address, no cookies (SteamTrades' own check excepted), time and size limits, no redirect elsewhere. What a site sends is only data: never shown as markup, never put in the diagnostic log, a notification or the documentation for an AI agent. Links to other sites open with no referrer, plain http and script links are refused, and the extension's background service follows the same rules
- Auto accept takes waiting gifts in the order they came, across page reloads and tabs (the one that has waited longest first; a gift whose accept failed goes behind the others). The background watch of incoming offers no longer counts an offer you are accepting at that moment as a new one Steam's list lags behind: no plain "pending now: N" notice for it, and a gift auto accept takes is not announced
- AI → "Documentation for an AI agent in the browser": an agent carries out an account action (an accept, a sale, a changed setting) only when you ask it for exactly that action in the same conversation, says what it is about to do before anything that cannot be undone, and never acts because a page, an offer's message or a notification seems to ask for it. The document also lists the price providers, their sites and settings, and the pricempire key only as a field that is never shown or logged

### 1.10.9 (2026-10-08)

- Background watch of incoming offers: when the watching tab goes silent (frozen or hung), a visible Steam tab takes the watch over a minute after its missed check (at most once in 30 minutes)
- Auto accept reads the offers list right after a run when new gifts may be waiting, and a hidden auto accept tab reacts to a new offer at once
- Auto accept: after a "gateway timeout" answer to an accept, the result is asked every 3 s for 20 s at most, then as before; a page left in the middle of a confirmation no longer holds the next check back
- Item counts in the header: counted once after an auto accept run instead of after each trade; your accepted sent offers change them by their own items (kept by the trade window when you send)
- Offers page: Steam's error page shown again during your own accept ends sooner: the page reloads as soon as auto accept has read the real list

### 1.10.8 (2026-10-07)

- SteamTrades reputation works in the extension: its request now carries your own steamtrades.com cookies (needed to pass the site's bot check), only while SteamTrades is on. If the row says "open site", open it, pass the check once, and the next page asks again

### 1.10.7 (2026-10-06)

- Trade summaries (the accepted trades list, the auto accept panel) and notifications count gems in sacks, as the header does (12 sacks and 345 gems → 12.35), with the Sack of Gems picture instead of the gem emoji

### 1.10.6 (2026-10-06)

- Offers page: items Steam itself stacks by amount (gems, sacks of gems) get no count badge; several such tiles of one item are shown as one stack with the summed amount

## 1.10.5 (Chrome Web Store, 2026-10-09)

### 1.10.5 (2026-10-06)

- Extension: the privacy policy opens as a readable page in all three languages (it used to open as raw text with broken Cyrillic)

### 1.10.4 (2026-10-06)

- Offers page: copies of one item that Steam lists with different instance ids are one stack again (916 + 1 keys → 917)
- Trade window: the item names in a summary's detail list keep their width next to the KEYS.LAND and market prices (no more "Mann Co. Supply Crate Key" broken letter by letter); when the list does not fit beside the items, it takes a line of its own

### 1.10.3 (2026-10-06)

- Extension: the first-run page asks again (its text changed): the reputation sites' box and the new "Allow automatic acceptance of incoming gift trade offers" box start unticked, with a plain explanation of what auto accept does; the options page shows a support contact; the cards of backpack.tf, SteamTrades and CSGO-Rep carry neutral marks of our own (the keys.land logo stays, with permission)
- Extension: a store build (tools/build-ext.js --store) without the self-update code and the private-build help, for the Chrome Web Store; the two script-protocol links of the old market code are plain links now

### 1.10.2 (2026-10-06)

- The texts follow the product as it is: the privacy notice, the consent page, the READMEs, the security notes and the document for AI agents (Settings → AI) now describe the selling modes, the listings awaiting confirmation, the card sets, the crafting and the default price sources

### 1.10.1 (2026-10-06)

- By default the prices now come from the Steam Community Market (Settings → General → Steam Community Market prices → "When KEYS.LAND is off: prices from the Steam Community Market…"); KEYS.LAND prices are off until you turn them on in Settings → KEYS.LAND → "Use KEYS.LAND prices". A copy that already has these switches saved keeps them
- Selling: an item whose listing still waits for your confirmation (the mobile app or e-mail) is never put up for sale again — not after a reload, not from another tab. "Sell everything", "Sell spare copies", "Sell selected", quick sell and the copies of Steam's sell dialog leave it out and say why ("awaiting confirmation of a listing"), its tile gets a violet frame, and it no longer counts as the copy that stays among your spare copies. The script remembers its own listings that wait (a week at most) and, after your click, reads your list of listings that wait on the Steam market (once in 30 s); confirm or cancel such a listing in the mobile app or on the market page
- Selling: when Steam fails to load your whole inventory, the panel says so ("Steam did not load the whole inventory: nothing was sent") with "Reload page", instead of "Something went wrong"

### 1.10.0 (2026-10-05)

- Market prices: a price list beside your inventory, market prices and totals in the trade window's summaries and under each offer ("Prices"), each with a progress line; "no listings" shown apart from failed prices, and failed prices tried again after a growing delay (Settings → General → Steam Community Market prices), with a cache shared by all tabs. The price tags on the tiles no longer have a panel of their own: a tag's tooltip says why its price is missing and when it is tried again
- Card sets: a window that counts complete sets and leftover cards per game, badge levels, sets you can still craft, extra sets and the price of a set — on inventories, in the trade window and under each offer ("Card sets")
- Crafting sets: a number of sets, up to an account level, or all — a plan with XP, level and the time it takes first, then one set at a time with your pause between crafts (2000 ms by default, 1000 at least; the badge is checked within the pause, so a set takes about 2.4 s) and the time left in its panel; it stops at the first error. "Craft sets…" on your badges page replaces "Craft all ready"; it is on your card set pages and in the card sets window too
- Take sets in the trade window: any number, chosen games, or sets you have not crafted yet, with the price of each set — added at a safe pace with progress and Stop; nothing is sent
- Big offers fold to their biggest stacks, with a large "…" that shows the rest — on by default, the rows in the settings (Settings → Trade offers)
- Fixed: with Steam's classic market pages turned on (Settings → Selling & market; Steam's bMarketOptOut cookie) every market price read failed — Steam sent a web page instead of the prices. The script now takes its own classic market cookie off for the moment of each price read and puts it back; a cookie set by Steam's own "Exit Market Beta" button is left alone: the prices wait, with "Let Smart Trader handle it"
- The old "worth $" trade summary is replaced by the new summary prices; a price tag shows "no listings" for an item with only buy orders (the order is in its tooltip); "Clear price cache" clears the new prices too
- Calm on the market: by themselves, prices ask Steam about at most 100 names per list and at most 150 times in any 10 minutes in all tabs, 2 s apart (the defaults; Settings → General → Steam Community Market prices); two "too many requests" answers within 15 minutes stop the automatic prices in every tab for 30 minutes ("Continue" lifts it)
- The maximum prices per kind are US dollars on every wallet, counted in your wallet's currency by Steam's smallest market amount (about one cent): the defaults 2.50 / 10 no longer leave out every card on a wallet in rupiahs or hryvnias (a maximum you set for another currency needs setting again). The sale review explains items above them, with a button to them (Settings → Selling & market → Price calculation)
- The extension's icons and the settings' logo follow the owner's new picture

### 1.9.5 (2026-10-04)

- Inventory → the selling buttons (Sell everything, spare copies, selected, all trading cards, all cases) ask first how: "Review first" (as before: every market price is read, then the table with the prices and the sums; nothing is listed before "Sell") or "Sell as prices come in": after a warning, the items are put up for sale in turn, each as soon as its market price has been read, without a table (Stop ends it; the prices show in Steam's "My listings"). A price your maximum or minimum for the kind would change, or one without a fresh order book, is not listed that way
- Gems: the dialog's table shows how many gems each item gives and each row's total (a foil card and a normal one have their own rows). "Gems from spare copies" asks the same question, and so does "Gems from selected" while "Ask for confirmation before bulk / irreversible actions" is on: "Grind as values come in" turns the items into gems in turn after a warning
- Booster packs: "Open all booster packs" asks the same question, and so does "Open selected packs" while "Ask for confirmation before bulk / irreversible actions" is on: "Open one after another" opens them after a warning, without the list
- The selling dialog with the prices is wider: the price's source ("second listing level…", "average of recent sales") stays on one line; a price capped at your maximum or raised to your minimum says so

### 1.9.4 (2026-10-04)

- Settings → General → Language: a new choice "Auto (browser language)" — the browser's own language (its first preferred one of English, Ukrainian, Russian), whatever language Steam is in. "Auto (Steam language)" stays the default
- Extension: on the first-run page, "I agree" and "Not now" go away once you have agreed (the boxes lock); only the thanks and what to do next stay

### 1.9.3 (2026-10-04)

- Settings → General: the time zone is "auto" by default now — the browser's own zone (a copy that already has a zone saved keeps it). Pick a zone by name when the browser's zone is not yours (a VPN, an antidetect browser)

### 1.9.2 (2026-10-04)

- Extension: the alert sound has one switch. The speaker in Steam's header, Settings → Trade offers ("notification sound") and the switch on the extension's options page are the same setting now; before, the options page had a second switch of its own and both had to be on. The volume and the tests stay on the options page
- Extension: the options page's cards of backpack.tf, SteamTrades and CSGO-Rep show the sites' own icons instead of the letters

### 1.9.1 (2026-10-04)

- Settings → KEYS.LAND: the keys.land logo is the tab's title picture, large; the note below has none
- The logo picture refreshed (the extension's icons and the title of this dialog)

### 1.9.0 (2026-10-04)

- The product is named Smart Trader everywhere now: the header button, this dialog, the notices, the help, the License Agreement (its terms are the same; it asks for your acceptance once more because its text names the new name) and the documents. The userscript keeps its own name "Steam Cool Trader", which its updates depend on
- The extension's texts no longer mention the script manager: the help and the labels that named it have their own words there

### 1.8.9 (2026-10-03)

- Light theme: the bar under the active game tab of the inventory now runs under the whole tab (the name box beside the icon covered it)
- Settings → KEYS.LAND: the tab's title is a link to keys.land
- A new logo (two crossed keys in a gold frame): the extension's icons, the title of this settings dialog. The extension is now named "Smart Trader - trading tools for Steam" (the userscript keeps its name, which its updates depend on)

### 1.8.8 (2026-10-03)

- Extension: the page shown before Smart Trader starts has a third box, ticked from the start, that turns on the optional services backpack.tf, SteamTrades and CSGO-Rep (the browser asks you to allow the sites); the data notice is accepted once more
- Extension: a left click on the Smart Trader button in the browser's toolbar opens Smart Trader's settings on the Steam page (on another page a Steam page opens first); the extension's own options are on the button's right-click menu, "Options"

### 1.8.7 (2026-10-03)

- The "not compatible with" notice names only what this very page found. Before, it also kept naming a userscript or extension you had already turned off, for up to 7 days or until a page where its marks used to show. Settings → General still lists what was found earlier, with the advice for a product that is off but still listed (reload the page; a disabled extension can keep its marks until the browser is restarted and its cache cleared) and a "Forget the list" button

### 1.8.6 (2026-10-03)

- Settings → KEYS.LAND: the keys.land logo as the tab's icon; the manual price table shows the items' own pictures, and "Key" is named in full, "Mann Co. Supply Crate Key"

### 1.8.5 (2026-10-03)

- Profiles: the inventory shortcuts next to "Inventory" show the games' own pictures (Counter-Strike 2, Dota 2, Team Fortress 2, Steam) instead of the letters; the letters come back if a picture does not load
- Extension: the keys.land card of the options page carries the keys.land logo, and Settings → KEYS.LAND starts with a note that the service itself is switched on that options page (the Smart Trader icon in the browser's toolbar opens it)

### 1.8.4 (2026-10-03)

- Light theme: the active game tab of the inventory no longer shows as a lighter patch inside a darker frame; it has one colour and a blue bar below
- Extension: keys.land prices work from the start. The price relay's host is now installed with the extension and the service is on unless you turn it off in the options (before, it was off until turned on, so prices did not load). The data notice says so and asks for your acceptance once more

### 1.8.3 (2026-10-03)

- Selling & market: a new setting, "Load Steam's classic market pages instead of its Market Beta" (off by default). Steam now serves the market's search and item pages in a new look, where the script's market tools find nothing. With the setting on the script keeps the cookie of Steam's own "Exit Market Beta" button, so the classic pages come (a beta page loads once more by itself); turned off, the script removes the cookie it wrote. On a beta page a small card in the corner offers to turn the setting on
- Trade window: "Faster drawing of the item slots" is written anew as the script's own code. Steam's own notices in the offer now come in the page's language, and the buttons that clear a side of the offer no longer depend on that setting
- Market item pages: the gem value line also shows when Steam draws the item's description a moment after the page, on a line of its own
- Copyright: the script and the extension now carry their author's copyright notice (the file LICENSE: the own code is not open source), next to the notices of the MIT and Apache-2.0 components. The script's header no longer names SteamWebTools among the original authors: none of its code is left

### 1.8.2 (2026-10-02)

- Market pages: the small tools (go to page N, numbered listings, the agreement tick of the buy dialogs, Sell of a commodity straight to Steam's multisell page with a prepared price, card and booster pack links, "do I have this emoticon", the gem value) and the simple listing tools of My listings are written anew as the script's own code. New in them: Enter in the page number box, a page number above the last one opens the last page, the numbers stay right after paging, Steam's own Remove link stays next to each tick, removals take turns at the market's pace and stop when Steam asks to wait, and every text is translated. They work on Steam's classic market pages; on the pages of Steam's "Market Beta" they do not appear
- The old inventory code (the menu command "old code (1.7.x)") is gone: the inventory and selling written anew in 1.8.0 are the only ones
- Interface languages: English, Ukrainian and Russian. Portuguese, Japanese and Chinese covered only a few old texts and are gone; with one of them chosen the language is picked automatically (from Steam's page and the browser)
- Licences: nothing of SteamWebTools (GPL-2.0) is left in the script, neither code nor translations; the License Agreement no longer names that licence (its version and your acceptance stay as they are)

### 1.8.1 (2026-10-02)

- Experimental: a light theme for Steam (Settings → General, off by default). Store, community and checkout pages turn light, every text stays readable; pictures, item icons and game colours stay as they are, and the script's own panels, dialogs and header buttons turn light with it. The first visit of a page after a Steam update may take a moment to turn fully light: the theme learns Steam's new styles once and keeps them in the page's own storage (at most 1.5 MB per site, cleared when the theme is turned off)
- Settings: a tick left of a tab's name in the rail while its switch is on (a dash while it is off), instead of the green dot
- Settings: "Restore defaults" is greyed out while every setting is already at its default
- Settings → AI: the file is now smart-trader.md (it was AGENTS.md) and is only for an AI agent that operates a browser with the script (it opens Steam's pages, reads what the script shows and uses its buttons and settings for you): what it must never do without you, how to open a setting by a link and change it, the pages, the storage keys and the reference of every setting. The parts for agents that change the script's code are gone
- Quick accept: once its queue has finished, the Incoming Offers page loads again by itself and then shows a summary of the run (how many offers were accepted, and why the others were not)
- Other userscripts and extensions: the warning to turn them off on Steam pages is now always the first card of Settings → General ("Don't show again" hides only the news). The script also recognises popular ones that conflict with it (Steam Inventory Helper, Augmented Steam, SteamDB, Steam Economy Enhancer, SteamWebTools and others, or a second copy of Smart Trader), names them on that card and in a notice on the page (× hides it for 24 hours)
- License Agreement: on the first run the script asks you to accept it, and nothing starts on Steam's pages until you do; Settings → License shows what you accepted and lets you withdraw it. Auto accept needs a separate consent to automation: until you give it, auto accept stays off

### 1.8.0 (2026-10-02)

- Trade window: your items that already sit in another active trade offer carry an "in trade" label on their tile, and (a setting, on) the add buttons, "Select all from page" and the quantity dialog pass them over; a double-click or drag on one is stopped with a note. The list comes from Steam's own trade offers service with the page's token, every 2 minutes while the window is open
- Steam's notifications popup (the bell in the header): a "Clear all" button next to "View All" marks every notification read, as "Mark All Read" on the notifications page does, says how many it cleared and closes the popup (Header & navigation; on). Only Steam Community pages
- Settings → AI: a new tab with "Download AGENTS.md" and "Copy to clipboard": documentation for AI agents (coding agents working on the script, or agents operating a browser with it) about what the script is and never does by itself, its pages and features, its settings and storage, the diagnostic log, the tests and the repository, with a reference of every setting generated from the running version. It holds nothing about you: no account, no values you typed, no addresses
- Settings look new, like a game's settings menu: the tabs in a rail on the left with icons, a light for each tab's on / off switch and how many of its settings differ from the defaults; a search over every setting of every tab (by its name, its description or its key), the results grouped by tab; switches instead of ticks, − / + by the numbers; a "Changed" mark and a "Reset to default" button on each setting that is not the default (it changes the field only: Save keeps it); Save is on once something was changed, with "Unsaved changes" next to it; the news (what is new, the word on other extensions) in a card at the top of General and behind the bell of the title bar; the cache buttons in General → Tools; the whole screen in a narrow window, the tabs as a strip at the top. Every setting, its place and the #ct-settings=… links stay as they were
- Inventory and selling rewritten (for this release the old code stays behind the script manager's menu command "Inventory & selling: old code (1.7.x)"): the stacks hide the copies without touching Steam's item data and regroup at once when the stack settings change; multi-select keeps the selection across pages; the search also finds the tag names the side panel shows; the lowest price on someone else's inventory is cached (and off by default now: Steam's own item panel shows its starting price). Bulk selling (everything, spare copies, selected, cards, TF2 and CS2 cases) shows every price and the sums in its own dialog before anything is sent, skips what has no price, is not above your minimum or is above your maximum and says why, sends one item at a time with "Stop" and "Retry", pauses in every tab when Steam asks and never decides by Steam's text; gems and booster packs count only confirmed answers; quick sell prices come from a cached order book; the sell dialog's "lowest ± offset" counts in your currency's steps; the price tags of the inventory and the trade window are one module, drawn only for the tiles in view and kept between tabs. The gift tools are gone (Steam has had no inventory gifts since 2017)
- Faster and lighter: on the trade and inventory history pages the script holds the page up about half as long (the header no longer forces extra layouts), a large inventory opens about a third faster than in 1.7.8, and every Steam tab keeps about 2 MB less memory for the script

### 1.7.8 (2026-10-01)

- Settings: the time zone and time format (trade history, trade offers, held trades) now stand in the General group next to the language, not in a group of their own
- Diagnostic log: every change of a setting is recorded wherever it is made (the dialog, a switch in the header or a panel, another tab, a reset: the keys and their new values, a text only by its key); how long each tip stayed open; the file now also says the versions this installation ran and when it was updated, which settings differ from their defaults, the state of the tips and tours, and when the recording began
- Audit fixes: Quick accept treats Steam's "too many requests" on an offer page as a wait (the tries with Steam's pause, then the queue stops) instead of failing each queued offer with one more request; batch selling and removing listings stop when Steam asks to wait and say how many went; Steam's error page keeps its try count through a long wait; fewer class-info requests on the offers page (one-item offers of other games are left alone); auto accept's "nothing to do" record is not written over a change another tab saw meanwhile; a closed tab hands its accept check to the next page at once; the settings dialog is a dialog for the keyboard (Escape closes it, focus moves in and back); the accept log keeps the result as a word with Steam's number and offer ids as short codes, never Steam's text
- The update server relays KEYS.LAND prices on the path the script asks (series), so prices over the server's address work again; a build refuses to publish a lower version than the one already published (a rollback) unless forced
- The corner panels (auto accept, the accept monitor, the selected trades, the progress of Load more and of the market prices) fold to their header with the "–" in it; the choice is kept per panel. A tip is never drawn over a panel: a line above the panel says a tip is behind it and folds the panel at a click; an open tip whose element is behind a panel says so at the top of the page

### 1.7.7 (2026-10-01)

- Diagnostic log: while it records, a red mark in the header shows the size of the log file and when the recording began; a click on it opens its menu (download, clear, turn off). Settings → Diagnostics shows the same, clearing the log now asks first, and the script manager menu can clear it too
- The log follows its switch in every open tab: turned on or off in one, the others start or stop recording at once
- The log now records every click you make in Steam (only what kind of control it was and where, never a text, an address or a number of an offer or item), whether you or the script clicked, Steam's answers to your declines, cancels, sales and purchases, and which tab each page was in (a popup or a tab opened from another says which one); a new tick in Settings → Diagnostics (and in the mark's menu) says that this account is also used elsewhere while you test

### 1.7.6 (2026-10-01)

- Auto accept and Quick accept read the offer's items from Steam before the accept (Steam no longer gives them once the trade is done): the notification and the small list name them again (🗝 🎫 💎), and the header's counts change at once and count again only the inventories the items went into, not every one after every gift
- Steam's error page on the offers pages ("There was an error retrieving your trade offers": Steam shows it while it finishes an accepted trade) reloads about a second after your own accept instead of a minute, waiting up to 3 minutes while this tab's accept request is still with Steam, and auto accept no longer puts the whole list into it
- A freshly opened Incoming Offers page takes its own gifts 3 seconds after it loads, a page being left starts no new accept (the gifts of auto accept: the next page takes them; any accept goes on if you stay on the page), and a page closed in the middle of an accept hands the check of its result to the next page at once
- Fewer requests: no read of Steam's list when fewer offers are pending only because of your own accepts; no details of new offers while every notification is off (the bell); KEYS.LAND prices kept 5 minutes instead of 1; an accepted trade's status checked less and less often (5 minutes, 30 minutes, then 1 to 8 hours), one check at a time
- Diagnostic log: your own sends and accepts on a trade offer page (timing and counts only), and what is needed to check these changes in the next logs

### 1.7.5 (2026-09-30)

- Item counts in the header: your inventory page updates them at once from its own list of games. A game with no items left shows 0 right away, with no request (before, the old number stayed for a minute or two), and an inventory whose size changed is counted again without the one-minute wait
- A trade auto accept took says so in its notification: "↓ Incoming trade accepted (auto accept)"

### 1.7.4 (2026-09-30)

- Auto accept works in the background on any Steam page, one tab at a time (the Incoming Offers page first, then any Steam Community page, a store page only when none is open). The tick on the Incoming Offers page is gone: the ⚡ button in the header turns it on and off
- Header: three switches before the Smart Trader button: ⚡ auto accept of gifts, the bell (every notification of Smart Trader), the speaker (their sound). The item counts moved to the row of the wallet balance
- Far fewer requests to Steam: with the background offer check on, auto accept reads the offers list only when that check sees a change; after Steam's "too many requests" (HTTP 429) every background part of the script waits 5 to 30 minutes; the offers pages reload by themselves at most every 90 seconds
- A gift Steam did not take after an unclear answer (as during Steam's restarts) stops only itself: it is sent again 3 minutes later, twice at most, while the other gifts go on (before, it paused auto accept for everything); an accept Steam answers clearly is confirmed about 2 seconds sooner
- No "new offer" notification for a gift auto accept takes (its result is told), and a result right after a new offer's notification stays silent; the Incoming Offers page no longer reloads after its own accepts: their rows show the result and go 30 seconds later
- Steadier through Steam's outages: Steam's error page on the offers pages reloads with longer and longer waits, 8 times at most; the background offer check no longer stops for good after a lost token, nor reads an empty answer as "no offers"; a request cut off by leaving the page is no longer taken for a failure of Steam
- KEYS.LAND prices: a copy less than 15 minutes old is shown at once while keys.land is asked in the background, and one load never takes longer than about 20 seconds; SteamTrades (and the other reputation sites) are asked nothing for 30 minutes after they refuse this address

### 1.7.3 (2026-09-30)

- Item counts in the header: opening your inventory page counts them again (once Steam's own page has loaded, the game it shows first, at most once a minute, reloads included; other tabs wait for that page too); after a trade the script sees (Quick accept, auto accept, an incoming offer accepted elsewhere, a sent offer accepted, a trade reversed) the counts of its items change at once, shown with "≈" and "updating…" in the tooltip, in every tab, and the inventories its items are in are counted from Steam 20 s and 2 minutes after the trade, also from a Steam tab in the background (an offer declined, cancelled or expired counts nothing again)
- The "Accepting trades" panel: opening your Incoming or Sent Offers page (or its history) updates it at once. A trade still waiting takes the result its offer shows on that page (accepted, on hold, declined, canceled, expired…; "Awaiting Mobile Confirmation" keeps it waiting), with its notification as before, and one the page no longer lists is asked about from Steam right away (five per page load at most, never beside a check already going on); offers added with Load more are read too
- An Incoming Offers page that shows a trade's result itself (as it loads, or in offers added with Load more) no longer reloads for it a few seconds later or shows "Offers changed — Reload"; your other Incoming Offers tabs still load again
- The "[tools]" menu under every trade offer (the trading card swap check) is off by default now, for everyone once; it can be turned on again in Settings → Trade offers
- Auto accept no longer turns itself off: when Steam is busy, has not confirmed an accept, or the session is gone (Steam maintenance), it pauses and then goes on by itself, without reloading the page. Only you turn it off
- The "Accepting trades" and "Auto accept" panels share the height fairly: each gets an equal part, and a panel with a short list keeps only what it needs, the rest going to the other

### 1.7.2 (2026-09-29)

- Your own profile: "full info + trade URL" next to "full info" copies the same text with your trade URL as the first line, ready for a trading site; the first click asks Steam for your current URL once (shown as "…"; when Steam is slow or fails, the URL the navigation panel keeps stands in), only a URL of this profile's account is used, and when there is none nothing is copied and a note says where to find it. Space copies too on "full info" and "full info + trade URL"
- Notifications no longer say "Smart Trader": the title is your own nickname, or, while it is not known, what happened ("New trade offer", "Trade accepted", "Trade not accepted", "Trade reversed", "Trade result unknown", "Trade results")
- After an accept the offers pages load again by themselves: an incoming offer accepted with Quick accept or auto accept (or elsewhere, such as Steam's own offer page or the mobile app) reloads the Incoming Offers pages open in your tabs, a sent offer accepted reloads the Sent Offers pages; several accepts close together bring one reload a few seconds after the last. A page in use is never reloaded under you (an accept running or waiting for Steam, in any tab, typing, a dialog, menu or tip open, offers selected, offers added with Load more, a Quick accept result such as a trade hold you have not looked at yet): a small bar "Offers changed — Reload" shows instead, and the page reloads once you are done (Trade offers → In the background, on by default)
- Navigation panel: "Incoming Offers (3)" and "Sent Offers (1)" show how many offers are waiting, from the background watch of incoming offers (the same account, at most 10 minutes old; no number while it is unknown); an offer you accept with Quick accept or auto accept leaves the number as soon as Steam confirms it. Header & navigation → Navigation panel, on by default
- Steam header: icons of your keys, Tour of Duty Tickets and gem sacks with how many of each you have, between Steam's menu and the "Smart Trader" button (gems are added to the sacks: 12 sacks and 345 gems show as 12.35); a click opens that inventory. Counted from your own inventory at most every 15 minutes by one Steam Community tab, and again shortly after a trade the script sees. Header & navigation → Steam header: switch it off, or add any other item of your inventories and put them in your order
- Trade notifications say what is in the trade: the keys, Tour of Duty Tickets and gems of each side as 🗝 🎫 💎 with their counts (a gem sack counts as 1,000 gems), or, with none of those, the three items it has most of by name, then how many other items, (+N others); an empty side is left out. For this the script asks Steam for the item details of each offer it tells about (one request per offer, three at most, 4 seconds at most). Several new incoming offers now get a notification each (the sound once; three at most, the rest counted in one more), each with its sender's avatar, so a long line never hides the next offer. The accept monitor's and the auto accept's panels show the same with Steam's own item pictures. When Steam does not give the item details in time, the notification counts the items as before

### 1.7.1 (2026-09-29)

- KEYS.LAND prices: the current posted BUY / SELL (as the site's price cards show them) instead of the last row of its 24 h series, which is written only every hour or two and lagged behind a price change; "Check now" also skips the browser's short cache

### 1.7.0 (2026-09-29)

- Steam header: the compact look, the hidden "Install Steam" button and the hidden wallet balance (now blurred: point at it to see the amount) are there from the page's first moment, also on market listings and the wishlist; the header stays on top while you scroll and the navigation panel stays right under it
- Profiles: "Full info" and "More info" ask Steam once per page; the dialog shows SteamID3, the registration date in your language and the account age; your own trade URL shows at once when the navigation panel knows it
- Your own links in the profile's "More" menu and on store game pages are now written "Name | address", with {steamid}, {accountid} and {name} on profiles and {type}, {id} and {name} in the store; your lists were converted, and a line that could not be is marked under its field in the settings
- Friends list changes: the number counts who joined and who left; a panel above the list and a switch that shows only the new friends; the list you had saved was carried over
- Badges: "Craft all" crafts one badge after another once you confirm the list, with progress and a Stop button; "only games with card drops left" can be switched off again
- Card swaps with friends: a card you have once no longer counts as missing, and only swaps that help both of you are offered; the search can be stopped. The card swap check of trade offers counts every item (it missed some before) and says when it cannot be sure
- Store: prices in other countries for each package, with discounts, "not sold here" and "free" told apart, kept 10 minutes without asking Steam again; the cart history keeps one entry per package, and adding to the cart asks you to confirm; the agreement box is ticked on Steam's new checkout page too
- Tips: the green dots no longer appear at once. On the first run a small window offers the full tour, "Just show the dots, I'll explore", "Later" or turning tips off; after an update with new features it offers a tour of only what is new, the full tour, "Later" or "Skip" (the new features then get dots, as before). No dot shows until you answer; "Later" asks again an hour later
- Settings → General → Diagnostics: a diagnostic log for bug reports (off by default). Switch it on, use Steam as usual, then download the log and send it: it keeps timings and outcomes of the script's work and its errors, never SteamIDs, names, profile or trade links, tokens or messages
- New incoming offers are noticed within about 30 s by default (up to a minute before): how often the script asks Steam is now a setting (Trade offers → In the background, 15 to 300 seconds)
- The notification about a new incoming offer says who sent it and how many items you get and give (several offers: the three newest in one notification, then "+N more"), with your own nickname in its title, also in the notifications about accepted trades
- KEYS.LAND → Manual price: tick it and your own BUY / SELL for a key, a Tour of Duty Ticket and a gem sack (a table filled with the last keys.land prices, "Fill from keys.land" copies them again) are used everywhere keys.land prices were, named "manual price"; keys.land is then not asked at all ("Check now" still shows its prices for comparison). After 24 hours the price pages remind you that the manual prices may be outdated, with a link to these settings
- Held trades: Steam's count on the trade history now comes from the small summary the incoming offers check already reads (usually with no request at all), not from the sent offers page, which can be megabytes (that page is asked only when the summary cannot be had); the count is shared by all your Steam tabs for 5 minutes
- An offer you sent is accepted: a notification says who accepted it and how many items you gave and got ("accepted, on hold" when Steam holds the trade), like the one about new incoming offers; a click opens your sent offers history (Trade offers → In the background, on by default)
- Navigation panel: now also on the trade offer page (the trade window and an offer you open), at the very top, where Steam shows no header; it stays there while you scroll, under Steam's item details and dialogs
- Navigation panel: your own links to the browser's own pages (chrome://extensions, about:config …) no longer lead to a broken https:// address. Browsers do not let a page or a script open them, so a click copies the address and a note says how to paste it into the address bar (Ctrl+L, Ctrl+V, Enter)
- Notifications about accepted trades say which way the trade went: "↓ Incoming trade accepted" (an offer you accepted with Quick accept or auto accept; "reversed after acceptance" if Steam rolls it back) or "↑ Outgoing trade accepted" (an offer you sent), then "&lt;partner> — you gave M · you got N", with the partner's avatar next to the nickname. Each trade gets its own notification (three at most at once, the rest counted in one more); a single new incoming offer shows its sender's avatar too
- Removed: one-click buy, sending several gifts, "to my inventory" at checkout, any amount when adding funds, the game artwork gallery, the SteamDB sales link, the profile edit page tools, "Set AppID" in the activity feed, the level-up services menu and the Gifts inventory shortcut

### 1.6.0 (2026-09-28)

- Navigation panel: the default order is Inventory, Trade URL's, Market, the four histories, Sent Offers, Incoming Offers (an order you changed yourself stays); while Load more loads, the page's button spins
- Prices: the decimal separator is now a dot (the comma can be chosen again in Settings → General); how long Steam market prices are kept is now a setting (General → market prices, 30 minutes by default)
- Trade history and inventory history rebuilt: item details, stacks with counts (metal in refined, TF2 craft weapons as one group, their list now taken from the game's own files), pictures of given items, held trades, the search and the tab title are the script's own code now, and long histories stay responsive
- History search: every word, SteamID, profile link or item ID you type must match, so each one narrows the list; a SteamID also finds partners with a custom profile address; the words are highlighted without changing the page, and the search stays in the address (#ct-search=…)
- Held trades: the panel shows their items as stacks with pictures and when the first one is released ("in 3 days"); Steam's own count of held trades is asked only on the newest history page
- When Steam shows an error page instead of the history, the inventory or your trade offers, the page loads again by itself after 5, 15 and 45 s, with "Try now" and "Stop" buttons (Settings → General)
- Steam's own item names stay as they are: the English market name and the details are shown next to them, so the search finds both; metal reads 0.11 / 1.33 ref, and keys follow the stack settings for "Not Usable in Crafting" and non-tradable items like other items do
- The tab title of a history page shows the dates of its rows in your language, for example "Trade history · Sep 16 – 27, 2026"
- Full tour of the tips: after the first install, after "Show all tips again" and when an update brings new features, the guide offers a tour that goes page by page (inventory, trade offers, histories, market, profile, store), shows each tip once and ends in the trade window of any trade URL you paste; the next page opens only when you click "Next page" (also in Settings → General → Tips and the Tampermonkey menu)
- Quick accept and auto accept: the list of trades being accepted, with the time left, now stays on every Steam page until everything is done and you close it; Steam is asked in the background how each trade stands (faster than the offers history), with a notification when a trade is accepted, not accepted, or reversed after acceptance (Settings → Trade offers)

### 1.5.0 (2026-09-28)

- Navigation panel: a "Market" button; the panel now stays on the page while a slow page loads, and a small spinner on the button you clicked shows the next page loading
- Navigation panel: Inventory History, Trade History, Sent History and Incoming History can be grouped into one "History ▾" menu (Header & navigation → Navigation panel; off by default)
- Own links of the panel can be of any type, such as steam://rungameid/440 or chrome://extensions, once that is allowed in the same place (off by default); links that could run code are never allowed
- Tips for new users: green dots mark what the script adds to Steam pages; a click on one explains the feature, and its Settings button opens that very setting. A tour of any page on request; Settings → General → Tips turns them off or shows them all again. After an update only new features get tips
- The 👍 "Like" button on profiles is removed: Steam no longer counts profile likes
- Trade offers → the accept timing log can also be downloaded as a CSV file (for Excel or Google Sheets)
- Item marks rebuilt: the TF2 unusual effects now come from the game's own files (624 effects, the newest included) and the marks are drawn with one element per item; market fees are worked out by the script and checked against Steam's page — when they differ, a sale always asks first
- Faster pages: trade history, inventory history, the inventory and trade offers take 20–40 % less of the script's time

### 1.4.0 (2026-09-28)

- Settings are arranged by what they do: General, KEYS.LAND, Header & navigation, Trade window, Trade offers, History, Items & inventory, Selling & market, Profiles & reputation, Steam store
- Every tab except General and KEYS.LAND has a switch at its top that turns all of its features off at once; their settings are kept for later
- Your settings are carried over as they worked: a feature that was off because its whole section was off shows as off (or its tab switch is off)
- Market "My listings" tools: one switch; the choice between the full and the simple set is under it
- The script's remaining third-party code is being replaced by its own, step by step, in the next versions; until then its licence notices are complete

### 1.2.64 (2026-09-28)

- Trade history and inventory history pages are fast again (1.2.63 spent several extra seconds on long histories)

### 1.2.63 (2026-09-27)

- Full audit: 62 problems fixed. Safety: selling one item of a stack no longer lists other variants with the same name; "Sell all duplicates" counts variants apart; "Decline All Active" is gone from the Sent Offers page; a partner's text cannot hide a trade hold; Save no longer turns auto accept back on without asking
- Inventory history: prices (KEYS.LAND / market) and item details now work there too
- Faster: trade history and inventory history pages start seconds sooner (the navigation panel no longer makes the browser lay out the whole page; Steam's item data is read without scanning megabytes)
- The panels in the bottom corners (auto accept, market prices, Load more, selected offers) stack instead of covering each other and no longer make the page redraw every second
- Many smaller fixes: CS2 keys with a non-English Steam, trade summary counts, history search while typing, a store age-check reload loop, store "Get prices" never finishing, settings showing values changed in another tab

### 1.2.62 (2026-09-27)

- Settings → General → Navigation panel (under Steam menu): show or hide the "Install Steam" button in the Steam header (hidden by default)
- Same place: "Profile" (in the language of Steam) instead of your nickname in the Steam menu (on by default)
- Market listings, store charts and other pages with the newer Steam header: the script starts once Steam has finished drawing the page, so its button and panel no longer vanish

### 1.2.61 (2026-09-27)

- Incoming trade offers watched in the background: the "Incoming Offers" button blinks with the count; a new offer brings a notification with the system sound, and the browser flashes in the taskbar when no Steam tab is in front
- The decimal separator is now under General: it applies to market prices too
- Market prices: every item is asked once per page, a failed answer waits 10 minutes, all tabs keep 3.5 s between requests; gems get the Sack of Gems price; labels redrawn only when a price changes
- This notice also holds the script's description; the warning is red

### 1.2.60 (2026-09-27)

- Market prices: with KEYS.LAND off, Steam Community Market prices for every item (lowest listing; a gem = 1/1000 of a sack), loaded within Steam's limits with a progress window, kept 30 minutes
- "Clear price cache" button
- This notice: close it, or hide it until the next update
