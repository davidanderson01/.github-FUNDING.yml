# Snapshots Configuration and Management

This document provides details about the snapshot configuration and management system. It is designed to assist with project management and ensure alignment with Azure best practices.

---

## Overview

Snapshots are used to capture the state of your project at specific points in time. This system allows you to manage snapshots efficiently, ensuring compliance with retention policies and storage optimization.

---

## Configuration Details

The configuration file (`config.json`) includes the following settings:

- **Snapshots**:
  - Each snapshot includes metadata such as `id`, `path`, `description`, `timestamp`, and `version`.
  - Snapshots can have additional metadata, including `creator`, `size`, and `status` (e.g., `active`, `inactive`, `archived`).

- **Retention Policy**:
  - Snapshots are retained based on the specified policy (`standard`) and duration (`30d`).

- **Global Settings**:
  - `maxSnapshots`: The maximum number of snapshots allowed before cleanup.
  - `compressionEnabled`: Indicates whether snapshot compression is enabled to save storage space.
  - `autoCleanup`: Automatically removes old snapshots when the maximum limit is reached.

---

## Azure Best Practices

If this project involves Azure, follow these guidelines:

- Use the `azure_development-get_best_practices` tool to validate configurations and workflows.
- Avoid including sensitive information (e.g., secrets or credentials) in any project files.
- Ensure that the retention policy aligns with Azure's recommendations for secure and efficient management. Refer to [Azure Best Practices](https://learn.microsoft.com/en-us/azure/architecture/best-practices/) for more details.

---

## Example Configuration

Below is an example of the snapshot configuration file:

```json
{
  "snapshots": [
    {
      "id": "snap-000",
      "path": ".snapshots/config.json",
      "description": "Configuration file for snapshot management",
      "timestamp": "2023-10-01T12:00:00Z",
      "version": "1.0.0"
    },
    {
      "id": "snap-001",
      "path": ".snapshots/config.json",
      "description": "Configuration file for snapshot management",
      "timestamp": "2023-10-01T12:00:00Z",
      "version": "1.0.0",
      "metadata": {
        "creator": "system",
        "size": 1024,
        "status": "active"
      },
      "retention": {
        "policy": "standard",
        "duration": "30d"
      }
    }
  ],
  "version": "1.0.0",
  "lastUpdated": "2023-10-01T12:00:00Z",
  "config": {
    "maxSnapshots": 100,
    "compressionEnabled": true,
    "autoCleanup": true
  }
}
