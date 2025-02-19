# WHSender API Documentation



## Sending Messages

**Endpoint:** `https://whsender.com/api/send`

**Method:** `POST`

**Request Body:**
```json
{
    "token": "your_auth_token",
    "user": "your_username",
    "contacts": "recipient_number_or_list",
    "content": "message_text",
    "is_file": 0,
    "is_random_code": 1
}
```

**Response:**
```json
{
    "state": "Started",
    "id": "message_id"
}
```

---

## Sending via Direct URL

**Endpoint:** `https://whsender.com/api/send-url?user=your_username&token=your_auth_token&message=message_text&contacts=recipient_number`

**Method:** `GET`

**Response:**
```json
{
    "state": "Started",
    "id": "message_id"
}
```

---

## Managing Message Queues

### Pause Sending
**Endpoint:** `https://whsender.com/api/pause`
**Method:** `POST`

### Resume Sending
**Endpoint:** `https://whsender.com/api/rasume`
**Method:** `POST`

### Cancel Sending
**Endpoint:** `https://whsender.com/api/cancel/{account_token}`
**Method:** `GET`

### Cancel Specific Message by ID
**Endpoint:** `https://whsender.com/api/cancel-by-id/{token}/{id}`
**Method:** `GET`

---

## Tracking Message Status

### Track Detailed Logs
**Endpoint:** `https://whsender.com/api/track-detail`
**Method:** `POST`

### Track Summary
**Endpoint:** `https://whsender.com/api/track-brief`
**Method:** `POST`

### Track Single Message Detail
**Endpoint:** `https://whsender.com/api/track-detail-single`
**Method:** `POST`

---

## Checking Extension Status

**Endpoint:** `https://whsender.com/api/state`
**Method:** `GET`

**Response:**
```json
{
    "state": "Logged" or "NoSession"
}
```

---

## Downloading Sent Files

**Endpoint:** `https://whsender.com/api/getFile/{file_path}`
**Method:** `GET`

---

## Setting Extension Free State

**Endpoint:** `https://whsender.com/api/iamfree/{token}`
**Method:** `GET`

---

This API provides seamless integration for sending and managing WhatsApp messages efficiently.
