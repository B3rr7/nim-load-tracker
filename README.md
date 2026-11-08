# NIM Load Tracker

NVIDIA NIM free model gulo kon somoy slow/fail kore ta track kore. GitHub Actions prottek 10 min e protita model e ekta choto request pathay, result `docs/data/results.csv` e jome, ar GitHub Pages e heatmap dekhay (IST te).

## Setup (5 minute)
1. Notun GitHub repo baniye ei file gulo push koro.
2. **Settings → Secrets and variables → Actions → New repository secret**: name `NVIDIA_API_KEY`, value tomar `nvapi-...` key.
3. **Settings → Actions → General → Workflow permissions**: "Read and write permissions" on koro.
4. **Settings → Pages**: Source = "Deploy from a branch", Branch = `main`, Folder = `/docs`.
5. **Actions** tab e giye `probe-nim` ke "Run workflow" diye ekbar chalao. Tarpor nijei cholbe.

## Customize
- Model list: `models.txt` (build.nvidia.com theke ID copy koro).
- Interval: `.github/workflows/probe.yml` er `cron`.
- Public repo hole Actions free. Key kokhono commit korona, shudhu Secret e rakho.

## Note
Probe gulo GitHub er US server theke jai, tai tomar location theke feel ektu alada hote pare. Tobe load er pattern (din vs raat) bujhar jonno jothesto.
