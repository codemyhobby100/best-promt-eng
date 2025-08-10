# Rocket.new Prompt Engineering Guide

## Table of Contents
- [Core Principles](#core-principles)
- [Website Development Prompts](#website-development-prompts)
- [App Development Prompts](#app-development-prompts)
- [Error Prevention Strategies](#error-prevention-strategies)
- [Token Management](#token-management)
- [Performance Optimization](#performance-optimization)

## Core Principles

### Prompt Structure Framework
```
[ROLE] + [CONTEXT] + [SPECIFIC_REQUIREMENTS] + [CONSTRAINTS] + [OUTPUT_FORMAT]
```

### Essential Elements
- Define precise technical specifications
- Include error handling requirements
- Specify responsive design parameters
- Detail accessibility standards
- Outline security requirements

## Website Development Prompts

### Landing Page Template
```
You are a senior full-stack developer building a conversion-optimized landing page.

REQUIREMENTS:
- Hero section with compelling headline and CTA button
- Social proof section with testimonials
- Features section with 3-column grid layout
- FAQ accordion component
- Contact form with validation
- Mobile-first responsive design

TECHNICAL SPECS:
- HTML5 semantic structure
- CSS Grid and Flexbox layouts
- JavaScript form validation
- 90+ Lighthouse performance score
- WCAG 2.1 AA accessibility compliance

CONSTRAINTS:
- Single HTML file with embedded CSS/JS
- No external dependencies
- Maximum file size: 50KB
- Load time under 3 seconds

OUTPUT:
Complete HTML file with inline styles and scripts.
Include comments explaining key sections.
```

### E-commerce Store Template
```
You are an e-commerce development specialist creating a product catalog page.

FEATURES REQUIRED:
- Product grid with image, title, price, rating
- Filter sidebar (category, price range, brand)
- Search functionality with autocomplete
- Sort options (price, popularity, rating)
- Shopping cart with quantity controls
- Wishlist functionality
- Product quick view modal

TECHNICAL IMPLEMENTATION:
- Local storage for cart persistence
- Debounced search input
- Lazy loading for product images
- Skeleton loaders for better UX
- Toast notifications for user actions

DATA STRUCTURE:
products = [
  {
    id: string,
    title: string,
    price: number,
    image: string,
    category: string,
    rating: number,
    inStock: boolean
  }
]

ERROR HANDLING:
- Empty search results message
- Network failure fallbacks
- Invalid product data handling
- Form validation with specific error messages

PERFORMANCE:
- Virtual scrolling for large product lists
- Image optimization and WebP support
- CSS and JS minification
- Critical CSS inlined
```

### Portfolio Website Template
```
You are a creative developer building a portfolio showcase website.

SECTIONS REQUIRED:
- Animated hero with your name and title
- About section with professional photo
- Skills section with proficiency bars
- Portfolio grid with project previews
- Contact form with email integration
- Footer with social media links

ANIMATIONS:
- Smooth scroll between sections
- Fade-in effects on scroll
- Typing animation for hero text
- Hover effects on portfolio items
- Loading animations for transitions

TECHNICAL DETAILS:
- Intersection Observer for scroll animations
- CSS transforms for smooth transitions
- Debounced scroll event handlers
- Progressive image loading
- SEO-optimized meta tags

ACCESSIBILITY:
- Reduced motion preferences respected
- Keyboard navigation support
- Screen reader friendly content
- High contrast color scheme
- Focus indicators visible
```

## App Development Prompts

### Task Management App
```
You are a productivity app developer creating a task management system.

CORE FEATURES:
- Create, edit, delete tasks
- Mark tasks as complete
- Task categories with color coding
- Due date assignments
- Priority levels (high, medium, low)
- Search and filter functionality
- Progress tracking dashboard

ADVANCED FEATURES:
- Drag and drop task reordering
- Bulk task operations
- Export tasks to CSV
- Dark/light theme toggle
- Offline functionality with sync

DATA MANAGEMENT:
- Local storage with backup
- Data validation for all inputs
- Unique ID generation for tasks
- State management for UI updates
- Conflict resolution for sync

USER INTERFACE:
- Clean, minimal design
- Intuitive navigation
- Modal dialogs for task editing
- Responsive layout for mobile
- Loading states for all actions

ERROR PREVENTION:
- Input sanitization
- Required field validation
- Duplicate task prevention
- Storage quota management
- Graceful degradation
```

### Weather App
```
You are a mobile app developer creating a weather application.

PRIMARY FEATURES:
- Current weather display
- 5-day forecast
- Hourly predictions
- Location-based weather
- Multiple city support
- Weather alerts and notifications

UI COMPONENTS:
- Weather cards with icons
- Temperature charts
- UV index indicator
- Humidity and wind displays
- Sunrise/sunset times
- Air quality index

API INTEGRATION:
- OpenWeatherMap API calls
- Geolocation services
- Error handling for API failures
- Rate limiting compliance
- Caching for offline access

DESIGN SPECIFICATIONS:
- Weather-based background changes
- Animated weather icons
- Smooth transitions between views
- Pull-to-refresh functionality
- Skeleton screens while loading

PERFORMANCE:
- Efficient API calls
- Image optimization
- Lazy loading for forecasts
- Memory management
- Battery usage optimization
```

### Social Media Dashboard
```
You are developing a social media management dashboard.

DASHBOARD FEATURES:
- Multi-platform post scheduling
- Analytics and engagement metrics
- Content calendar view
- Team collaboration tools
- Hashtag suggestions
- Image editing capabilities

POST COMPOSER:
- Rich text editor
- Image/video upload
- Post preview for each platform
- Character count with platform limits
- Optimal posting time suggestions
- Bulk upload functionality

ANALYTICS SECTION:
- Engagement rate charts
- Follower growth tracking
- Top performing content
- Audience demographics
- Competitor analysis
- Custom date ranges

TECHNICAL REQUIREMENTS:
- OAuth integration for platforms
- Real-time data updates
- Responsive charts and graphs
- File upload with progress bars
- Notification system for scheduled posts

SECURITY:
- Token-based authentication
- HTTPS-only connections
- Input validation and sanitization
- XSS prevention measures
- CSRF protection
```

## Error Prevention Strategies

### Input Validation Framework
```javascript
const validateInput = {
  email: (email) => /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email),
  phone: (phone) => /^\+?[\d\s\-\(\)]+$/.test(phone),
  required: (value) => value && value.trim().length > 0,
  minLength: (value, min) => value.length >= min,
  maxLength: (value, max) => value.length <= max
};
```

### Error Handling Patterns
- Try-catch blocks for all async operations
- Fallback UI states for failed requests
- User-friendly error messages
- Automatic retry mechanisms
- Logging for debugging purposes

### Type Safety Measures
- Input type checking
- API response validation
- Null/undefined checks
- Array bounds validation
- Object property existence verification

## Token Management

### Efficient Prompting Strategies
- Break complex requirements into smaller chunks
- Use specific technical terms to reduce ambiguity
- Reference established patterns and frameworks
- Include exact code examples when needed
- Prioritize critical features first

### Context Optimization
- Remove unnecessary explanations
- Use bullet points for requirements
- Include only essential technical details
- Reference standard implementations
- Avoid redundant specifications

### Iterative Refinement
- Start with core functionality
- Add features incrementally
- Test each component individually
- Refine based on specific feedback
- Document changes for future reference

## Performance Optimization

### Code Optimization Techniques
- Minimize DOM manipulations
- Use event delegation
- Implement lazy loading
- Optimize images and assets
- Reduce HTTP requests

### Caching Strategies
- Browser caching for static assets
- Local storage for user data
- Service worker for offline access
- API response caching
- Progressive enhancement

### Monitoring and Metrics
- Core Web Vitals tracking
- Performance budget enforcement
- Bundle size analysis
- Runtime performance profiling
- User experience metrics

## Common App Features by Niche

### E-commerce Apps
- Product catalog with search/filter
- Shopping cart and checkout
- User accounts and profiles
- Order tracking
- Payment integration
- Reviews and ratings
- Wishlist functionality
- Inventory management

### Education Apps
- Course catalog and enrollment
- Video player with progress tracking
- Quiz and assessment system
- Discussion forums
- Progress dashboards
- Certification generation
- Offline content access
- Multi-language support

### Healthcare Apps
- Appointment scheduling
- Patient records management
- Symptom checker
- Medication reminders
- Telemedicine integration
- Health data visualization
- Emergency contact system
- Privacy compliance (HIPAA)

### Finance Apps
- Account balance display
- Transaction history
- Budget tracking
- Bill payment system
- Investment portfolio
- Security authentication
- Spending analytics
- Financial goal setting

### Food Delivery Apps
- Restaurant discovery
- Menu browsing
- Order customization
- Real-time tracking
- Payment processing
- Rating and review system
- Delivery scheduling
- Loyalty programs

## Implementation Best Practices

### Development Workflow
1. Define project scope and requirements
2. Create wireframes and user flows
3. Set up development environment
4. Implement core functionality first
5. Add advanced features incrementally
6. Test across devices and browsers
7. Optimize for performance
8. Deploy with monitoring

### Quality Assurance
- Unit testing for critical functions
- Integration testing for user flows
- Cross-browser compatibility testing
- Mobile responsiveness verification
- Accessibility audit
- Performance testing
- Security vulnerability assessment
- User acceptance testing

### Documentation Requirements
- API documentation
- Component usage examples
- Setup and installation guide
- Troubleshooting section
- Contributing guidelines
- Version changelog
- License information
- Contact details for support
