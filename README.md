# twitter-ivermectin-pharmacies
geotracking disinformation by foreign pharmacies claiming to be based in the US

## Background


## Methodology
* Identified accounts selling ivermectin products using the search term "ivermectin"
 * Search performed on 11/24/2025
* Compared stated location with actual location provided by Twitter --> identified many pharmacies that claimed to be based in the US, but were in fact based abroad (particularly India)
* For each store, compared the URL --> identified multiple accounts that link to same account --> was able to identify additional fradulent accounts this way
* Traced the information about each store using `WHOIS` --> was able to identify additional fraudulent accounts, also found several that tried to hide thier location

## Results
### Summary data
Actual Location Counts:
India: 58
United States: 2
Nigeria: 2
Germany: 1
South Asia: 1
South Africa: 1
(Blanks: ~35)

| Metric                                | Value              | Notes                                                                                                                                |
|---------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Total Accounts                        | 99                 | Includes header row; all appear to be Ivermectin-focused sellers.                                                                    |
| Verified Accounts                     | 28 (28%)           | YES: 28; NO: 71. Verified ones are more concerning for fraud reach.                                                                  |
| Accounts with Actual Location = India | 58 (59%)           | Dominant origin; 22 of these honestly claim India.                                                                                   |
| Suspected Fraudulent Accounts         | 27 (27%)           | Defined as Actual: India and Claimed: US/UK/US state (e.g., "USA", "United States", "California"). These pose as Western businesses. |
| Verified Fraudulent Accounts          | 10 (37% of frauds) | Verified scammers: e.g., @getivermectins, @IvermectinShop.                                                                           |
| Accounts with Blank Actual Location   | ~35                | Incomplete data; could hide more fraud if investigated.                                                                              |

### Fradulent accounts identified
* How many accounts fraudulently claim to be in the US, but are in fact based in India?
  * → 40 (93% of everything that pretends to be American)
* How many did we discover purely thanks to the WHOIS + redirect investigation?
  * → 13 additional fraudulent US-claimers that were not yet flagged in based on Twitter provided location

| Category                        | Count | Examples (Handles)                                                                               |
|---------------------------------|-------|--------------------------------------------------------------------------------------------------|
| Claimed: USA/United States      | 16    | @getivermectins, @IvermectinShop, @Medicine_Villa, @Ivermectin12hUS, @Ivermectin__US             |
| Claimed: Specific US State/City | 7     | @Allhealthdrugs (California), @_GetIvermectin_ (USA but state-like), @Ivermectin_cell (New York) |
| Claimed: UK                     | 2     | @IvermectinRx (UK), @BIvermectinUK (implied via name)                                            |
| Verified Among Frauds           | 10    | @getivermectins, @IvermectinShop, @skymeds_store, @medicine_kart, @Ivermectin_Dose               |



| Category                                                                                                                             | Number of Accounts | % of Total                          | Notes                                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------|--------------------|-------------------------------------|-----------------------------------------------------------------------------|
| Total accounts                                                                                                                       | 99                 | 100%                                |                                                                             |
| Claim to be in the United States (any variant of "USA", "United States", "California", "New York", "Denver", "Florida", etc. in bio) | 43                 | 43%                                 | These are the ones explicitly pretending to be US pharmacies                |
| Fraudulent US-claimers (claim US but are provably not in the US)                                                                     | 40                 | 40% of total 93% of all US-claimers | All evidence points to India (or Nigeria/South Africa in a couple of cases) |
| Actually based in India (either you marked Actual_Location = India or WHOIS = IN or both)                                            | 71                 | 72%                                 | This is the true operational base for the vast majority                     |


### Impact of fraudulent accounts
| Metric                        | All Accounts (99) | Fraudulent US-Claimers (46) | Non-Fraud (53) | Verified Accounts (28)  |
|-------------------------------|-------------------|-----------------------------|----------------|-------------------------|
| Total Followers               | ~170,000          | ~140,000 (82%)              | ~30,000        | ~110,000 (65% of total) |
| Average Followers per Account | 1,717             | 3,043                       | 567            | 3,929                   |
| Median Followers              | 97                | 157                         | 81             | 2,002                   |

### Top 5 misinformation accounts
* @skymeds_store (43k followers)
* @_Ivermectincure (16k)
* @Ivermectin_net (13k)
* @24Medico__ (6.6k)
* @Apotheke_Store2 (6.4k)


## Limitations
* This work used a convenience sample of n=99 sites. Would be more comprehensive if expanded.
* Some sites that are based in the US could conceivably employ social media teams based in India, potentially providing a benign explanation
