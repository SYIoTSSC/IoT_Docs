## IoTSSC Gateway-Cloud Communication Specification (REST API)
### Version 1

### Authentication

**Register a device**
```
GET /auth/get_token/<device_identifier>
BODY:
{
    token: <token>
}
```

* <device_identifier> will be embedded in the device's firmware, and should be kept secret.

**Data Upload**
POST: /device/send/
HEADER:
    Authorization: Bearer <token>
BODY:
{
    data: {TBD}
}
