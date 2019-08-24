---
zkdip: 1
title: ZKDIP Purpose and Guidelines
status: Active
type: Meta
author: Kevin Jeong <kevin.j@onther.io>
created: 2019-8-24
updated:
---

## What is an ZKDIP?

ZKDIP stands for ZK-DEX Improvement Proposal. An ZKDIP is a design document providing information to the zk-dex community, or describing a new feature for zk-dex or its processes or environment. The ZKDIP should provide a concise technical specification of the feature and a rationale for the feature. The ZKDIP author is responsible for building consensus within the community and documenting dissenting opinions.

## ZKDIP Rationale

We intend ZKDIPs to be the primary mechanisms for proposing new features, for collecting community technical input on an issue, and for documenting the design decisions that have gone into zk-dex. Because the ZKDIPs are maintained as text files in a versioned repository, their revision history is the historical record of the feature proposal.

For zk-dex implementers, ZKDIPs are a convenient way to track the progress of their implementation. Ideally each implementation maintainer would list the ZKDIPs that they have implemented. This will give end users a convenient way to know the current status of a given implementation or library.

## ZKDIP Types

There are three types of ZKDIP:

- A **Standard Track ZKDIP** describes any change that affects most or all zk-dex implementations, such as a change to the note input, a change in exchanging note rules, proposed application standards/conventions, or any change or addition that affects the interoperability of applications using Ethereum. Furthermore Standard ZKDIPs can be broken down into the following categories. Standards Track ZKDIPs consist of three parts, a design document, implementation, and finally if warranted an update to the [formal specification].
  - **Protocol** - improvements requiring a Protocol Update, as well as changes that are not necessarily consensus critical but may be relevant to “core dev” discussions.
  - **Circuit** - includes improvements around circuit.
  - **Interface** - includes improvements around client [API/RPC] specifications and standards, and also certain language-level standards like method names. The label “interface” aligns with the [interfaces repo] and discussion should primarily occur in that repository before an ZKDIP is submitted to the ZKDIPs repository.
- A **Meta ZKDIP** describes a process surrounding zk-dex or proposes a change to (or an event in) a process. Process ZKDIPs are like Standards Track ZKDIPs but apply to areas other than the zk-dex protocol itself. They may propose an implementation, but not to zk-dex's codebase; they often require community consensus; unlike Informational ZKDIPs, they are more than recommendations, and users are typically not free to ignore them. Examples include procedures, guidelines, changes to the decision-making process, and changes to the tools or environment used in zk-dex development. Any meta-ZKDIP is also considered a Process ZKDIP.
- An **Informational ZKDIP** describes an zk-dex design issue, or provides general guidelines or information to the zk-dex community, but does not propose a new feature. Informational ZKDIPs do not necessarily represent zk-dex community consensus or a recommendation, so users and implementers are free to ignore Informational ZKDIPs or follow their advice.

It is highly recommended that a single ZKDIP contain a single key proposal or new idea. The more focused the ZKDIP, the more successful it tends to be. A change to one client doesn't require an ZKDIP; a change that affects multiple clients, or defines a standard for multiple apps to use, does.

An ZKDIP must meet certain minimum criteria. It must be a clear and complete description of the proposed enhancement. The enhancement must represent a net improvement. The proposed implementation, if applicable, must be solid and must not complicate the protocol unduly.

## ZKDIP Work Flow

### Shepherding an ZKDIP

Parties involved in the process are you, *ZKDIP author*, the [*ZKDIP editors*](#ZKDIP-editors), and the *ZK-DEX Core Developers*.

Before you begin writing a formal ZKDIP, you should vet your idea. Ask the zk-dex community first if an idea is original to avoid wasting time on something that will be be rejected based on prior research. It is thus recommended to open a discussion thread on [the Issues section of this repository].

In addition to making sure your idea is original, it will be your role as the author to make your idea clear to reviewers and interested parties, as well as inviting editors, developers and community to give feedback on the aforementioned channels. You should try and gauge whether the interest in your ZKDIP is commensurate with both the work involved in implementing it and how many parties will have to conform to it. For example, the work required for implementing a Core ZKDIP will need sufficient interest from the zk-dex client teams. Negative community feedback will be taken into consideration and may prevent your ZKDIP from moving past the Draft stage.

### Core ZKDIPs

For Core ZKDIPs, given that they require client implementations to be considered **Final** (see "ZKDIPs Process" below), you will need to either provide an implementation for clients or convince clients to implement your ZKDIP.

The best way to get client implementers to review your ZKDIP is to present it on an AllCoreDevs call. You can request to do so by making seminar event on an [Open Blockchain Webinar Calender](https://calendar.google.com/calendar/embed?src=onther.io_r5sqccaoqrrjfio3nli8bpbk34%40group.calendar.google.com&ctz=Asia%2FSeoul).  

The seminar call serve as a way for implementers to do this things. To discuss the technical merits of ZKDIPs.

These calls generally result in a "rough consensus" around what ZKDIPs should be implemented. This "rough consensus" rests on the assumptions that ZKDIPs is technically sound.

:warning: The ZKDIPs process and seminar call were not designed to address contentious non-technical issues, but, due to the lack of other ways to address these, often end up entangled in them. This puts the burden on client implementers to try and gauge community sentiment, which hinders the technical coordination function of ZKDIPs and seminar calls. If you are shepherding an ZKDIP, you can make the process of building community consensus easier by making sure that [ZKDIPs Issues] thread for your ZKDIP includes or links to as much of the community discussion as possible and that various stakeholders are well-represented.

*In short, your role as the author is to write the ZKDIP using the style and format described below, shepherd the discussions in the appropriate forums, and build community consensus around the idea.*

### ZKDIP Process

Following is the process that a successful ZKDIP will move along:

```
[ WIP ] -> [ DRAFT ] -> [(ACCEPTED)] -> [ FINAL ]
```

Each status change is requested by the ZKDIP author and reviewed by the ZKDIP editors. Use a pull request to update the status. Please include a link to where people should continue discussing your ZKDIP. The ZKDIP editors will process these requests as per the conditions below.

* **Active** -- Some Informational and Process ZKDIPs may also have a status of “Active” if they are never meant to be completed. E.g. ZKDIP-1 (this ZKDIP).
* **Work in progress (WIP)** -- Once the author has asked the ZK-DEX community whether an idea has any chance of support, they will write a draft ZKDIP as a [pull request]. Consider including an implementation if this will aid people in studying the ZKDIP.
  * :arrow_right: Draft -- If agreeable, ZKDIP editor will assign the ZKDIP a number (generally the issue or PR number related to the ZKDIP) and merge your pull request. The ZKDIP editor will not unreasonably deny an ZKDIP.
  * :x: Draft -- Reasons for denying draft status include being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing backwards compatibility.
* **Draft** -- Once the first draft has been merged, you may submit follow-up pull requests with further changes to your draft until such point as you believe the ZKDIP to be mature and ready to proceed to the next status. An ZKDIP in draft status must be implemented to be considered for promotion to the next status (ignore this requirement for core ZKDIPs).
  * :arrow_right: Final -- After seminar and if agreeable, the ZKDIP editor will assign Final status.
  * :x: Final -- A request for Final status will be denied if material changes are still expected to be made to the draft.
* **Accepted (Core ZKDIPs only)** -- This ZKDIP is in the hands of the zk-dex core developers. Their process for deciding whether to encode it into their implementation of zk0dex as part of a upgrade is not part of the ZKDIP process.
  * :arrow_right: Final -- Standards Track Core ZKDIPs must be implemented in at least three viable Ethereum clients before it can be considered Final. When the implementation is complete and adopted by the community, the status will be changed to “Final”.
* **Final** -- This ZKDIP represents the current state-of-the-art. A Final ZKDIP should only be updated to correct errata.

Other exceptional statuses include:

* **Abandoned** -- This ZKDIP is no longer pursued by the original authors or it may not be a (technically) preferred option anymore.
* **Rejected** -- An ZKDIP that is fundamentally broken or a Core ZKDIP that was rejected by the Core Devs and will not be implemented.
* **Active** -- This is similar to Final, but denotes an ZKDIP which may be updated without changing its ZKDIP number.
* **Superseded** -- An ZKDIP which was previously final but is no longer considered state-of-the-art. Another ZKDIP will be in Final status and reference the Superseded ZKDIP.

## What belongs in a successful ZKDIP?

Each ZKDIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the ZKDIP, including the ZKDIP number, a short descriptive title (limited to a maximum of 44 characters), and the author details. See [below](#ZKDIP-header-preamble) for details.
- Simple Summary - “If you can’t explain it simply, you don’t understand it well enough.” Provide a simplified and layman-accessible explanation of the ZKDIP.
- Abstract - a short (~200 word) description of the technical issue being addressed.
- Motivation (*optional) - The motivation is critical for ZKDIPs that want to change the Ethereum protocol. It should clearly explain why the existing protocol specification is inadequate to address the problem that the ZKDIP solves. ZKDIP submissions without sufficient motivation may be rejected outright.
- Specification - The technical specification should describe the syntax and semantics of any new feature. The specification should be detailed enough to allow competing, interoperable implementations for any of the current zk-dex platforms.
- Rationale - The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.
- Backwards Compatibility - All ZKDIPs that introduce backwards incompatibilities must include a section describing these incompatibilities and their severity. The ZKDIP must explain how the author proposes to deal with these incompatibilities. ZKDIP submissions without a sufficient backwards compatibility treatise may be rejected outright.
- Test Cases - Test cases for an implementation are mandatory for ZKDIPs that are affecting consensus changes. Other ZKDIPs can choose to include links to test cases if applicable.
- Implementations - The implementations must be completed before any ZKDIP is given status "Final", but it need not be completed before the EIP is accepted. While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of "rough consensus and running code" is still useful when it comes to resolving many discussions of API details.
- Copyright Waiver - All ZKDIPs must be in the public domain. See the bottom of this ZKDIP for an example copyright waiver.

## ZKDIP Formats and Templates

ZKDIPs should be written in [markdown] format.
Image files should be included in a subdirectory of the `assets` folder for that ZKDIP as follows: `assets/ZKDIP-N` (where **N** is to be replaced with the ZKDIP number). When linking to an image in the ZKDIP, use relative links such as `../assets/ZKDIP-1/image.png`.

## ZKDIP Header Preamble

Each ZKDIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order. Headers marked with "*" are optional and are described below. All other headers are required.

` ZKDIP:` <ZKDIP number> (this is determined by the ZKDIP editor)

` title:` <ZKDIP title>

` author:` <a list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.>

` * discussions-to:` \<a url pointing to the official discussion thread\>

` status:` <Draft | Last Call | Accepted | Final | Active | Abandoned | Rejected | Superseded>

`* review-period-end:` <date review period ends>

` type:` <Standards Track (Core, Networking, Interface, ERC)  | Informational | Meta>

` * category:` <Core | Networking | Interface | ERC>

` created:` <date created on>

` * updated:` <comma separated list of dates>

` * requires:` <ZKDIP number(s)>

` * replaces:` <ZKDIP number(s)>

` * superseded-by:` <ZKDIP number(s)>

` * resolution:` \<a url pointing to the resolution of this ZKDIP\>

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header optionally lists the names, email addresses or usernames of the authors/owners of the ZKDIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the author header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

#### `resolution` header

The `resolution` header is required for Standards Track ZKDIPs only. It contains a URL that should point to an email message or other web resource where the pronouncement about the ZKDIP is made.

#### `discussions-to` header

While an ZKDIP is a draft, a `discussions-to` header will indicate the mailing list or URL where the ZKDIP is being discussed. As mentioned above, examples for places to discuss your ZKDIP include an issue in this repo or in a fork of this repo.

No `discussions-to` header is necessary if the ZKDIP is being discussed privately with the author.

As a single exception, `discussions-to` cannot point to GitHub pull requests.

#### `type` header

The `type` header specifies the type of ZKDIP: Standards Track, Meta, or Informational. If the track is Standards please include the subcategory (core, networking, interface, or ERC).

#### `category` header

The `category` header specifies the ZKDIP's category. This is required for standards-track ZKDIPs only.

#### `created` header

The `created` header records the date that the ZKDIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `updated` header

The `updated` header records the date(s) when the ZKDIP was updated with "substantial" changes. This header is only valid for ZKDIPs of Draft and Active status.

#### `requires` header

ZKDIPs may have a `requires` header, indicating the ZKDIP numbers that this ZKDIP depends on.

#### `superseded-by` and `replaces` headers

ZKDIPs may also have a `superseded-by` header indicating that an ZKDIP has been rendered obsolete by a later document; the value is the number of the ZKDIP that replaces the current document. The newer ZKDIP must have a `replaces` header containing the number of the ZKDIP that it rendered obsolete.

## Auxiliary Files

ZKDIPs may include auxiliary files such as diagrams. Such files must be named ZKDIP-XXXX-Y.ext, where “XXXX” is the ZKDIP number, “Y” is a serial number (starting at 1), and “ext” is replaced by the actual file extension (e.g. “png”).

## Transferring ZKDIP Ownership

It occasionally becomes necessary to transfer ownership of ZKDIPs to a new champion. In general, we'd like to retain the original author as a co-author of the transferred ZKDIP, but that's really up to the original author. A good reason to transfer ownership is because the original author no longer has the time or interest in updating it or following through with the ZKDIP process, or has fallen off the face of the 'net (i.e. is unreachable or isn't responding to email). A bad reason to transfer ownership is because you don't agree with the direction of the ZKDIP. We try to build consensus around an ZKDIP, but if that's not possible, you can always submit a competing ZKDIP.

If you are interested in assuming ownership of an ZKDIP, send a message asking to take over, addressed to both the original author and the ZKDIP editor. If the original author doesn't respond to email in a timely manner, the ZKDIP editor will make a unilateral decision (it's not like such decisions can't be reversed :)).

## ZKDIP Editors

The current ZKDIP editors are

` * Kevin Jeong (@ggs134)`

` * Carl Park (@4000D)`

` * Aidep Park (@Dapploper)`

` * Thomas Shin (@thomashin)`

## ZKDIP Editor Responsibilities

For each new ZKDIP that comes in, an editor does the following:

- Read the ZKDIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the ZKDIP for language (spelling, grammar, sentence structure, etc.), markup (Github flavored Markdown), code style

If the ZKDIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the ZKDIP is ready for the repository, the ZKDIP editor will:

- Assign an ZKDIP number (generally the PR number or, if preferred by the author, the Issue # if there was discussion in the Issues section of this repository about this ZKDIP)

- Merge the corresponding pull request

- Send a message back to the ZKDIP author with the next step.

Many ZKDIPs are written and maintained by developers with write access to the Ethereum codebase. The ZKDIP editors monitor ZKDIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on ZKDIPs. We merely do the administrative & editorial part.

## History

This document was derived heavily from [Ethereum's EIP-1] by Martin Becze  which in turn was derived from [Bitcoin's BIP-0001]. In many places text was simply copied and modified.

Augest 24, 2019: ZKDIP 1 has been Published.

### Bibliography

[pull request]: https://github.com/Onther-Tech/ZKDIPs/pulls
[formal specification]:
[the Issues section of this repository]: https://github.com/Onther-Tech/ZKDIPs/issues
[markdown]: https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet
[Ethereum's EIP-1]: https://github.com/bitcoin/bips
[Blockchain Webinar Calender]: https://calendar.google.com/calendar/embed?src=onther.io_r5sqccaoqrrjfio3nli8bpbk34%40group.calendar.google.com&ctz=Asia%2FSeoul

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
