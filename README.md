# Why

For OVOS we have a [msm alternative](https://github.com/OpenVoiceOS/ovos_skill_manager) and this repo is used to control msm behaviour in mycroft-core

Mycroft does not like [alternative appstores](https://github.com/MycroftAI/mycroft-skills-manager/pull/75), but we can replace the official marketplace url

Mycroft also makes it hard to uninstall default skills, they will keep reinstalling automatically even if you remove them. We consider this goes against user freedom

# Disabling MSM completely

If you want to completely disable msm, change your mycroft.conf

```
  "skills": {
    "msm": {
      "repo": {
        "url": "https://github.com/OpenVoiceOS/disable-msm-dummy-repo",
        "branch": "disable_msm"
      }
    },
```


# Keeping backend skills

If you want to only keep the configuration and pairing skills, needed to properly interact with Selene

```
  "skills": {
    "msm": {
      "repo": {
        "url": "https://github.com/OpenVoiceOS/disable-msm-dummy-repo",
        "branch": "backend_only"
      }
    },
```

# Disabling default skills

If you want to keep the full msm functionality (marketplace installer skill), but not have default skills installed (except pairing and configuration)

NOTE: this may lag behind official marketplace, open an Issue if we are due an update

Last sync: 27/12/2020  branch 20.08

```
  "skills": {
    "msm": {
      "repo": {
        "url": "https://github.com/OpenVoiceOS/disable-msm-dummy-repo",
        "branch": "no_default_skills"
      }
    },
```

# Alternative default skills

If you want an alternative setup open an Issue, we can provide a branch with your personal default skill selection. If however you want a full alternative appstore then you should fork mycroft-skills and maintain it yourself

