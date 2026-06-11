# Interface: AnnouncementHandlers

Defined in: packages/adapter/dist/index.d.ts:63

Callbacks for [ChainAdapter.watchAnnouncements](ChainAdapter.md#watchannouncements).

## Properties

### onAnnouncement

> **onAnnouncement**: (`announcement`) => `void`

Defined in: packages/adapter/dist/index.d.ts:65

Invoked for each decoded announcement (caller handles its own sync errors).

#### Parameters

##### announcement

[`Announcement`](Announcement.md)

#### Returns

`void`

***

### onError?

> `optional` **onError?**: (`error`) => `void`

Defined in: packages/adapter/dist/index.d.ts:67

Invoked when the underlying watcher stops or errors.

#### Parameters

##### error

`Error`

#### Returns

`void`
