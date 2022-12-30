# Hash Slinger

![GitHub](https://img.shields.io/github/license/unclesp1d3r/hash-slinger)
![GitHub issues](https://img.shields.io/github/issues/unclesp1d3r/hash-slinger)
![GitHub Repo stars](https://img.shields.io/github/stars/unclesp1d3r/hash-slinger?style=social)
![GitHub last commit](https://img.shields.io/github/last-commit/unclesp1d3r/hash-slinger)
![Maintenance](https://img.shields.io/maintenance/yes/2022)

A hashcat wrapper for distributed cracking, with scalability in mind.

Hash Slinger is a wrapper for hashcat that allows you to distribute cracking jobs across multiple machines. It is designed to be scalable, and can be used to crack large amounts of hashes in a short amount of time.

## Why Hash Slinger?

As avid users of Hashtopolis, we were disappointed to find that it did not scale very well on large environments with many machines, large amounts of hashes, and/or large amounts of rules. We wanted to create a tool that could scale to meet the needs of our environment, and that could be used by others in similar situations, but that was also easy to use and maintain. Hash Slinger is focused on the needs of large Red Teams and pentesting organizations that complex rulesets and large amounts of hashes to crack.

The initial release of Hash Slinger is a proof of concept, and is not intended for production use. It is currently in development, and will be updated with new features and bug fixes as they are developed. The goal of the initial release is to be 100% compatible with Hashtopolis Communication Protocol v2, and to be able to distribute cracking jobs across multiple machines.

Some examples of features that are unique to Hash Slinger's design include:

- Support for uploading and downloading complete pot files for use in other cracking jobs
  In many pentesting environments, the same hashes are cracked multiple times, with different rulesets and masks. Hash Slinger allows you to upload the pot file from one cracking job to another, so that you can skip cracking hashes that have already been cracked. Additionally, pentesters will often use a pot file during an onsite engagement to quickly identify hashes that have already been cracked, and then use that pot file to crack the remaining hashes. Hash Slinger allows you to upload a pot file from an engagement to a central server, and then use that pot file to skip cracking hashes that have already been cracked.
- Support for very large mask sets
- Support for very large rulesets
- Allowing systems to be assigned to different projects so that the system will prioritize cracking jobs for the project it is assigned to.
  Often, resources will be paid for by the project, so it is important to prioritize cracking jobs for the project that is paying for the resources. Hash Slinger allows you to assign systems to different projects, and then prioritize cracking jobs for the project that the system is assigned to. When a cracking job for the assigned project is not available, the system will then crack jobs for other projects.

## Roadmap

- [ ] Initial release

  - [ ] Support for registering hashtopolis agents
  - [ ] Support for automatic setup of hashtopolis agents
    - [ ] Support for downloading cracker binaries
    - [ ] Support for uploading cracker binaries
  - [ ] Support for importing and exporting crack lists
    - [ ] Support for uploading potfiles
    - [ ] Support for downloading potfiles
  - [ ] Support for creating basic dictionary tasks
    - [ ] Support for uploading wordlists
    - [ ] Support for uploading hashlists
  - [ ] Support for downloading basic dictionary tasks
    - [ ] Support for downloading wordlists
    - [ ] Support for downloading custom files
    - [ ] Support for downloading hashlist
  - [ ] Support for rule-based tasks
    - [ ] Support for uploading rulesets
    - [ ] Support for uploading hashlists
  - [ ] Support for creating mask tasks
    - [ ] Support for uploading masks
    - [ ] Support for uploading hashlists

## Contributing

Contributions are always welcome!

See `CONTRIBUTING.md` for ways to get started.

Please adhere to this project's `code of conduct`.

## Acknowledgements

- The [Hashtopolis](https://github.com/hashtopolis/server) team for the inspiration and the [Hashtopolis Communication Protocol v2](https://github.com/hashtopolis/server/blob/master/doc/protocol.pdf) documentation
- [Hashcat](https://github.com/hashcat/hashcat) for the awesome cracker

## License

[GPL-3.0](https://choosealicense.com/licenses/gpl-3.0/)
