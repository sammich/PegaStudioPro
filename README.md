![rocket-launch-line-icon](https://github.com/sammich/PegaStudioPro/assets/1682127/39f93eb8-25c1-4f2e-a525-d7b090dfb198)

# Pega Studio Pro

This is the home of the *Pega Studio Pro* component.

For issues, questions, feedback, feature requests, suggestions, create an issue. Vote on whatever you think should be added.

## What is it?

*Pega Studio Pro* is an growing collection of over 120 developer experience/Quality of Life enhancements to Dev Studio. It was built and used on a client project, and development has continued beyond it.

For detailed overview of (almost) every change, see [this Miro board](https://miro.com/app/board/uXjVNWQE6xU=/?share_link_id=476120716316).

This component only enhances the *authoring* experience. There are no runtime changes or side effects as a result of this component being used. We recommend use on Development systems only.

## Why did you make this component?

I spend a lot of time in Dev Studio and I like the tools I use a lot to be efficient and be friendly to use. Since we want the output of the applications we build on the platform to be 'user friendly' why not our development tools (typically referred to as DX or Developer QoL)?

Therefore, this component was built to:

- reduce the number of clicks to achieve common actions, such as lifting actions out of menus
- surface data that is otherwise hidden, such as the 'pass parameter page'
- increase the density or make better use of the UI
    - the new persistent sidebar
    - the branch landing page
- improve tools such as tracer/clipboard
- remove unnecessary friction, such as with the default password feature

## Requirements

- Pega 8.6 or later
- Latest [Pega Peer Review](https://community.pega.com/marketplace/components/peer-review-component) for your platform installed
    - v8.6.8 for platform versions up to 8.8.x
    - v8.83.09 for platform '23 or later

## Available versions

The component is available in two streams based on your platform version:

- Infinity 8.8 or earlier (pre-Infinity '23)
- Infinity '23 and later

Download the file indicated by the version here (`08` = 8.8 and earlier, `23` = '23 and later)

```
PegaStudioPro-08.08.01-yyyy-MM-dd-hhmm.zip
                 ^^
```

## Installation

1. Download a copy of the component for your platform (see above)
2. Ensure you have the correct version of [Pega Peer Review](https://community.pega.com/marketplace/components/peer-review-component) installed
3. Install it like any Pega component. There is a schema installation step.
   Ignore the warning about the component being exported from a newer platform version.
4. In your application definition, add this component and save.
   There's no need to also have Pega Peer Review component on your application as it's included as a dependency in the Pega Studio Pro component.

See 'Configuration' section below for additional options after installation.

### Upgrading from 8.8 to 8.23

If you are using *Pega Studio Pro* and upgraded your platform to Inifinty '23:

1. Install the supported *Pega Peer Review* version (see Requirements above)
2. Import the Infinity '23 version of *Pega Studio Pro*
3. Update each application using the previous version of *Pega Studio Pro* to use `8.23.0` of the component

## Configuration

Pega Studio Pro has a settings page you can access from the PSP widget on the 'Home' tab in Dev Studio. You may want to take some time to understand the options available, and configure it before you use it for the first time.

There are also configurations available on the [Operator-level](https://miro.com/app/board/uXjVNWQE6xU=/?moveToWidget=3458764568005141127&cot=14).

Please note:

- Configuration have a per-application scope
    - On the setting landing page, each configuration has a 'Use as default' action to override the default on the system-level, so you don't need to set it for every application you use PSP on
    - Each time you install the component, the component defaults will be defaulted to the packaged values. You'll need to click on 'Use as default' for each value again
    - For any reason, if you want to restore the component defaults as-shipped, there's a button on the landing page ("Restore PSP config")

## Updates and releases

The component, depending on feedback and enhancement requests, may get fairly regular updates as they are added.

When the Pega Peer Review component is updated, this component will get updated in due course. Do not manually update to the new component version.

Check the release notes for details of all changes in each release.

## What if something goes wrong? (a.k.a. warranty & support)

No warranty is provided for this component. Support is provided via the GitHub issues on this repo.

> [!CAUTION]
> If you suspect any issues with your application, please retest with the component removed, *before* raising a support ticket with Pega.

1. If it's a blocking issue, remove the component from your app. The component is designed to only be assistive, and can be removed at any time without consequence.
2. Check the issues page if it's an existing issue, and vote for it, or create a new issue and share as much as you can.

However, I will be notified of all activity on this repo, so if you report it, it will be noticed. Depending on the severity, might even be addressed fairly quickly.

## FAQs

- **What environments can I use this in?**

  This is primarily a development tool, and shouldn't need to be used in non-dev environments.

  There is no reason why this can't be used in higher environments, as we strictly avoid creating end-user (UI) or runtime changes (process engine, etc.). In other words, all changes are to improve the authoring experience.

  However, while great care has been taken in building this component, please be mindful that support is only available via this repo.

- **How will newer platform versions be supported? How long will it take to support a new version?**

  Officially, the component may support the latest release as soon as GA day, as the validation process is fairly quick. However, based on past releases, you should not experience any issues running an older version for a newer platform.
  
  When a minor (8.x) or patch (8.x.y) Pega Platform is released, we:

  1. Identify all the overriden rules in the component which have been updated in the latest release (via a report)
  2. Manually examine each updated rule, merging changes or rebuilding as necessary
  3. Perform a regression test
 
  For more details, head over to the [wiki](https://github.com/sammich/PegaStudioPro/wiki/Development-guidelines).

- **I don't like change X**

  Some features can be turned off. If the option isn't there yet, create an issue and the discussion can happen in there.

- **Do I need to have Pega Peer Review?**

  Yes. Question is, why *aren't* you using it?

- **Can I get a simplified version for use in Prod?**

  If there is enough community support for such a release, with a good reason for which changes make it unsuitable for Pre-Prod/Prod, then it can be considered.

- **How did you modify Dev Studio? Aren't all the rules Final/Internal/pz?**

  Yes.
