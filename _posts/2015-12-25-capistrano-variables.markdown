---
layout: post
title: Capistrano Variables
published: true
date:   2015-12-25 10:37
categories: Web
tags: Capistrano
comments: true
description: more
---


```application``` – required

`repository` – required

`scm` – defaults to :subversion

`deploy_via` – defaults to :checkout

`revision` – defaults to the latest head version

`rails_env` – defaults to ‘production’

`rake` – defaults to ‘rake’

`source` – `Capistrano::Deploy::SCM` object
real_revision

`strategy` – Capistrano::Deploy::Strategy object defined by deploy_via

`release_name` – timestamp in the form of `“%Y%m%d%H%M%S”
`
`version_dir` – defaults to ‘`releases`’

`shared_dir` – defaults to ‘`shared`’

`shared_children` – defaults to `['public/system', 'log', 'tmp/pids']`

`current_dir` – defaults to ‘current’

`releases_path` – path of `deploy_to + version_dir` (`e.g. /u/apps/example/releases` )

`shared_path` – path of `deploy_to + shared_dir` (e.g. `/u/apps/example/shared` )

`current_path` – path of `deploy_to + current_dir` (`e.g. /u/apps/example/current` )

`release_path` – path of releases_path + release_name (e.g. /u/apps/example/releases/20100624000000 )

`releases` – list of releases, found by running ls -x
current_release – path of releases_path + last release (e.g. /u/apps/example/releases/20100624000000 )

`previous_release` – path of releases_path + previous release (e.g. /u/apps/example/releases/20100623000000 )

`current_revision` – revision id of the current release, found in the REVISION file

`latest_revision` – revision id of the latest release

`previous_revision` – revision id of the previous release

`run_method` – either :`run` or :`sudo` depending on if :`use_sudo` is set

`latest_release` – release path or the current release depending on if the current symlink is valid

`maintenence_basename` – defaults to “maintenance”. This and `maintenence_tempate_path` are used to customize the page shown when the application is disabled (e.g. `cap deploy:web:disable`)

`maintenence_template_path` – defaults to the ‘`templates/maintenance.rhtml`’ path
`migrate_env`

`migrate_target` – the version to migrate to. Defaults to :`latest`.