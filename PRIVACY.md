# MusicMute Local privacy policy

Updated October 7, 2026

This policy explains how the MusicMute Local Chrome extension and its required
MusicMute Mac companion handle information. Their purpose is to prepare and play
a voice-only audio track synchronized with a supported YouTube watch video.
MusicMute operates this product independently of YouTube and Google.

## Operator and contact

The operator is MusicMute. For support, privacy questions or requests about your
data, use the [MusicMute support page](https://api.music-mute.com/support) or email
[hatemragapdev@gmail.com](mailto:hatemragapdev@gmail.com). Do not send passwords,
authentication tokens, browser cookies, private audio or protected download URLs.
The [account deletion page](https://api.music-mute.com/delete-account) provides
the account-deletion process. The
[MusicMute service privacy policy](https://api.music-mute.com/privacy) covers
other MusicMute clients and the wider account service.

## Information handled by the extension

On supported YouTube watch pages, the extension reads the selected video's
identifier, duration, playback position, volume, mute state, and player and
advertisement state. It uses these to add controls and synchronize vocals with
the video. The extension stores playback and language preferences and a bounded
diagnostic history in the current Chrome profile.

The extension does not read your general browsing history, Google password or
browser cookies. It requests access to supported YouTube pages, local settings,
offscreen audio playback, and the separately installed native companion. It
retrieves prepared audio over a temporary protected connection to a loopback
server on the same Mac.

## Local audio preparation

The extension follows the processing choice saved in the Mac app. With local
processing selected, the Mac app acquires the selected audio online when needed
and runs vocal separation on your Mac. It stores reusable original audio,
prepared vocals, processing metadata and preferences in its local managed
storage. Temporary playback grants connect the extension to those local results.
Automatic local preparation is enabled by default for eligible playing videos;
you can turn it off or set a shorter duration limit.

The downloader operates as a logged-out guest and does not import your Chrome
account, browser profile or cookies. It may use anonymous session data supplied
by YouTube for that guest request. YouTube and its media servers receive the
requests needed to acquire the selected audio, including the Mac's IP address.
Guest access can be refused; the app does not bypass login requirements.

**Local processing includes shared MusicMute service use. It does not mean all
YouTube data stays only on your Mac.** The shared behavior below can operate
while you are signed out of MusicMute.

## Shared YouTube lookup and saving

For a local YouTube request, the Mac app may send the canonical video URL to
MusicMute to look up reusable original audio and vocals. It uses a scoped guest
capability stored in macOS Keychain, so no MusicMute account is required. A
shared hit can download existing vocals instead of acquiring the audio from
YouTube or running separation. A shared original can also be downloaded for
local separation.

When local preparation creates a new YouTube result, video metadata may be sent
before playback to reserve shared saving. After vocals start playing, the Mac
app may upload the original audio, vocals and associated video metadata in the
background, **even while signed out**. Pending saves can resume when the app or
helper starts again. Accepted shared results can be reused by other MusicMute
users to provide the same voice-playback feature. Media transfers use temporary
access grants to private Cloudflare R2 storage; the storage bucket is not public.
MusicMute services control access, including scoped guest playback grants.

Accepted shared YouTube originals, vocals and metadata have no automatic expiry.
They remain available after local cache clearing, job deletion or account/guest
deletion. Stopping playback does not delete a shared result or cancel an already
released background save. Signing out does not disable this shared behavior.
There is no separate per-video opt-in control for shared saving in this version.

## Optional account and cloud use

A MusicMute account is optional for local playback and shared YouTube reuse.
Signing into the Mac app can attach shared YouTube references to your account
Library. The native app handles authentication with MusicMute and Firebase/Google;
the account service handles information such as your account identifier, profile
name, email when available, verification state and linked sign-in provider. Account
credentials remain in the Mac app and are not sent to the Chrome extension.

When MusicMute cloud is selected in the app, manually starting a video sends its
canonical YouTube watch URL to MusicMute using that saved choice, without a
per-video confirmation in Chrome. MusicMute services acquire audio or reuse a
shared result. For this cloud request, the Mac does not acquire and upload the
original audio. Cloud processing requires the app's signed-in account and uses
its processing allowance. The resulting vocals are downloaded to the Mac for
playback. Automatic preparation never submits new cloud processing.

Personal audio or video files processed in the Mac app use its account-private
saving path and are not contributed to the shared YouTube catalog. Account
records can include input and result audio, filenames, duration, size, processing
history, source URLs and metadata. Saving and access are subject to the account's
permissions and storage limits.

## Services that receive information

- MusicMute services receive the selected canonical YouTube URL and necessary
  video or processing metadata for shared lookup, shared saving or selected cloud
  processing. They receive audio when the flows above upload or process it.
- Cloudflare R2 stores media in private storage and handles protected transfers.
  Account and job records are stored in MusicMute's service database, including
  MongoDB. Hosting, network, security and audio-acquisition providers process the
  requests needed to deliver these features, which can include URLs, IP addresses,
  request metadata and security/session records.
- Firebase/Google handles optional account authentication. Signing into MusicMute
  does not authenticate the isolated guest YouTube downloader.
- YouTube and its media servers handle guest audio-acquisition requests.
- GitHub and its download infrastructure receive requests, IP addresses and
  request metadata when you download the app or runtime components. The voice
  model is downloaded from its approved upstream GitHub release. These download
  hosts are not the destination for user audio or diagnostic reports.

Information is used to provide voice playback, selected processing, shared
YouTube reuse and account Library features, and to operate and protect those
services. This extension does not sell user data, use it for advertising or send
it to analytics services. Information may also be disclosed when required by law
or necessary to investigate abuse or protect users and the service.

## Diagnostics and security

Extension and local companion diagnostics remain local. There is no automatic
upload of their diagnostic reports, analytics or telemetry. Exporting diagnostics
creates a local report; you choose whether to share it. The report omits audio,
credentials, browser cookies and private media URLs. Separately, online services
can retain operational and security records for requests they receive.

Remote service and media transfers use HTTPS or secure WebSockets, as applicable.
Account credentials and guest capabilities are handled by the native app, with
Keychain storage. Local native messaging and protected loopback playback occur
on the same Mac. Browser executable code is bundled with the extension; setup
downloads checksum-verified native runtime components and model data for the
companion. These security measures do not guarantee absolute security.

## Your controls and retention

You can turn automatic preparation on or off, choose a duration limit, switch
between vocals and original sound, or stop playback. These playback controls do
not delete previously saved data or accepted shared results.

Use **Stop playback and clear local cache** in the extension's local tools to
clear its managed reusable results. Pending background saves and account Library
items are managed separately by the Mac app. Local cached data is subject to its
managed cache budget. Ordinary app replacement preserves the installed runtime,
model and app data. Removing the Chrome extension removes its Chrome settings;
it does not uninstall the Mac app or delete its files, cloud Library or accepted
shared YouTube results.

Privately uploaded files and account history can be removed through the relevant
account controls or account deletion, subject to processing cleanup. An accepted
account-deletion request immediately blocks account access and starts a 15-day
recovery period. Permanent cleanup starts after that deadline. Shared public-link
originals and results remain; deletion removes the account's records and access
to them. Exported copies and source material held by another provider remain
under that user's or provider's control. Operational logs and backups can remain
for their normal service lifecycle or when preservation is required for security
or law, as described in the MusicMute service privacy policy. Contact support for
privacy or deletion questions about data that the available controls do not remove.

## Chrome Web Store Limited Use

MusicMute Local uses and transfers user data only for its disclosed voice
playback, processing, shared YouTube reuse and account Library features, in
accordance with the
[Chrome Web Store User Data Policy](https://developer.chrome.com/docs/webstore/program-policies/user-data-faq),
including its Limited Use requirements. User data is not used or transferred for
personalized, retargeted or interest-based advertising. Human access to user data
is limited to the policy's permitted situations, such as your agreement to
specific support access, security investigations or compliance with law.

## Policy changes

Material changes will be published here with an updated date. The disclosures
above describe the current Chrome extension and required Mac companion; they do
not grant permission to download or process content owned by someone else. Use
only material you own or are authorized to process.
