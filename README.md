# insula-ttis-tus-v2

[日本語](README.ja.md)

Paper version of the comparison between temporal interference stimulation (tTIS) and transcranial ultrasound stimulation (TUS) of the human insula.

The competition version (Sim4Life Student Competition 2026, one head model in Sim4Life.lite, peripheral axons) is in [H4guk/insula-tTIS-TUS](https://github.com/H4guk/insula-tTIS-TUS). This repository redoes the comparison with open tools so that the limitations of that version can be fixed:

- several head models instead of one
- the same head model and the same neuron simulator for both methods
- cortical pyramidal neurons instead of peripheral axons

Planned tools (not yet verified): SimNIBS (head models, tTIS fields), BabelBrain or k-Wave (TUS fields), NEURON with the Aberra cortical neurons and PySONIC (neuron responses).

The neuron comparison in the paper uses cortical pyramidal neurons only. MorphoSONIC axons are kept as a check that the new pipeline reproduces the competition results, and as a fallback if the pyramidal neurons do not work for TUS; they are not reported as results.

## Repository structure

```
insula-ttis-tus-v2/
├── README.md            # this file (English)
├── README.ja.md         # Japanese version of this file
├── LICENSE              # MIT
├── requirements.txt     # Python packages for post-processing (planned tools listed as comments)
├── .gitignore           # excludes head data (MRI/CT) / SimNIBS meshes / field outputs / secrets
├── .github/             # git rules
│   ├── CONTRIBUTING.md              # rules for issues, branches, commits, PRs and reviews
│   ├── ISSUE_TEMPLATE/              # issue forms: [Bug] / [改修] / [作業] / [アイデア]
│   ├── PULL_REQUEST_TEMPLATE.md     # PR template
│   └── workflows/pr-format-check.yml  # checks the PR title and headings
├── scripts/             # pipeline and analysis scripts
│   ├── README.md                    # which script belongs to which stage
│   └── archive/                     # one-off probes and checks (kept as history)
├── notebooks/           # analysis notebooks
├── docs/                # progress log, error log, method notes
│   ├── progress-log.md
│   ├── error-log.md
│   └── figures/
└── results/             # small result tables (large field outputs are in .gitignore)
```

Head data (MRI, CT), SimNIBS head meshes and field outputs are not committed (see `.gitignore`).

