# insula-ttis-tus-v2

Paper version of the comparison between temporal interference stimulation (tTIS) and transcranial ultrasound stimulation (TUS) of the human insula.

The competition version (Sim4Life Student Competition 2026, one head model in Sim4Life.lite, peripheral axons) is in [H4guk/insula-tTIS-TUS](https://github.com/H4guk/insula-tTIS-TUS). This repository redoes the comparison with open tools so that the limitations of that version can be fixed:

- several head models instead of one
- the same head model and the same neuron simulator for both methods
- cortical pyramidal neurons instead of peripheral axons

Planned tools (not yet verified): SimNIBS (head models, tTIS fields), BabelBrain or k-Wave (TUS fields), NEURON with the Aberra cortical neurons and PySONIC (neuron responses).

---

島皮質に対する tTIS と TUS の比較の論文版。コンテスト版（S4L 2026）は H4guk/insula-tTIS-TUS に残し、こちらで限界（頭部モデル1体・手法ごとに違う神経ソルバー・末梢の軸索）を直す。
