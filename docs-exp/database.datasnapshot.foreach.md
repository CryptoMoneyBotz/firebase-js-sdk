<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [@firebase/database](./database.md) &gt; [DataSnapshot](./database.datasnapshot.md) &gt; [forEach](./database.datasnapshot.foreach.md)

## DataSnapshot.forEach() method

Enumerates the top-level children in the `DataSnapshot`<!-- -->.

Because of the way JavaScript objects work, the ordering of data in the JavaScript object returned by `val()` is not guaranteed to match the ordering on the server nor the ordering of `onChildAdded()` events. That is where `forEach()` comes in handy. It guarantees the children of a `DataSnapshot` will be iterated in their query order.

If no explicit `orderBy*()` method is used, results are returned ordered by key (unless priorities are used, in which case, results are returned by priority).

<b>Signature:</b>

```typescript
forEach(action: (child: DataSnapshot) => boolean | void): boolean;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  action | (child: [DataSnapshot](./database.datasnapshot.md)<!-- -->) =&gt; boolean \| void | A function that will be called for each child DataSnapshot. The callback can return true to cancel further enumeration. |

<b>Returns:</b>

boolean

true if enumeration was canceled due to your callback returning true.
