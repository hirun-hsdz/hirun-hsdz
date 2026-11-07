# GitHub Profile README — Setup (Sinhala)

මෙම ZIP එකේ අඩංගු වන්නේ:

- `README.md` — ඔබගේ සම්පූර්ණ profile README
- `.github/workflows/metrics.yml` — GitHub metrics, languages, contribution calendar සහ achievements generate කරයි
- `.github/workflows/streak-stats.yml` — contribution streak SVG එක generate කරයි
- `.github/workflows/snake.yml` — contribution snake SVG දෙක generate කරයි

## 1. Files upload කරන්න

මේ files සියල්ල `hirun-hsdz/hirun-hsdz` profile repository එකේ root එකට upload කරන්න. Folder paths ඒ විදිහටම තබන්න.

## 2. Metrics token එක හදන්න

1. GitHub → Settings → Developer settings → Personal access tokens → Fine-grained tokens වෙත යන්න.
2. Token එකක් සාදන්න. Metrics documentation අනුව scope-less token එකක් බොහෝ public profile data සඳහා ප්‍රමාණවත් විය හැක.
3. Repository → Settings → Secrets and variables → Actions → New repository secret.
4. Name එක `METRICS_TOKEN` ලෙස දෙන්න. Token value එක paste කර save කරන්න.
5. Token එක README හෝ workflow YAML එකට කෙළින්ම paste කරන්න එපා.

## 3. Workflow permissions

Repository → Settings → Actions → General → Workflow permissions යටතේ **Read and write permissions** enable කර Save කරන්න.

## 4. Workflows run කරන්න

Repository → Actions වෙත ගොස් මේ workflows තුන වෙන වෙනම open කර **Run workflow** කරන්න:

- Update GitHub Metrics
- Update Contribution Streak
- Generate Contribution Snake

පළමු run එක සම්පූර්ණ වීමට මිනිත්තු කිහිපයක් ගත විය හැක. සියල්ල success වුණාම `metrics.svg`, `profile/streak.svg`, `output/github-snake.svg` සහ `output/github-snake-dark.svg` files නිර්මාණය වී තිබිය යුතුයි.

## 5. වැදගත්

- `metrics.svg` සහ streak SVG එක workflow run එකෙන් පසුව පමණක් පෙන්වයි.
- Snake images `output` folder එකේ workflow එකෙන් generate වේ.
- GitHub contributions update වීමට පැය 24ක් පමණ ප්‍රමාද විය හැක.
- LinkedIn සහ email placeholders ඔබගේ සැබෑ details වලින් වෙනස් කරන්න.
- Project repository placeholders සැබෑ repository URLs වලින් වෙනස් කරන්න.
- External banner, typing text, badges සහ footer සේවා තවමත් external services භාවිතා කරයි; ඒවායේ uptime එක වෙනම පවතී.

References:
- https://github.com/lowlighter/metrics
- https://github.com/DenverCoder1/github-readme-streak-stats
- https://github.com/Platane/snk
