# Design Guidelines: Social Media Monitoring & Data Leak Detection Platform

## Design Approach

**Selected Approach**: Design System-Based with Security Dashboard Inspiration

**Justification**: As an enterprise security monitoring tool requiring data clarity, trust, and operational efficiency, this application follows established patterns from security operations centers (SOCs) and monitoring platforms. Drawing inspiration from Splunk, Datadog, and modern security dashboards while maintaining a contemporary, professional aesthetic.

**Core Principles**:
- Information hierarchy and scannable data presentation
- Trust through professional polish and stability
- Alert prominence without alarm fatigue
- Real-time monitoring aesthetic

## Color Palette

### Dark Mode (Primary)
- **Background**: 222 15% 8% (deep charcoal base)
- **Surface**: 222 12% 12% (elevated cards/panels)
- **Surface Elevated**: 222 10% 16% (interactive elements)
- **Primary Brand**: 210 95% 55% (professional security blue)
- **Accent/Alert Critical**: 0 85% 60% (urgent red for critical alerts)
- **Accent/Alert Warning**: 38 92% 55% (amber for warnings)
- **Accent/Alert Success**: 142 76% 45% (green for resolved/safe)
- **Text Primary**: 0 0% 95%
- **Text Secondary**: 0 0% 70%
- **Border**: 222 10% 20%

### Light Mode
- **Background**: 0 0% 98%
- **Surface**: 0 0% 100%
- **Surface Elevated**: 210 20% 98%
- **Primary Brand**: 210 95% 48%
- **Text Primary**: 222 15% 15%
- **Text Secondary**: 222 10% 45%

## Typography

**Font Families**:
- **Primary (UI)**: Inter (Google Fonts) - Clean, modern sans-serif for data readability
- **Monospace (Data)**: JetBrains Mono (Google Fonts) - For URLs, IPs, usernames, timestamps

**Hierarchy**:
- H1 (Dashboard Title): 2xl/3xl, font-semibold
- H2 (Section Headers): xl/2xl, font-semibold
- H3 (Card Titles): lg/xl, font-medium
- Body: base/sm, font-normal
- Data Labels: sm/xs, font-medium, uppercase tracking-wide
- Metrics/Stats: 3xl/4xl, font-bold (for KPIs)

## Layout System

**Spacing Primitives**: Tailwind units of **2, 4, 6, 8, 12, 16** (e.g., p-4, gap-6, mb-8)

**Grid Structure**:
- Main dashboard: 12-column grid with sidebar
- Sidebar: Fixed 64-72 width (16-18 units)
- Content area: Responsive grid using grid-cols-1 md:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4
- Full-width monitoring feeds: Single column with max-w-7xl

**Containers**: 
- Dashboard wrapper: px-4 md:px-6 lg:px-8, py-6
- Card padding: p-6
- Dense data tables: p-4

## Component Library

### Navigation
- **Sidebar Navigation**: Fixed left sidebar with icon + label navigation, collapsible on mobile
- **Top Bar**: Logo, global search, notification bell (with badge counter), user profile dropdown, theme toggle
- **Breadcrumbs**: For nested views (Monitoring > Social Media > Twitter Alerts)

### Core Dashboard Components

**Alert Feed Cards**:
- Card with severity indicator (left border: 4px colored stripe)
- Timestamp, platform icon, alert type, preview snippet
- Quick actions: View details, Mark safe, Escalate
- Hover: Subtle lift with shadow

**Metrics Dashboard**:
- KPI cards in grid: Total scans, Active threats, Data exposed records, Platforms monitored
- Large number display with trend indicators (↑↓ arrows with percentage)
- Mini sparkline charts for trends

**Real-Time Activity Monitor**:
- Live feed table/list showing recent detections
- Alternating row backgrounds for scanability
- Status badges (Critical, High, Medium, Low)
- Platform icons (Twitter, LinkedIn, Facebook, Instagram)

**Threat Visualization**:
- Horizontal bar charts for threat distribution by platform
- Donut chart for threat severity breakdown
- Timeline graph for incidents over time
- Use Chart.js or Recharts via CDN

**Data Tables**:
- Sortable headers with sort indicators
- Row hover states
- Pagination controls
- Density toggle (comfortable/compact views)
- Export functionality button

### Forms & Filters

**Search & Filter Panel**:
- Global search bar with autocomplete
- Multi-select dropdowns for platforms, severity, date ranges
- Tag-based active filters with clear individual/all options
- Collapsible advanced filters section

**Configuration Forms**:
- Clean two-column layouts for settings
- Toggle switches for enable/disable features
- Input fields with helper text and validation states
- Save/Cancel button pairs (primary/ghost)

### Interactive Elements

**Buttons**:
- Primary: Solid primary color, white text
- Secondary: Outline with primary color
- Ghost: Transparent with hover background
- Danger: Red for destructive actions
- Sizes: sm, md, lg

**Badges**:
- Severity levels with appropriate colors
- Platform tags (subtle backgrounds matching brand colors)
- Count indicators (rounded pills)

**Modals/Overlays**:
- Alert detail modal: Full breach information, affected data, recommended actions
- Confirmation dialogs: For critical actions
- Slide-over panels: For detailed monitoring feed inspection

## Visual Enhancements

**Icons**: Heroicons (outline for navigation, solid for status indicators)

**Micro-interactions** (Minimal):
- Smooth fade-ins for new alerts (300ms)
- Pulse animation for "live" indicators
- Loading skeleton states for data fetching
- Hover lift on cards (translate-y-1)

**Data Visualization**:
- Use muted colors for non-critical data
- Highlight critical/anomalous data points
- Consistent color coding across all charts

## Images

**Hero Section**: No traditional hero image. Dashboard leads with live data and metrics immediately visible.

**Platform Icons/Logos**: Small social media platform logos (16x16 to 24x24) next to entries - use Font Awesome brand icons or placeholder circles with initials.

**Illustration Use**: Optional empty states (e.g., "No alerts detected" with simple shield icon illustration).

**Avatar Placeholders**: For detected user profiles in monitoring feed - circular 32x32 or 40x40 with initials on colored background.

## Accessibility & Responsiveness

- WCAG AA contrast ratios throughout
- Keyboard navigation for all interactive elements
- Screen reader labels for icons and data visualizations
- Responsive breakpoints: sm (640px), md (768px), lg (1024px), xl (1280px)
- Mobile: Stacked single-column layouts, collapsible sidebar as drawer
- Focus indicators on all interactive elements

This design creates a professional, trustworthy security monitoring platform that prioritizes data clarity and operational efficiency while maintaining modern aesthetics.