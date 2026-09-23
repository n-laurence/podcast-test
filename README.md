# The Future in Tech

<p align="center">
  <img src="images/artwork.jpg" alt="The Future in Tech podcast artwork" width="280">
</p>

<p align="center">
  <strong>Conversations with the people building the next generation of technology.</strong>
</p>

<p align="center">
  <a href="https://n-laurence.github.io/podcast-test/podcast.xml">
    <img src="https://img.shields.io/badge/Podcast%20Feed-RSS-orange?logo=rss&logoColor=white" alt="Podcast RSS feed">
  </a>
  <a href="https://github.com/n-laurence/podcast-test">
    <img src="https://img.shields.io/github/repo-size/n-laurence/podcast-test" alt="Repository size">
  </a>
  <a href="https://github.com/n-laurence/podcast-test/commits/main">
    <img src="https://img.shields.io/github/last-commit/n-laurence/podcast-test" alt="Last commit">
  </a>
  <a href="https://github.com/n-laurence/podcast-test/blob/main/LICENSE">
    <img src="https://img.shields.io/badge/license-not%20specified-lightgrey" alt="License not specified">
  </a>
</p>

> A lightweight Python-powered podcast feed for **The Future in Tech**, a weekly series powered by LinkedIn Learning and hosted by Ray Villalobos.

## Listen and learn

Explore conversations about generative AI, responsible technology, DevOps, business strategy, and the tools shaping the future of work.

<p align="center">
  <a href="https://go.raybo.org/tfit-episodes"><strong>Browse episodes</strong></a>
  ·
  <a href="https://n-laurence.github.io/podcast-test/podcast.xml"><strong>Subscribe to the RSS feed</strong></a>
  ·
  <a href="https://go.raybo.org/tfit-youtube"><strong>Watch on YouTube</strong></a>
</p>

## About the project

This repository uses a simple, maintainable workflow:

1. Podcast metadata and episode details are stored in [`feed.yaml`](feed.yaml).
2. [`feed.py`](feed.py) reads the YAML configuration.
3. The script generates [`podcast.xml`](podcast.xml), an RSS feed ready for podcast applications.
4. Audio and artwork are served as static assets from GitHub Pages.

## Repository contents

| Path | Purpose |
| --- | --- |
| [`feed.yaml`](feed.yaml) | Podcast and episode metadata |
| [`feed.py`](feed.py) | Generates the RSS XML document |
| [`podcast.xml`](podcast.xml) | Generated podcast feed |
| [`audio/`](audio/) | Episode audio files |
| [`images/`](images/) | Podcast artwork and images |
| [`.github/`](.github/) | GitHub configuration and workflows |

## Run locally

### Requirements

- Python 3
- PyYAML

Install the Python dependency:

```bash
python -m pip install pyyaml
```

Generate the feed:

```bash
python feed.py
```

The generated feed is written to `podcast.xml`.

## Add an episode

Add a new item to `feed.yaml` with the episode title, description, publication date, audio path, duration, and file size:

```yaml
item:
  - title: EP06-Your Episode Title
    description: A short description of the episode.
    published: Thu, 16 Feb 2023 18:00:00 GMT
    file: /audio/TFIT06.mp3
    duration: 00:00:30
    length: 480000
```

Then run:

```bash
python feed.py
```

Commit the updated `feed.yaml`, generated `podcast.xml`, and new audio file together before publishing.

## GitHub Pages

The site is configured for static hosting at:

**[n-laurence.github.io/podcast-test](https://n-laurence.github.io/podcast-test)**

The podcast feed is available at:

**[podcast.xml](https://n-laurence.github.io/podcast-test/podcast.xml)**

For GitHub Pages to serve the feed correctly, make sure the repository's Pages source is configured to publish from the branch and directory containing `podcast.xml`.

## Related links

- [The Future in Tech](https://go.raybo.org/tfit)
- [Episode Guide](https://go.raybo.org/tfit-episodes)
- [YouTube Playlist](https://go.raybo.org/tfit-youtube)
- [Audio-Only Podcast Feed](https://go.raybo.org/tfit-feed-audio)
- [Episode Newsletter](https://go.raybo.org/tfit-newsletter)
- [LinkedIn Learning](https://www.linkedin.com/learning/)

## Contributing

To update the podcast, edit `feed.yaml`, add the corresponding audio or image assets, regenerate `podcast.xml`, and submit a pull request with the complete set of changes.

## License

No license is currently specified for this repository. Add a `LICENSE` file if you intend to permit reuse or redistribution.
