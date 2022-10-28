# gits-hitokoto

## Prerequisites

1. Create a public GitHub Gist
   - Visit https://gist.github.com/
   - Create a new gist, set filename to `🌧Hitokoto`

2. Create GitHub Token
   - Visit https://github.com/settings/tokens/new
   - Check `gist` permission
   - Generate and save the token

## Installation Steps

1. Fork this repository

2. Enable GitHub Actions
   - Go to your forked repository
   - Switch to Actions tab
   - Enable "Update gist with new hitokoto" workflow

3. Configure Environment Variables
   Set in `.github/workflows/update.yml`:
   - `GIST_ID`: ID of your created gist (last part of URL)
   - `CATEGORY`: Hitokoto category code
     - Default value `abh` (Anime, Comics, Movies/TV)
     - Leave empty to get all categories
   - Update frequency: Modify `cron` expression (default: hourly)

4. Set Repository Secrets
   - Go to repository Settings > Secrets
   - Click "New repository secret"
   - Add `GH_TOKEN`: Enter your created GitHub token
