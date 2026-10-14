# godwinmix-ci-deps

Copies of the large third party installers that GodwinMix's CI downloads, so a
build does not fail when the upstream server is slow or down. Each release here
holds one unmodified file, as published upstream, with its SHA256.

* `gstreamer-1.28.6`: the official GStreamer 1.28.6 MSVC x86_64 installer for
  Windows, from https://gstreamer.freedesktop.org/data/pkg/windows/1.28.6/msvc/.
  GStreamer is LGPL; its source is at https://gitlab.freedesktop.org/gstreamer/gstreamer.

`.github/workflows/mirror-gstreamer.yml` makes a release: it resumes the download
from upstream until the file is whole, checks its size and, when upstream answers,
its SHA256, and uploads it.
