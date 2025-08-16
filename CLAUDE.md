# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

**GEO资产库内容操作系统 (EurekaCOS)** is a comprehensive content management and distribution platform designed for multi-channel content operations. The system enables businesses to create standardized content assets, automate distribution across multiple channels, and optimize content performance through data-driven insights using AI-powered GEO (Generative Engine Optimization) techniques.

## Architecture

This is a frontend-only demonstration project consisting of HTML files that showcase the various modules of the GEO system:

- **诊断模块** (Diagnostic): `00a-00c` - AI search channel diagnostics and GEO optimization strategies
- **建库模块** (Asset Library): `01a-01e` - Content asset creation and management
- **编排模块** (Content Orchestration): `02a-02b` - Content assembly and marketplace
- **分发模块** (Distribution): `03a-03c` - Omnichannel publishing and A/B testing
- **承接模块** (Conversion): `04a-04b` - User journey and conversion management
- **回流模块** (Analytics): `05a-05b` - Real-time monitoring and AI optimization
- **AI辅助模块** (AI Assistant): `06a-06c` - AI-powered tools and collaboration
- **系统管理** (System): `07` - System settings and configuration

## Development Commands

Since this is a static HTML project, no build or compilation is required:

```bash
# To serve the files locally with a simple HTTP server:
python3 -m http.server 8000

# Alternative with Node.js:
npx http-server -p 8000

# For auto-reload during development:
npx browser-sync start --server --files "*.html"
```

## Repository Information

- **Git Repository**: Yes (main branch)
- **Remote**: https://github.com/keevingfu/eurekacos.git
- **Dependencies**: None - pure static HTML/CSS/JS project
- **Build Process**: None required

## Key Technologies

- **Frontend**: Pure HTML/CSS/JavaScript
- **Design System**: Custom CSS variables for consistent theming
- **Layout**: Flexbox and Grid for responsive design
- **Interactivity**: Vanilla JavaScript for UI interactions
- **Charts**: Canvas-based chart implementations

## Code Structure

Each HTML file represents a complete module interface:
- Self-contained with inline styles and scripts
- Responsive design with mobile considerations
- Mock data for demonstration purposes
- Interactive elements to showcase functionality

## Module Navigation System

The project includes two navigation entry points:
- `login.html` - Login page (entry point)
- `index.html` - Main portal with comprehensive navigation menu (requires authentication)
- Individual module files - Direct access to specific functionality

### Authentication Flow
- Users must log in through `login.html` before accessing the system
- Demo credentials: `admin/admin123` or `demo/demo123`
- Session managed via localStorage
- Logout functionality available in the user dropdown menu

### Navigation Updates

The `index.html` portal has been enhanced with:
- **诊断** (Diagnostic) menu added before **建库** menu
- Submenus link to diagnostic analysis pages
- System settings corrected to point to `07-system-settings-console.html`

### Specialized Module Groups

1. **Diagnostic Analysis Tools** (NEW):
   - `00a-eureka-ai-channel-diagnostic.html` - AI搜索渠道诊断
   - `00b-eureka-geo-opportunity.html` - GEO市场机会分析
   - `00c-eureka-geo-strategy.html` - GEO优化策略

2. **Marketplace Components**:
   - `marketplace-*.html` - Various marketplace features including templates, statistics, collaboration, and workflow management
   - `marketplace-home.html` - New marketplace homepage
   - `02b-content-marketplace.html` - Enhanced with iframe navigation for marketplace pages

3. **Special Purpose Pages**:
   - `eureka-geo-dam.html` - Advanced visualization dashboard with cosmic theme

## Important Design Patterns

1. **Color System**: Uses CSS variables (`--primary`, `--success`, `--warning`, etc.) for consistent theming
2. **Card-based Layout**: Information organized in cards for better visual hierarchy
3. **Status Indicators**: Color-coded badges and tags for quick status recognition
4. **Data Visualization**: Canvas-based charts and graphs for metrics display
5. **Action-oriented UI**: Clear CTAs and workflow guidance

## JavaScript Patterns

- Event delegation for dynamic content
- Mock data generation for demonstration
- Chart rendering using native Canvas API
- Tab/navigation state management
- Form interaction handlers

## Documentation References

- `geo-product-design.md` - Comprehensive product design document
- `geo-asset-flowcharts.md` - Business and data flow diagrams
- `geo-asset-requirements.md` - Detailed system requirements
- `geo-asset-system-manual.md` - System implementation guide
- `geo-asset-user-guide.md` - End-user documentation

## Working with the Codebase

1. Each module is independent and can be tested individually
2. All styles and scripts are inline for portability
3. Mock data is embedded in JavaScript for demonstration
4. No external dependencies or build process required
5. Cross-module navigation is handled via standard HTML links

## Common Development Tasks

### Testing Changes
```bash
# Start a local server and open in browser
python3 -m http.server 8000 && open http://localhost:8000
```

### Creating New Modules
When creating new module files, follow these conventions:
- Use the naming pattern: `[module-number][letter]-[feature-name].html`
- Include inline CSS using the established CSS variables
- Add mock data within `<script>` tags
- Ensure responsive design with mobile breakpoints
- Include navigation back to index.html

### CSS Variable Reference
The project uses a consistent design system with these key variables:
- `--primary`: #1890ff (primary blue)
- `--success`: #52c41a (green)
- `--warning`: #faad14 (yellow)
- `--error`: #f5222d (red)
- `--purple`: #722ed1
- `--cyan`: #13c2c2
- `--background`: #f0f2f5
- `--card-bg`: #ffffff

### Common UI Components
- **Cards**: `.card` class with rounded corners and shadows
- **Buttons**: `.btn-primary`, `.btn-secondary` with consistent styling
- **Status Badges**: `.status-badge` with color variants
- **Data Tables**: `.data-table` with hover states
- **Charts**: Canvas-based implementations in module scripts

## Navigation Architecture

The system uses a hierarchical navigation structure:
- `index.html` serves as the main portal with a comprehensive menu system
- Each module maintains consistent navigation back to the portal
- Module files are numbered according to their workflow stage (01-06)
- Special-purpose tools (AI search, marketplace) exist as standalone implementations

## Data Handling Patterns

Since this is a demonstration project:
- All data is mocked within JavaScript blocks in each HTML file
- No backend API calls or database connections
- Mock data follows consistent structures across modules
- Data generators simulate realistic content for demonstrations

## Responsive Design Breakpoints

The system uses mobile-first responsive design:
- Mobile: < 768px
- Tablet: 768px - 1024px
- Desktop: > 1024px
- Wide screens: > 1400px (max-width containers)

## Event Handling Conventions

- Event listeners use delegation for dynamic content
- Form submissions preventDefault() for demo purposes
- Tab switching maintains state within the page session
- Modal interactions follow accessibility best practices

## Chart Implementation Details

Charts are implemented using native Canvas API:
- Line charts for time-series data (monitoring, analytics)
- Bar charts for categorical comparisons
- Pie/donut charts for distribution visualization
- All charts include mock data generators for realistic displays

## File Naming Conventions

- Core modules: `[module-number][letter]-[function].html` (e.g., `01a-question-collector.html`)
- AI tools: `ai-[function].html` (e.g., `ai-search-optimization-system.html`)
- Marketplace: `marketplace-[feature].html` (e.g., `marketplace-template-library.html`)
- Documentation: `geo-[type].md` (e.g., `geo-product-design.md`)

## Testing Approach

For testing changes in this static HTML project:
```bash
# Quick test with Python's built-in server
python3 -m http.server 8000 && open http://localhost:8000

# Alternative with Node.js
npx http-server -p 8000
```

## Common Customization Points

When extending the system:
1. **Adding new modules**: Copy an existing module file and update navigation links
2. **Modifying color schemes**: Update CSS variables in `:root` selector
3. **Adding mock data**: Update the JavaScript data arrays in `<script>` blocks
4. **Creating new components**: Follow existing patterns for cards, tables, and forms
5. **Implementing new charts**: Use the existing Canvas-based chart functions as templates

## Recent Updates

### Visual Enhancements
- `eureka-geo-dam.html` updated with cosmic starry background effect
- Removed rotating animations on chart hover effects
- Force-directed graph changed to static layout with fixed positions

### Navigation Improvements
- Added iframe-based navigation in `02b-content-marketplace.html`
- Marketplace subpages load within the main marketplace interface
- Created `marketplace-home.html` as the default marketplace landing page

### Chart Visualizations
Some pages may include advanced ECharts visualizations for complex data representation. Most modules use native Canvas API for simpler charts.

## Project Status

All major modules are implemented and functional. The system demonstrates:
- Comprehensive GEO (Generative Engine Optimization) analysis tools
- Multi-channel content management capabilities
- AI-powered optimization features
- Real-time analytics and monitoring
- Collaborative workflow management
- Data-driven decision support