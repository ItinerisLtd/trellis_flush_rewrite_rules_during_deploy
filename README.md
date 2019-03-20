# trellis-flush-rewrite-rules-during-deploy

[![Build Status](https://travis-ci.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy.svg?token=ptrvJskDR5BKm8thpNdd&branch=master)](https://travis-ci.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy)
[![GitHub tag](https://img.shields.io/github/tag/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy.svg)](https://github.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy/tags)
[![license](https://img.shields.io/github/license/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy.svg)](https://github.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy/blob/master/LICENSE)

<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->


- [Requirements](#requirements)
- [Installation](#installation)
- [Usage](#usage)
- [Author Information](#author-information)
- [Feedback](#feedback)
- [Change log](#change-log)
- [License](#license)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

## Goal

Resets WordPress' rewrite rules (based on registered post types, etc) during [Trellis](https://github.com/roots/trellis) deploys.

## Minimum Requirements

- Trellis [9dfddfd](https://github.com/roots/trellis/commit/9dfddfd0d5f7d10886d2f434c02d3bd23edb8684)
- Ansible v2.4
- [WP CLI](https://wp-cli.org/) v2.1.0

## Installation

Add this role to `requirements.yml`:

```yaml
# requirements.yml
- src: itinerisltd.trellis-flush-rewrite-rules-during-deploy
  version: 0.1.0 # Check for latest version!
```

Add this role to the [`deploy_finalize_after` hook](https://roots.io/trellis/docs/deploys/#hooks):

```yaml
# group_vars/all/deploy-hooks.yml
# Learn more on https://roots.io/trellis/docs/deploys/#hooks
deploy_finalize_after:
  - "{{ playbook_dir }}/vendor/roles/trellis-flush-rewrite-rules-during-deploy/tasks/main.yml"
```

## Usage

[Deploy](https://roots.io/trellis/docs/deploys/#example) as usual. No special action needed.

This role executes `[$ wp rewrite flush](https://developer.wordpress.org/cli/commands/rewrite/flush/)` during [Trellis](https://github.com/roots/trellis) deploys.

## FAQs

### It looks awesome. Where can I find some more goodies like this?

- Articles on [Itineris' blog](https://www.itineris.co.uk/blog/)
- More projects on [Itineris' GitHub profile](https://github.com/itinerisltd)
- More plugins on [Itineris' wp.org profile](https://profiles.wordpress.org/itinerisltd/#content-plugins)
- Follow [@itineris_ltd](https://twitter.com/itineris_ltd) and [@TangRufus](https://twitter.com/tangrufus) on Twitter
- Hire [Itineris](https://www.itineris.co.uk/services/) to build your next awesome site

### This isn't on wp.org. Where can I give a ⭐️⭐️⭐️⭐️⭐️ review?

Thanks! Glad you like it. It's important to let my boss knows somebody is using this project. Instead of giving reviews on wp.org, consider:

- tweet something good with mentioning [@itineris_ltd](https://twitter.com/itineris_ltd) and [@TangRufus](https://twitter.com/tangrufus)
- star this [Github repo](https://github.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy)
- watch this [Github repo](https://github.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy)
- write blog posts
- submit pull requests
- [hire Itineris](https://www.itineris.co.uk/services/)

## Feedback

**Please provide feedback!** We want to make this library useful in as many projects as possible.
Please submit an [issue](https://github.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy/issues/new) and point out what you do and don't like, or fork the project and make suggestions.
**No issue is too small.**

## Change Log

Please see [CHANGELOG](./CHANGELOG.md) for more information on what has changed recently.

## Security

If you discover any security related issues, please email [hello@itineris.co.uk](mailto:hello@itineris.co.uk) instead of using the issue tracker.

## Credits

[trellis-flush-rewrite-rules-during-deploy](https://github.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy) is a [Itineris Limited](https://www.itineris.co.uk/) project created by [Tang Rufus](https://typist.tech).

Full list of contributors can be found [here](https://github.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy/graphs/contributors).

## License

[trellis-flush-rewrite-rules-during-deploy](https://github.com/ItinerisLtd/trellis-flush-rewrite-rules-during-deploy) is licensed under the [MIT License](https://opensource.org/licenses/MIT).
Please see [License File](./LICENSE) for more information.
