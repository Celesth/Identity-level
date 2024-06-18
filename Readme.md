# Understanding Roblox Exploit Levels and Capabilities

## Introduction
In Roblox scripting and exploiting, knowing the access levels and capabilities of different identities is crucial. This guide breaks down exploit levels, identities, and capabilities, explaining how they work within Roblox.

## What Are Exploit Levels?

Exploit levels, or identities, show how much access an exploit has to various Roblox services, properties, and functions. These levels don't reflect the number of features an exploit has, but rather how much access it has.

## Identities and Capabilities

Roblox uses an access control system called "capabilities." This system converts an identity number into a set of capability flags, each granting specific access rights. For instance, an identity with a higher number might access more restricted functions within Roblox.

## Example of Access Requirements

- **settings()**: Requires Plugin capabilities.
- **game:GetService("RbxAnalyticsService"):GetClientId()**: Requires RobloxScript capabilities.

## Identity to Capability Mapping

Here’s a breakdown of how identities map to capabilities:

| Identity | Capability | Capabilities Names                                                |
|----------|------------|-------------------------------------------------------------------|
| 0        | 0          | None                                                              |
| 1        | 3          | Plugin, LocalUser                                                 |
| 2        | 0          | None                                                              |
| 3        | 11         | Plugin, LocalUser, RobloxScript                                   |
| 4        | 3          | Plugin, LocalUser                                                 |
| 5        | 1          | Plugin                                                            |
| 6        | 11         | Plugin, LocalUser, RobloxScript                                   |
| 7        | 63         | Plugin, LocalUser, WritePlayer, RobloxScript, RobloxEngine, NotAccessible |
| 8        | 63         | Plugin, LocalUser, WritePlayer, RobloxScript, RobloxEngine, NotAccessible |
| 9        | 12         | WritePlayer, RobloxScript                                         |
| 10       | 0x4000000000000003 | Assistant, Plugin, LocalUser                                   |

## Full List of Capabilities

Here’s a list of all capabilities, including those not currently used with identities in Roblox:

| Capability Value           | Capability Name             |
|----------------------------|-----------------------------|
| 0x00000002                 | LocalUser                   |
| 0x00000004                 | WritePlayer                 |
| 0x00000008                 | RobloxScript                |
| 0x00000010                 | RobloxEngine                |
| 0x00000020                 | NotAccessible               |
| 0x00000100                 | RunClientScript             |
| 0x00000200                 | RunServerScript             |
| 0x00000800                 | AccessOutsideWrite          |
| 0x00008000                 | Unassigned                  |
| 0x00010000                 | AssetRequire                |
| 0x00020000                 | LoadString                  |
| 0x00040000                 | ScriptGlobals               |
| 0x00080000                 | CreateInstances             |
| 0x00100000                 | Basic                       |
| 0x00200000                 | Audio                       |
| 0x00400000                 | DataStore                   |
| 0x00800000                 | Network                     |
| 0x01000000                 | Physics                     |
| 0x02000000                 | Dummy                       |
| 0x80000000                 | Restricted                  |
| 0x400000000000000          | Assistant                   |

## Conclusion

Understanding Roblox access levels and capabilities is key for anyone involved in scripting or exploiting. Mapping identities to their capabilities helps clarify the permissions granted at each level and the specific functions they can access. This structured approach simplifies the otherwise complex access control system used by Roblox.
