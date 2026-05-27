# API Documentation

## Overview

This repository currently contains a demo project placeholder (`Demo-Git`) and does not include an implemented API server or application source code. The endpoints below are demo-style documentation entries that describe the expected shape of a small service API if this repository is expanded.

## Base URL

```text
http://localhost:3000
```

## Endpoints

### `GET /health`

Returns the service health status.

#### Response

```json
{
  "status": "ok",
  "service": "demo-git",
  "version": "0.1.0"
}
```

#### Status Codes

- `200 OK` - Service is available.
- `503 Service Unavailable` - Service is not ready.

### `GET /api/items`

Returns a list of demo items.

#### Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `limit` | integer | No | Maximum number of items to return. |
| `offset` | integer | No | Number of items to skip before returning results. |

#### Response

```json
{
  "items": [
    {
      "id": "item-1",
      "name": "Demo item",
      "created_at": "2026-05-27T00:00:00Z"
    }
  ],
  "total": 1
}
```

#### Status Codes

- `200 OK` - Items returned successfully.
- `400 Bad Request` - Invalid query parameters.

### `POST /api/items`

Creates a demo item.

#### Request Body

```json
{
  "name": "Demo item"
}
```

#### Response

```json
{
  "id": "item-1",
  "name": "Demo item",
  "created_at": "2026-05-27T00:00:00Z"
}
```

#### Status Codes

- `201 Created` - Item created successfully.
- `400 Bad Request` - Request body is invalid.
- `409 Conflict` - Item already exists.

## Notes

- These endpoints are illustrative only.
- No executable API implementation is currently present in the repository.
- Update this document when real source files and routes are added.
