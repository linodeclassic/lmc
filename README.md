On January 31, 2020, Linode [shuts down](https://www.linode.com/2019/11/18/notice-legacy-linode-manager-users/) its classic Linode Manager interface in favor of its new Cloud Manager.

Many of us who are long-time users of Linode and the classic manager are disappointed about this change, as it is evidenced in the comments under the announcement. Despite any of the flaws it may have, the classic Linode Manager works, it’s efficient, and we are familiar with it. In contrast the new Cloud Manager features a completely redesigned interface, which many find slow, lacking in information density, and unfamiliar in its structure. It also requires running JavaScript, which some of us may want to avoid.

This project is an attempt to create an open source reimplementation of the classic Linode Manager using the Linode API. It is written from scratch in Go, without using any code from the original, striving to be fast and secure, with lightweight, semantic, accessible markup, and no JavaScript required. It is distributed as a self-contained native binary with no external dependencies, that can be run on either a remote or local machine, without installing any server, runtime, or library.

An online demo with test data is available at http://li1842-248.members.linode.com:8080. You can also download it for [Linux](http://li1842-248.members.linode.com/demo/linux/lmc), [macOS](http://li1842-248.members.linode.com/demo/macos/lmc), and [Windows](http://li1842-248.members.linode.com/demo/windows/lmc.exe), and run it locally with real data:

    ./lmc [username] [email] [access_token]

The command accepts three arguments:

1. A username to display in the header
2. An email address to display its associated gravatar
3. An API access token with at least read-only *Linodes* and *Account* access (you can generate these in the [Cloud Manager](https://cloud.linode.com/profile/tokens))

We are planning to publish frequent demos to update everyone on our progress and to get feedback. Issues can be reported and discussed on the project’s [GitHub page](https://github.com/linodeclassic/lmc), where the source code will also be available. We will also share updates on the project and campaign on our [Twitter account](https://twitter.com/linodeclassic).

For information on our crowdfunding campaign, sponsorship options, and benefits, please see our [Patreon page](https://www.patreon.com/linodeclassic).
