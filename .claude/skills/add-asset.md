# add-asset

Add a new asset to the dashboard by CoinGecko ID.

## Steps
1. Look up $ARGUMENTS on the CoinGecko API to confirm it exists and get its current price.
2. Determine the appropriate decimal places based on the current price:
   - Price > $1,000 → 0 decimals
   - Price $1–$1,000 → 2 decimals
   - Price < $1 → 4 decimals
3. Add the asset to `index.html` following the exact same pattern as existing assets:
   - Add entry to the `ASSETS` config object
   - Add a `.price-card` div in the `#priceGrid`
   - Add a `<button>` in `#chartTabs`
   - Update the grid layout if needed to accommodate the new card count
4. Commit the change with message: `feat: add [asset name] to dashboard`
5. Push to GitHub.

## Rules
- Match the existing format exactly — same structure, same style, same timeframe.
- Do not modify any existing asset configuration.
- If the CoinGecko ID is not found, stop and tell me.
