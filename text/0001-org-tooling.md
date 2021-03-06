*   Start date: 2018-12-06
*   Scope: the collective
*   RFC PR: [1][]
*   Implementation issue(s): n/a (see [`unifiedjs/github-tools`][tools])

# Summary

GitHub and npm tooling for open source projects.

## Basic example

```sh
org unifiedjs
```

## Motivation

For large projects, especially those that are split amongst numerous
organizations like unified, are often required to perform a lot of
manual admin tasks.

*   team management
*   npm scopes
*   issue templates
*   code of conducts
*   label consistency

I propose an org tool that automates a lot of this process.
This is useful for orgs at the scale of unified, where there is a large,
distributed team and hundreds of repos across numerous orgs.
Without automation it can be cumbersome to keep things in sync, and manual
actions are susceptible to errors.

This could serve like a terraform for open source organizations, removing a lot
of the boilerplate required in setting up repos, ensuring consistency, etc.

## Detailed design

The tool would be based off a template defined in a `.github` repo (following
the pattern of `.github` directories in repos).
In `.github` teams and permissions can be defined, templates, code of conduct,
labels and anything else that might be desired.
It would use this information to update all repos under the org.

## Drawbacks

*   it’d be a reasonable code investment to implement well
*   maybe it’s too much automation

## Alternatives

There isn’t an alternative other than manual handling of these tasks that I’m
aware of.

## Adoption strategy

We’d use the tooling immediately.

[1]: https://github.com/unifiedjs/rfcs/pull/1

[tools]: https://github.com/unifiedjs/github-tools
