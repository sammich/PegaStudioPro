![rocket-launch-line-icon](https://github.com/sammich/PegaDeveloperProductivityBooster/assets/1682127/39f93eb8-25c1-4f2e-a525-d7b090dfb198)

# Pega Developer Productivity Booster

This is the current home of the PDPB component.

For issues, questions, feedback, feature requests, suggestions, create an issue. Vote on whatever you think should be added.

## What is it?

It’s a large (maybe 100+) collection of Developer Experience/Quality of Life modifications to Dev Studio. It was built and used on a real client project.

For super-detailed overview of basically every change, see [this Miro board](https://miro.com/app/board/uXjVNWQE6xU=/?share_link_id=474308154811).

## Why did you make this component?

I spend a lot of time in Dev Studio and I like the tools I used a lot to be efficient and be friendly to use. Since we want the output of the applications we build on the platform to be 'user friendly' why not our development tools (typically referred to as DX or Developer QoL)?

Therefore, this component was built to:

- reduce the number of clicks to achieve common actions, such as lifting actions out of menus
- surface data that is otherwise hidden, such as the 'pass parameter page'
- increase the density or make better use of the UI
  - the new persistent sidebar
  - the branch landing page
- improve tools such as tracer/clipboard
- remove unnecessary friction, such as with the default password feature

## Requirements

- See [the Miro board](https://miro.com/app/board/uXjVNWQE6xU=/?moveToWidget=3458764567999200990&cot=14) for platform compatability
- [Pega Peer Review v8.6.8](https://community.pega.com/marketplace/components/peer-review-component) installed

## Installation

The component is currently shipping as a single RAP supporting all Pega platform versions.

2. Get a copy of the component (TBA, still in closed testing)
3. Install it like any Pega component.

   Ignore the warning about the component being exported from a newer platform version.
   
5. If you're not on the latest Pega version, open the component and change the ruleset version.

   For example, if you're on 8.8.3, change the ruleset version (component is unlocked) from `SamsMods-ProductivityBooster:08-23-01` to `SamsMods-ProductivityBooster:08-08-03`.
   
   <img width="565" alt="image" src="https://github.com/sammich/PegaDeveloperProductivityBooster/assets/1682127/052fd3d8-7fce-41f7-a43b-08ab13651cdf">
6. Save
7. In your application definition, add this component and save.

   There's no need to also have Pega Peer Review component on your component as it's included as a dependency in the component.
   
8. See configuration

## Configuration

- Uses configuration sets from within App Studio
- If you use an issue tracker like Agile Studio or Jira, you'll need to configure it first

## What if something goes wrong? (a.k.a. warranty & support)

No warranty is provided for this component. Support is provided via the GitHub issues on this repo. This is subject to change, as the component is still in closed testing.

1. If it's a blocking issue, remove the component from your app
2. Check the issues page if it's an existing issue, and vote for it, or create a new issue and share as much as you can

## Potential FAQs

- **What environments can I use this in?**

  Technically, there's no reason you can't use this in environments other than dev, but due to the nature of this component
  and that higher environments more production-like (not less), you probably shouldn't. Then again, there's nothing stoppping
  you.

- **Can I install this on Platform verisons earlier than 8.8.3?**

  I haven't tested it on lower (or higher) platform versions.

  I have plans and metadata in place to support lower and higher versions but as I don't have access to every platform version
  it will take time to get support in.

- **How did you modify Dev Studio? Aren't all the rules Final/Internal/pz?**

  Yes.

- **Won't supporting versions other than 8.8.3 be really difficult?**

  It won't be easy. But I have recorded metadata against every OOTB rule I've overriden in this component to make it easier to
  find out which rules need to be rebuilt or evaluated for support. I will likely need community support to test support for
  Platform versions I don't have easy access to.

- **I don't like change X**

  Some features can be turned off. If the option isn't there yet, create an issue and the discussion can happen in there.

- **Do I need to have Pega Peer Review?**

  Yes. Question is, why *aren't* you using it?

- **Can I get a simplified version for use in Prod?**

  Considering it. If the consensus is that the component is definitely is too hot for Prod.
