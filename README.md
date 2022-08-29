# Nix cache proxy for R2

## Setting up on your domain

 1. Create an A record on the subdomain you want this Worker to run on which points to `192.0.2.1` (see https://community.cloudflare.com/t/a-record-name-for-worker/98841/2 for why)
 2. Edit `wrangler.toml`
    - `account_id` should be your Cloudflare account's tag
    - `route` should be the subdomain this Worker will run on followed by `/*`
    - `bucket_name` and `preview_bucket_name` should be the name of the R2 bucket you'll use
 3. Run `npm run login` to login to Wrangler
 4. Run `npm run deploy`!
 5. Upload an `index.html` to your bucket if you want a landing page