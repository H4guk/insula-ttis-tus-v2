# insula-ttis-tus-v2

[日本語](README.ja.md)

Paper version of the comparison between temporal interference stimulation (tTIS) and transcranial ultrasound stimulation (TUS) of the human insula.

The competition version (Sim4Life Student Competition 2026, one head model in Sim4Life.lite, peripheral axons) is in [H4guk/insula-tTIS-TUS](https://github.com/H4guk/insula-tTIS-TUS). This repository redoes the comparison with open tools so that the limitations of that version can be fixed:

- several head models instead of one
- the same head model and the same neuron simulator for both methods
- cortical pyramidal neurons instead of peripheral axons

Planned tools (not yet verified): SimNIBS (head models, tTIS fields), BabelBrain or k-Wave (TUS fields), NEURON with the Aberra cortical neurons and PySONIC (neuron responses).

The neuron comparison in the paper uses cortical pyramidal neurons only. MorphoSONIC axons are kept as a check that the new pipeline reproduces the competition results, and as a fallback if the pyramidal neurons do not work for TUS; they are not reported as results.

### Contents

```
.github/         git rules (CONTRIBUTING.md), issue/PR templates, PR format check
docs/            progress log, error log, method notes, figures
notebooks/       analysis notebooks
results/         small result tables (large field outputs are not committed)
scripts/         pipeline and analysis scripts (see scripts/README.md)
requirements.txt Python packages for post-processing
```

Head data (MRI, CT), SimNIBS head meshes and field outputs are not committed (see `.gitignore`).

