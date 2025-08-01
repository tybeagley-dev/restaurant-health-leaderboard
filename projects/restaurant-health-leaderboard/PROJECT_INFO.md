# Restaurant Health Score Leaderboard Project

## Overview
A live leaderboard application for tracking and displaying restaurant health inspection scores, designed for trade show demonstrations.

## Project Details
- **Created**: July 2025
- **Purpose**: Trade show demonstration tool
- **Type**: Single-page web application
- **Technology**: HTML, CSS, JavaScript (vanilla)

## Git History
Recent commits related to this project:
- `7b80d31` - Make delete buttons more visible and prominent
- `34a332e` - Add individual row deletion and instant clear functionality  
- `26d8613` - Add restaurant health score leaderboard for trade show

## Features
### Core Functionality
- Add restaurants with name, location, and health score (0-100)
- Automatic ranking based on health scores
- Live leaderboard display with visual ranking indicators
- Individual entry deletion
- Clear all entries functionality

### UI/UX Features
- Responsive design with mobile support
- Gradient backgrounds and modern styling
- Animated entry additions with pulse effects
- Color-coded health scores:
  - Excellent (90-100): Green gradient
  - Good (80-89): Light green gradient
  - Fair (70-79): Orange gradient
  - Poor (0-69): Red gradient
- Prominent ranking badges (Gold, Silver, Bronze)
- Hover effects and smooth transitions

## Technical Implementation
### Architecture
- Single HTML file with embedded CSS and JavaScript
- Client-side only (no backend required)
- In-memory data storage (resets on page refresh)

### Key Components
1. **Input Section**: Form for adding new restaurant entries
2. **Leaderboard Display**: Sorted list of restaurants by score
3. **Interactive Controls**: Delete individual entries or clear all

### Data Structure
```javascript
{
  name: "Restaurant Name",
  location: "City, State", 
  score: 85,
  timestamp: 1722384000000
}
```

## File Structure
```
restaurant-health-leaderboard/
├── index.html          # Main application file
└── PROJECT_INFO.md     # This documentation file
```

## Usage
1. Open `index.html` in a web browser
2. Enter restaurant name, location, and health score (0-100)
3. Click "Add to Board" or press Enter
4. View live rankings with automatic sorting
5. Delete individual entries using the × button
6. Clear all entries using "Clear All" button

## Trade Show Context
This application was specifically designed for trade show demonstrations, featuring:
- Professional appearance with modern gradients
- Large, readable text and buttons
- Engaging animations for audience attention
- Simple, intuitive interface for quick demonstrations
- Responsive design for various display sizes

## Development Notes
- Pure vanilla JavaScript implementation (no frameworks)
- CSS Grid and Flexbox for responsive layout
- Smooth animations using CSS transitions and keyframes
- Accessibility considerations with proper labeling
- Input validation for data integrity