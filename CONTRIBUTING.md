# Contributing

If you have an idea or feature request please open an [issue][1], even if you
don't have time to contribute!

## Making Changes

> **Note**: This guide assumes you have a working Altium Designer 21
> installation and Git for Windows with LFS support installed. This repository
> relies on resources managed by the [Altium][2] template repository, which
> should be set up prior to making changes.

To get started, [fork][3] this repository on GitHub and clone a working copy for
development under `C:\Altium\Projects`:

    $ git clone git@github.com:YOUR-USERNAME/PCB-PiDP11IOExpander.git

Once cloned, open the project and make changes as needed. When you are finished,
be sure to check ERC and DRC output. At a minimum, there should be no
regressions. If user-facing changes are introduced, be sure to add an entry to
the `Unreleased` section in [CHANGELOG.md][4].

With that out of the way, you may now commit your changes and create a [pull
request][4] against the `master` branch for review!

## Making New Releases

Making new releases is automated by Altium Designer's [Project Releaser][5].
Releases should only be created from the `master` branch; as such `master`
should be passing ERC and DRC at all times.

To make a new release, follow these steps:

1. Update the `ProjectRev` parameter by right clicking on the project file in
   the Projects Panel and selecting `Project Options...` and navigating to the
   `Parameters` tab.
2. Create a new section in [CHANGELOG.md][4] for the new revision, and move items
   from `Unreleased` to this section. Links should also be updated to point to
   the correct tags for comparison.
3. Commit changes by issuing: `git commit -a -m "Release Revision <ProjectRev>"`.
4. Create a release tag by issuing: `git tag -a -m "Release Revision <ProjectRev>"
   Rev<ProjectRev>`.
5. Push changes to `master` by issuing: `git push origin master --tags`.
6. Refresh VCS status by right clicking on the project file in the Projects
   Panel and selecting `Version Control` then `Refresh`.
7. Right click on the project file in the Projects Panel and select `Project
   Releaser...` then click on the `Prepare & Pack` button.
8. Once finished, create a new release on [GitHub][6] using the resulting
   archive in the `Project Outputs` folder.

## License

By contributing to this repository, you agree that your contributions will be
licensed under its Simplified BSD License.

[1]: https://github.com/sstallion/PCB-PiDP11IOExpander/issues
[2]: https://github.com/sstallion/Altium
[3]: https://docs.github.com/en/github/getting-started-with-github/fork-a-repo
[4]: https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request
[5]: https://www.altium.com/documentation/altium-designer/working-with-the-project-releaser-ad
[6]: https://github.com/sstallion/PCB-PiDP11IOExpander/releases

[CHANGELOG.md]: CHANGELOG.md
