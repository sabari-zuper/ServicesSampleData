# iOS SwiftUI Interview Task

## Technical Requirements

Build a **Listing and Detail Screen** using SwiftUI that displays a list of services with search functionality and detailed views. The app should demonstrate proficiency in modern iOS development patterns, including SwiftUI, Combine framework, and native iOS design principles.

| List | Details |
|---------|---------|
|![image (1)](https://github.com/user-attachments/assets/16683613-ff6d-4642-b151-d3e7a18fe50e)|![image (2)](https://github.com/user-attachments/assets/bfe16b7a-235e-4e5c-8873-4cbcb9e4043d)|


**Primary Evaluation Focus** 
- SwiftUI Implementation 
- List Management 
- Search with Combine 
- Navigation Patterns 
- Pull-to-Refresh

## Technical Requirements

- **Minimum Deployment Target:** iOS 16.0
- **SPM:** Use SPM package, don't drag and drop the package
- **UI Framework:** SwiftUI (use NavigationStack, List, etc.)
- **Search Implementation:** Combine framework with debounce functionality (300ms delay)
- **Date Formatting:** Smart formatting - Today, Tomorrow, Yesterday, dd/mm/yyyy
- **Refresh Functionality:** Pull-down to refresh with async implementation
- **Architecture:** MVVM pattern with proper state management
- **State Management:** Proper use of @State, @StateObject, @ObservedObject
- **No External Libraries:** Use only native iOS frameworks
- **Use Tabler Icons:** https://tablericons.com
- **Maps:** Use default AppleMaps with marker(Harcode the coordinates)



## Screen Specifications

### Screen 1: Services List

**🔍 Search Functionality:** Implement real-time search using Combine framework with 300ms debounce. Search should filter across service title, customer name, and description fields.

**📝 List Implementation:** Use SwiftUI List with custom rows. Each row should display title, subtitle, description, status badge, priority indicator, and formatted date.

**🔄 Pull-to-Refresh:** Implement using SwiftUI's refreshable modifier with async data loading. Simulate delay of 2-3 seconds.

**🎨 Visual Design:** Follow iOS design guidelines with proper spacing, typography, and native iOS styling patterns.

### Screen 2: Service Details

**🧭 Navigation:** Implement proper navigation using NavigationStack with back button functionality and smooth data passing between views.

**📋 Content Sections:** Display service information in clearly organized sections: Description, Scheduled Time, Location, and Service Notes.

**📱 iOS Patterns:** Follow native iOS navigation patterns, proper header styling, and standard detail view layout.

## 📅 Date Formatting Specifications

### 📋 Required Date Formats

- **Today:** "Today, 2:30 PM"
- **Tomorrow:** "Tomorrow, 10:00 AM"
- **Yesterday:** "Yesterday, 3:00 PM"
- **Other dates:** "15/11/2024, 2:30 PM"
- **Time format:** 12-hour format with AM/PM
- **Date format:** DD/MM/YYYY for dates beyond yesterday/tomorrow/today

## 🔍 Search Implementation Requirements

- **Framework:** Use Combine framework with Publishers and Subscribers
- **Debounce:** Implement 300ms debounce to avoid excessive filtering
- **Case Insensitive:** Search should be case-insensitive across all text fields
- **Fields:** Search across title, customerName, and description
- **Performance:** Optimize for smooth scrolling and responsive search
- **Clear Search:** Handle empty search state properly
