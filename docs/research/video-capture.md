# Video capture and streaming research

**Status:** Open investigation.

Compare Linux V4L2/UVC support, audio synchronization, input formats, buffering, hardware encoder compatibility, and end-to-end latency. Candidates include USB capture with an Intel Quick Sync host; no device selected.

Test at least:
- direct HDMI -> TV baseline
- HDMI -> capture -> local preview
- HDMI -> capture -> hardware encode -> wired client decode -> TV
- recovery from video loss and console reset

Record capture format, encode settings, network conditions, display mode, audio drift, and input-to-photon latency. Avoid treating manufacturer latency claims as measured end-to-end results.
