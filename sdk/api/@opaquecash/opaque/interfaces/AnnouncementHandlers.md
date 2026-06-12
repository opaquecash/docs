# Interface: AnnouncementHandlers

Defined in: packages/adapter/dist/index.d.ts:63

Callbacks for [ChainAdapter.watchAnnouncements](/sdk/api/@opaquecash/opaque/interfaces/ChainAdapter.md#watchannouncements).

## Properties

### onAnnouncement

> **onAnnouncement**: (`announcement`) => `void`

Defined in: packages/adapter/dist/index.d.ts:65

Invoked for each decoded announcement (caller handles its own sync errors).

#### Parameters

##### announcement

[`Announcement`](/sdk/api/@opaquecash/opaque/interfaces/Announcement.md)

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
