# Group Set Read Only

Sets whether the group is read only or not.

| URL                          | Requires Auth | HTTP Method |
| ---------------------------- | ------------- | ----------- |
| `/api/v1/groups.setReadOnly` | `yes`         | `POST`      |

## Payload

| Argument   | Example              | Required | Description                                       |
| ---------- | -------------------- | -------- | ------------------------------------------------- |
| `roomId`   | `ByehQjC44FwMei5LbX` | Required | The group's id                                    |
| `readOnly` | `true`               | Required | Boolean of whether the group is read only or not. |

## Example Call

```bash
curl -H "X-Auth-Token: 9HqLlyZOugoStsXCUfD_0YdwnNnunAJF8V47U3QHXSq" \
     -H "X-User-Id: aobEdbYhXfu5hkeqG" \
     -H "Content-type: application/json" \
     http://localhost:3000/api/v1/groups.setReadOnly \
     -d '{ "roomId": "ByehQjC44FwMei5LbX", "readOnly": true }'
```

## Example Result

```javascript
{
    "group": {
        "_id": "ByehQjC44FwMei5LbX",
        "name": "testing-private",
        "t": "p",
        "msgs": 0,
        "u": {
            "_id": "aiPqNoGkjpNDiRx6d",
            "username": "goose160"
        },
        "ts": "2017-01-05T18:02:50.754Z",
        "ro": true,
        "sysMes": true,
        "_updatedAt": "2017-01-05T19:02:24.429Z",
        "usernames": [
            "goose160",
            "graywolf336"
        ],
        "joinCodeRequired": true,
        "muted": []
    },
    "success": true
}
```

## Change Log

| Version | Description |
| ------- | ----------- |
| 0.49.0  | Added       |
