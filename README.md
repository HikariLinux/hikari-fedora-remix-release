# Hikari Fedora Remix release files

Release identity, systemd presets, and RPM package definitions for the Hikari
Linux Fedora Remix. The spec and software identity tags use Hikari branding;
Fedora compatibility capabilities, repository dependencies, and release-file
paths are retained. The approved Hikari logo is installed as a scalable SVG.

This is a development packaging repository, not a released distribution image.
The preserved spec defaults to Fedora 39/Rawhide when no build target is supplied;
select the intended Fedora build target explicitly. The inherited edition list
does not establish that Hikari images or hardware support exist for those editions.

## Building

Use a Fedora RPM build environment with `redhat-rpm-config`,
`systemd-rpm-macros`, and `rpmautospec`. Supply the files listed by the spec's
`Source` entries from this checkout, and process its automatic release and
changelog macros using the normal rpmautospec workflow before building
`hikari-fedora-remix-release.spec`.

Each renamed package provides and obsoletes its former
`asahi-fedora-remix-release` counterpart. Replace the matching common, variant,
and identity packages together. The existing `fedora-release` capabilities and
`ID_LIKE=fedora` preserve dependency and distribution detection compatibility.
The Fedora legal notice and Fedora package documentation remain applicable to
the Fedora components and retain their original references.

## Origin and license

Based on the preserved [asahi-fedora-remix-release snapshot](https://github.com/HikariLinux/asahi-fedora-remix-release/tree/2adaa98695b768ff64f35f9ffca5d44adfdf8186),
commit `2adaa98695b768ff64f35f9ffca5d44adfdf8186`. Original history and the
`snapshot-2026-11-08` tag are retained. Hikari Linux maintains this project
independently; this is not an official Asahi Linux or Fedora release.

Original copyright and license notices are preserved. Hikari Linux changes
and artwork are provided under the [MIT license](LICENSE).
