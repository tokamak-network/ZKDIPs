# ZKDIPs
ZK-DEX Improvement Proposals (ZKDIPs) describe standards for the zk-dex platform, including core protocol specifications, client APIs, and contract standards.

# Contributing

 1. Review [ZKDIP-1](ZKDIPs/zkdip-1.md).
 2. Fork the repository by clicking "Fork" in the top right.
 3. Add your ZKDIP to your fork of the repository. There is a [template ZKDIP here](zkdip-template.md).
 4. Submit a Pull Request to [ZKDIPs repository](https://github.com/Onther-Tech/ZKDIPs).

Your first PR should be a first draft of the final ZKDIP. It must meet the formatting criteria. An editor will manually review the first PR for a new ZKDIP and assign it a number before merging it. Make sure you include a `discussions-to` header with the URL to a discussion forum or open GitHub issue where people can discuss the ZKDIP as a whole.

If your ZKDIP requires images, the image files should be included in a subdirectory of the `assets` folder for that ZKDIP as follows: `assets/zkdip-N` (where **N** is to be replaced with the ZKDIP number). When linking to an image in the ZKDIP, use relative links such as `../assets/zkdip-1/image.png`.

When you believe your ZKDIP is mature and ready to progress past the draft phase, you should do one of two things:

 - **For a Standards Track ZKDIP of type Core**, open zoom seminar at [here](https://calendar.google.com/calendar/embed?src=onther.io_r5sqccaoqrrjfio3nli8bpbk34%40group.calendar.google.com&ctz=Asia%2FSeoul), where it can be discussed for inclusion in a future hard fork. If implementers agree to include it, the ZKDIP editors will update the state of your ZKDIP to 'Final'.
 - **For all other ZKDIPs**, open a PR changing the state of your ZKDIP to 'Final'. An editor will review your draft and ask if anyone objects to its being finalised. If the editor decides there is no rough consensus - for instance, because contributors point out significant issues with the ZKDIP - they may close the PR and request that you fix the issues in the draft before trying again.

# ZKDIP Status Terms

* **Draft** - an ZKDIP that is undergoing rapid iteration and changes.
* **Final (non-Core)** - an ZKDIP that has any technical changes that were requested have been addressed by the author.
* **Final (Core)** - an ZKDIP that the Core Devs have decided to implement and release in a future hard fork or has already been released in a hard fork.
