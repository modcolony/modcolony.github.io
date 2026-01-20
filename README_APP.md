# Wonton Management System - Role-Based Menu Access

This implementation provides a complete role-based menu access system for the Wonton business management application.

## Features

### Role-Based Access Control
- **Admin Role**: Full access to all menu items
- **User Role**: Limited access to specific menu items (Home, Product Inflow, Product Outflow)

### Menu Structure

#### Main Menu Items:
1. **Home** (User & Admin) - Orange highlight
2. **Dashboard** (Admin Only) - Blue highlight
3. **Product Inflow** (User & Admin) - Orange highlight
   - Dumpling production
   - Other production
4. **Product Outflow** (User & Admin) - Orange highlight
5. **Inventory** (Admin Only) - Blue highlight
   - Inflow
   - Outflow
   - Net change
6. **Sale** (Admin Only) - Blue highlight
7. **Wage** (Admin Only) - Blue highlight
8. **SETUP** (Admin Only) - Blue highlight

### Color Coding
- **Orange** (#FF7043): User-accessible menus
- **Blue** (#1976D2): Admin-only menus

## How to Use

1. Open `app.html` in your browser
2. Use the **Role Switcher** in the sidebar to toggle between User and Admin roles
3. Observe how the menu changes based on the selected role:
   - As **User**: Only Home, Product Inflow, and Product Outflow are visible
   - As **Admin**: All menu items are visible
4. Click on menu items to navigate to different pages
5. Menu items with submenus will expand/collapse when clicked

## Implementation Details

### Technology Stack
- Pure HTML/CSS/JavaScript (no frameworks required)
- Responsive design
- Clean, modern UI with Inter font family

### Key Components

#### Menu Configuration
The menu structure is defined in the `menuConfig` array with:
- Menu ID and label
- Icon representation
- Role-based access (`roles` array)
- Color class for visual coding
- Optional submenu items

#### State Management
- `currentRole`: Tracks the active user role
- `currentPage`: Tracks the currently displayed page
- `expandedMenus`: Set of expanded menu IDs

#### Core Functions
- `renderMenu()`: Dynamically renders the menu based on current role
- `navigateToPage(pageId)`: Handles page navigation
- `toggleSubmenu(menuId)`: Expands/collapses submenus
- `handleRoleChange()`: Updates the application when role is changed

## Accessing the Application

From the main landing page (`index.html`), click the "Management App" button in the navigation to access the management system.

Direct access: Open `app.html` in your browser.

## Customization

To add new menu items or modify access:

1. Edit the `menuConfig` array in `app.html`
2. Add/modify menu items with appropriate role access
3. Add corresponding content in the `pageContent` object
4. The UI will automatically update based on the configuration

## Security Note

This is a frontend-only implementation for demonstration purposes. In a production environment, role-based access should be enforced on the backend with proper authentication and authorization mechanisms.
