# ServicesSampleData

A minimal Swift Package Manager library that provides randomly generated sample data for iOS SwiftUI interview tasks.

## Installation

### Swift Package Manager

Add this package to your Xcode project:

1. File → Add Package Dependencies
2. Enter package URL: `https://github.com/yourcompany/ServicesSampleData`
3. Select version and add to target

Or add to your `Package.swift`:

```swift
dependencies: [
    .package(url: "https://github.com/sabari-zuper/ServicesSampleData.git", from: "1.0.0")
]
```

## Usage

### Import and Generate Data

```swift
import ServicesSampleData

// Generate 15 random services (default)
let services = SampleData.generateServices()

// Generate specific number of services
let moreServices = SampleData.generateServices(count: 20)

// Generate single service
let singleService = SampleData.generateSingleService()


## Data Models

### Service

```swift
struct Service: Identifiable, Codable, Hashable {
    let id: String
    let title: String
    let customerName: String
    let description: String
    let status: ServiceStatus
    let priority: Priority
    let scheduledDate: String  // ISO8601 format: "2024-11-15T14:30:00Z"
    let location: String
    let serviceNotes: String
}
```

### ServiceStatus

- `.active`
- `.scheduled`  
- `.completed`
- `.inProgress`
- `.urgent`

### Priority

- `.low`
- `.medium`
- `.high`
- `.critical`

## Date Handling

**Important**: The `scheduledDate` field is a **String** in ISO8601 format (e.g., "2024-11-15T14:30:00Z").

**You need to implement:**
1. **Parse string to Date** using ISO8601DateFormatter
2. **Format Date according to requirements:**
   - "Today, 2:30 PM"
   - "Tomorrow, 10:00 AM"  
   - "Yesterday, 3:00 PM"
   - "15/11/2024, 2:30 PM"


**Features:**
- Unique service/customer combinations (no duplicates)
- Services sorted by scheduled date
- Realistic business hours (8 AM - 6 PM)
- 15-minute time intervals
- Mix of all statuses and priorities
- ISO8601 formatted date strings

## What You Need to Implement

This package provides only raw data generation. You need to implement:

- **Date parsing and formatting** (ISO8601 to Today/Tomorrow/Yesterday/DD/MM/YYYY)
- **Search functionality** with Combine framework and debounce
- **Pull-to-refresh** functionality
- **List filtering** by status/priority
- **SwiftUI views** and navigation
- **State management** with @State, @StateObject, @ObservedObject
