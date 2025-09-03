# YouTube-Dashboard-Updates
📊 Interactive YouTube Analytics Dashboard for creators to explore video performance, watch time, engagement trends, and audience insights. Built with HTML, CSS, and JS, this project helps simplify analytics, visualize key data, and design data-driven content growth strategies.
[index.html](https://github.com/user-attachments/files/22113030/index.html)
<link rel="stylesheet" href="style.css">
<script src="chart.js"></script>
<script src="app.js"></script>


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>MagicMitraVlogs YouTube Analytics Dashboard</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
</head>
<body>
    <!-- Header Section -->
    <header class="dashboard-header">
        <div class="container">
            <div class="header-content">
                <div class="brand-section">
                    <div class="logo-placeholder">
                        <div class="logo-icon">MM</div>
                    </div>
                    <div class="brand-info">
                        <h1 class="brand-title">MagicMitraVlogs YouTube Analytics Dashboard</h1>
                        <p class="brand-tagline">Data-Driven Content Strategy by Nagendra</p>
                        <div class="brand-handles">
                            <span class="channel-handle">@MagicMitraVlogs</span>
                            <span class="instagram-handle">@MagicMitraWorld</span>
                        </div>
                    </div>
                </div>
                <div class="header-stats">
                    <div class="stat-item">
                        <span class="stat-value">12.4M</span>
                        <span class="stat-label">Monthly Searches</span>
                    </div>
                    <div class="stat-item">
                        <span class="stat-value">85.6%</span>
                        <span class="stat-label">Peak Growth</span>
                    </div>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Dashboard -->
    <main class="dashboard-main">
        <div class="container">
            <!-- Navigation Tabs -->
            <nav class="dashboard-nav">
                <button class="nav-tab active" data-section="trending">Trending Topics</button>
                <button class="nav-tab" data-section="engagement">Engagement Metrics</button>
                <button class="nav-tab" data-section="posting">Posting Calendar</button>
                <button class="nav-tab" data-section="gaps">Content Gaps</button>
            </nav>

            <!-- Trending Topics Section -->
            <section id="trending" class="dashboard-section active">
                <div class="section-header">
                    <h2>Trending Topics Analysis</h2>
                    <div class="section-controls">
                        <select class="form-control category-filter">
                            <option value="all">All Categories</option>
                            <option value="Entertainment">Entertainment</option>
                            <option value="Education">Education</option>
                            <option value="Technology">Technology</option>
                            <option value="Lifestyle">Lifestyle</option>
                        </select>
                    </div>
                </div>
                
                <div class="trending-grid">
                    <div class="trending-cards" id="trending-cards">
                        <!-- Trending topic cards will be populated by JavaScript -->
                    </div>
                    
                    <div class="trending-chart">
                        <div class="chart-container" style="position: relative; height: 400px;">
                            <canvas id="trendingChart"></canvas>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Engagement Metrics Section -->
            <section id="engagement" class="dashboard-section">
                <div class="section-header">
                    <h2>Engagement Metrics Analyzer</h2>
                </div>
                
                <div class="metrics-grid">
                    <div class="metric-card">
                        <h3>Watch Time Targets</h3>
                        <div class="metric-items">
                            <div class="metric-item">
                                <span class="metric-label">Shorts</span>
                                <div class="progress-bar">
                                    <div class="progress-fill" style="width: 87%"></div>
                                    <span class="progress-text">85-90%</span>
                                </div>
                            </div>
                            <div class="metric-item">
                                <span class="metric-label">Long Form</span>
                                <div class="progress-bar">
                                    <div class="progress-fill" style="width: 60%"></div>
                                    <span class="progress-text">55-65%</span>
                                </div>
                            </div>
                            <div class="metric-item">
                                <span class="metric-label">Educational</span>
                                <div class="progress-bar">
                                    <div class="progress-fill" style="width: 67%"></div>
                                    <span class="progress-text">60-75%</span>
                                </div>
                            </div>
                        </div>
                    </div>

                    <div class="metric-card">
                        <h3>Engagement Rate Benchmarks</h3>
                        <div class="engagement-chart">
                            <div class="chart-container" style="position: relative; height: 250px;">
                                <canvas id="engagementChart"></canvas>
                            </div>
                        </div>
                    </div>

                    <div class="metric-card">
                        <h3>Performance Indicators</h3>
                        <div class="indicator-grid">
                            <div class="indicator">
                                <div class="indicator-value">5-8%</div>
                                <div class="indicator-label">Likes/Views</div>
                            </div>
                            <div class="indicator">
                                <div class="indicator-value">0.5-2%</div>
                                <div class="indicator-label">Comments/Views</div>
                            </div>
                            <div class="indicator">
                                <div class="indicator-value">0.2-1%</div>
                                <div class="indicator-label">Shares/Views</div>
                            </div>
                            <div class="indicator">
                                <div class="indicator-value">1-3%</div>
                                <div class="indicator-label">Subscribers/Viewers</div>
                            </div>
                        </div>
                    </div>
                </div>
            </section>

            <!-- Posting Calendar Section -->
            <section id="posting" class="dashboard-section">
                <div class="section-header">
                    <h2>Optimal Posting Calendar</h2>
                    <div class="timezone-info">IST (India Standard Time)</div>
                </div>
                
                <div class="calendar-container">
                    <div class="calendar-legend">
                        <div class="legend-item">
                            <div class="legend-color peak"></div>
                            <span>Peak Hours</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color good"></div>
                            <span>Good Hours</span>
                        </div>
                        <div class="legend-item">
                            <div class="legend-color optimal"></div>
                            <span>Optimal Days</span>
                        </div>
                    </div>
                    
                    <div class="weekly-calendar" id="weekly-calendar">
                        <!-- Calendar will be populated by JavaScript -->
                    </div>
                </div>
            </section>

            <!-- Content Gaps Section -->
            <section id="gaps" class="dashboard-section">
                <div class="section-header">
                    <h2>Content Gap Analysis</h2>
                    <p class="section-subtitle">High-opportunity niches with low competition</p>
                </div>
                
                <div class="gaps-grid">
                    <div class="gaps-cards" id="gaps-cards">
                        <!-- Gap analysis cards will be populated by JavaScript -->
                    </div>
                    
                    <div class="gaps-chart">
                        <div class="chart-container" style="position: relative; height: 350px;">
                            <canvas id="gapsChart"></canvas>
                        </div>
                    </div>
                </div>
            </section>
        </div>
    </main>

    <!-- Footer -->
    <footer class="dashboard-footer">
        <div class="container">
            <div class="footer-content">
                <div class="footer-brand">
                    <p>Powered by MagicMitraVlogs Research</p>
                    <div class="footer-links">
                        <a href="https://youtube.com/channel/MagicMitraVogs" target="_blank">YouTube Channel</a>
                        <span class="separator">•</span>
                        <a href="#" target="_blank">@MagicMitraWorld</a>
                    </div>
                </div>
                <div class="footer-actions">
                    <button class="btn btn--secondary" id="exportData">Export Data</button>
                    <button class="btn btn--primary" id="refreshData">Refresh Data</button>
                </div>
            </div>
        </div>
    </footer>

    <script src="app.js"></script>
</body>
</html>

[style.css](https://github.com/user-attachments/files/22113037/style.css)
:root {
  /* Primitive Color Tokens */
  --color-white: rgba(255, 255, 255, 1);
  --color-black: rgba(0, 0, 0, 1);
  --color-cream-50: rgba(252, 252, 249, 1);
  --color-cream-100: rgba(255, 255, 253, 1);
  --color-gray-200: rgba(245, 245, 245, 1);
  --color-gray-300: rgba(167, 169, 169, 1);
  --color-gray-400: rgba(119, 124, 124, 1);
  --color-slate-500: rgba(98, 108, 113, 1);
  --color-brown-600: rgba(94, 82, 64, 1);
  --color-charcoal-700: rgba(31, 33, 33, 1);
  --color-charcoal-800: rgba(38, 40, 40, 1);
  --color-slate-900: rgba(19, 52, 59, 1);
  --color-teal-300: rgba(50, 184, 198, 1);
  --color-teal-400: rgba(45, 166, 178, 1);
  --color-teal-500: rgba(33, 128, 141, 1);
  --color-teal-600: rgba(29, 116, 128, 1);
  --color-teal-700: rgba(26, 104, 115, 1);
  --color-teal-800: rgba(41, 150, 161, 1);
  --color-red-400: rgba(255, 84, 89, 1);
  --color-red-500: rgba(192, 21, 47, 1);
  --color-orange-400: rgba(230, 129, 97, 1);
  --color-orange-500: rgba(168, 75, 47, 1);

  /* RGB versions for opacity control */
  --color-brown-600-rgb: 94, 82, 64;
  --color-teal-500-rgb: 33, 128, 141;
  --color-slate-900-rgb: 19, 52, 59;
  --color-slate-500-rgb: 98, 108, 113;
  --color-red-500-rgb: 192, 21, 47;
  --color-red-400-rgb: 255, 84, 89;
  --color-orange-500-rgb: 168, 75, 47;
  --color-orange-400-rgb: 230, 129, 97;

  /* Background color tokens (Light Mode) */
  --color-bg-1: rgba(59, 130, 246, 0.08); /* Light blue */
  --color-bg-2: rgba(245, 158, 11, 0.08); /* Light yellow */
  --color-bg-3: rgba(34, 197, 94, 0.08); /* Light green */
  --color-bg-4: rgba(239, 68, 68, 0.08); /* Light red */
  --color-bg-5: rgba(147, 51, 234, 0.08); /* Light purple */
  --color-bg-6: rgba(249, 115, 22, 0.08); /* Light orange */
  --color-bg-7: rgba(236, 72, 153, 0.08); /* Light pink */
  --color-bg-8: rgba(6, 182, 212, 0.08); /* Light cyan */

  /* Semantic Color Tokens (Light Mode) */
  --color-background: var(--color-cream-50);
  --color-surface: var(--color-cream-100);
  --color-text: var(--color-slate-900);
  --color-text-secondary: var(--color-slate-500);
  --color-primary: var(--color-teal-500);
  --color-primary-hover: var(--color-teal-600);
  --color-primary-active: var(--color-teal-700);
  --color-secondary: rgba(var(--color-brown-600-rgb), 0.12);
  --color-secondary-hover: rgba(var(--color-brown-600-rgb), 0.2);
  --color-secondary-active: rgba(var(--color-brown-600-rgb), 0.25);
  --color-border: rgba(var(--color-brown-600-rgb), 0.2);
  --color-btn-primary-text: var(--color-cream-50);
  --color-card-border: rgba(var(--color-brown-600-rgb), 0.12);
  --color-card-border-inner: rgba(var(--color-brown-600-rgb), 0.12);
  --color-error: var(--color-red-500);
  --color-success: var(--color-teal-500);
  --color-warning: var(--color-orange-500);
  --color-info: var(--color-slate-500);
  --color-focus-ring: rgba(var(--color-teal-500-rgb), 0.4);
  --color-select-caret: rgba(var(--color-slate-900-rgb), 0.8);

  /* Common style patterns */
  --focus-ring: 0 0 0 3px var(--color-focus-ring);
  --focus-outline: 2px solid var(--color-primary);
  --status-bg-opacity: 0.15;
  --status-border-opacity: 0.25;
  --select-caret-light: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' viewBox='0 0 24 24' fill='none' stroke='%23134252' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");
  --select-caret-dark: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' viewBox='0 0 24 24' fill='none' stroke='%23f5f5f5' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");

  /* RGB versions for opacity control */
  --color-success-rgb: 33, 128, 141;
  --color-error-rgb: 192, 21, 47;
  --color-warning-rgb: 168, 75, 47;
  --color-info-rgb: 98, 108, 113;

  /* Typography */
  --font-family-base: "FKGroteskNeue", "Geist", "Inter", -apple-system,
    BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
  --font-family-mono: "Berkeley Mono", ui-monospace, SFMono-Regular, Menlo,
    Monaco, Consolas, monospace;
  --font-size-xs: 11px;
  --font-size-sm: 12px;
  --font-size-base: 14px;
  --font-size-md: 14px;
  --font-size-lg: 16px;
  --font-size-xl: 18px;
  --font-size-2xl: 20px;
  --font-size-3xl: 24px;
  --font-size-4xl: 30px;
  --font-weight-normal: 400;
  --font-weight-medium: 500;
  --font-weight-semibold: 550;
  --font-weight-bold: 600;
  --line-height-tight: 1.2;
  --line-height-normal: 1.5;
  --letter-spacing-tight: -0.01em;

  /* Spacing */
  --space-0: 0;
  --space-1: 1px;
  --space-2: 2px;
  --space-4: 4px;
  --space-6: 6px;
  --space-8: 8px;
  --space-10: 10px;
  --space-12: 12px;
  --space-16: 16px;
  --space-20: 20px;
  --space-24: 24px;
  --space-32: 32px;

  /* Border Radius */
  --radius-sm: 6px;
  --radius-base: 8px;
  --radius-md: 10px;
  --radius-lg: 12px;
  --radius-full: 9999px;

  /* Shadows */
  --shadow-xs: 0 1px 2px rgba(0, 0, 0, 0.02);
  --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.04), 0 1px 2px rgba(0, 0, 0, 0.02);
  --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.04),
    0 2px 4px -1px rgba(0, 0, 0, 0.02);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.04),
    0 4px 6px -2px rgba(0, 0, 0, 0.02);
  --shadow-inset-sm: inset 0 1px 0 rgba(255, 255, 255, 0.15),
    inset 0 -1px 0 rgba(0, 0, 0, 0.03);

  /* Animation */
  --duration-fast: 150ms;
  --duration-normal: 250ms;
  --ease-standard: cubic-bezier(0.16, 1, 0.3, 1);

  /* Layout */
  --container-sm: 640px;
  --container-md: 768px;
  --container-lg: 1024px;
  --container-xl: 1280px;
}

/* Dark mode colors */
@media (prefers-color-scheme: dark) {
  :root {
    /* RGB versions for opacity control (Dark Mode) */
    --color-gray-400-rgb: 119, 124, 124;
    --color-teal-300-rgb: 50, 184, 198;
    --color-gray-300-rgb: 167, 169, 169;
    --color-gray-200-rgb: 245, 245, 245;

    /* Background color tokens (Dark Mode) */
    --color-bg-1: rgba(29, 78, 216, 0.15); /* Dark blue */
    --color-bg-2: rgba(180, 83, 9, 0.15); /* Dark yellow */
    --color-bg-3: rgba(21, 128, 61, 0.15); /* Dark green */
    --color-bg-4: rgba(185, 28, 28, 0.15); /* Dark red */
    --color-bg-5: rgba(107, 33, 168, 0.15); /* Dark purple */
    --color-bg-6: rgba(194, 65, 12, 0.15); /* Dark orange */
    --color-bg-7: rgba(190, 24, 93, 0.15); /* Dark pink */
    --color-bg-8: rgba(8, 145, 178, 0.15); /* Dark cyan */
    
    /* Semantic Color Tokens (Dark Mode) */
    --color-background: var(--color-charcoal-700);
    --color-surface: var(--color-charcoal-800);
    --color-text: var(--color-gray-200);
    --color-text-secondary: rgba(var(--color-gray-300-rgb), 0.7);
    --color-primary: var(--color-teal-300);
    --color-primary-hover: var(--color-teal-400);
    --color-primary-active: var(--color-teal-800);
    --color-secondary: rgba(var(--color-gray-400-rgb), 0.15);
    --color-secondary-hover: rgba(var(--color-gray-400-rgb), 0.25);
    --color-secondary-active: rgba(var(--color-gray-400-rgb), 0.3);
    --color-border: rgba(var(--color-gray-400-rgb), 0.3);
    --color-error: var(--color-red-400);
    --color-success: var(--color-teal-300);
    --color-warning: var(--color-orange-400);
    --color-info: var(--color-gray-300);
    --color-focus-ring: rgba(var(--color-teal-300-rgb), 0.4);
    --color-btn-primary-text: var(--color-slate-900);
    --color-card-border: rgba(var(--color-gray-400-rgb), 0.2);
    --color-card-border-inner: rgba(var(--color-gray-400-rgb), 0.15);
    --shadow-inset-sm: inset 0 1px 0 rgba(255, 255, 255, 0.1),
      inset 0 -1px 0 rgba(0, 0, 0, 0.15);
    --button-border-secondary: rgba(var(--color-gray-400-rgb), 0.2);
    --color-border-secondary: rgba(var(--color-gray-400-rgb), 0.2);
    --color-select-caret: rgba(var(--color-gray-200-rgb), 0.8);

    /* Common style patterns - updated for dark mode */
    --focus-ring: 0 0 0 3px var(--color-focus-ring);
    --focus-outline: 2px solid var(--color-primary);
    --status-bg-opacity: 0.15;
    --status-border-opacity: 0.25;
    --select-caret-light: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' viewBox='0 0 24 24' fill='none' stroke='%23134252' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");
    --select-caret-dark: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' viewBox='0 0 24 24' fill='none' stroke='%23f5f5f5' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");

    /* RGB versions for dark mode */
    --color-success-rgb: var(--color-teal-300-rgb);
    --color-error-rgb: var(--color-red-400-rgb);
    --color-warning-rgb: var(--color-orange-400-rgb);
    --color-info-rgb: var(--color-gray-300-rgb);
  }
}

/* Data attribute for manual theme switching */
[data-color-scheme="dark"] {
  /* RGB versions for opacity control (dark mode) */
  --color-gray-400-rgb: 119, 124, 124;
  --color-teal-300-rgb: 50, 184, 198;
  --color-gray-300-rgb: 167, 169, 169;
  --color-gray-200-rgb: 245, 245, 245;

  /* Colorful background palette - Dark Mode */
  --color-bg-1: rgba(29, 78, 216, 0.15); /* Dark blue */
  --color-bg-2: rgba(180, 83, 9, 0.15); /* Dark yellow */
  --color-bg-3: rgba(21, 128, 61, 0.15); /* Dark green */
  --color-bg-4: rgba(185, 28, 28, 0.15); /* Dark red */
  --color-bg-5: rgba(107, 33, 168, 0.15); /* Dark purple */
  --color-bg-6: rgba(194, 65, 12, 0.15); /* Dark orange */
  --color-bg-7: rgba(190, 24, 93, 0.15); /* Dark pink */
  --color-bg-8: rgba(8, 145, 178, 0.15); /* Dark cyan */
  
  /* Semantic Color Tokens (Dark Mode) */
  --color-background: var(--color-charcoal-700);
  --color-surface: var(--color-charcoal-800);
  --color-text: var(--color-gray-200);
  --color-text-secondary: rgba(var(--color-gray-300-rgb), 0.7);
  --color-primary: var(--color-teal-300);
  --color-primary-hover: var(--color-teal-400);
  --color-primary-active: var(--color-teal-800);
  --color-secondary: rgba(var(--color-gray-400-rgb), 0.15);
  --color-secondary-hover: rgba(var(--color-gray-400-rgb), 0.25);
  --color-secondary-active: rgba(var(--color-gray-400-rgb), 0.3);
  --color-border: rgba(var(--color-gray-400-rgb), 0.3);
  --color-error: var(--color-red-400);
  --color-success: var(--color-teal-300);
  --color-warning: var(--color-orange-400);
  --color-info: var(--color-gray-300);
  --color-focus-ring: rgba(var(--color-teal-300-rgb), 0.4);
  --color-btn-primary-text: var(--color-slate-900);
  --color-card-border: rgba(var(--color-gray-400-rgb), 0.15);
  --color-card-border-inner: rgba(var(--color-gray-400-rgb), 0.15);
  --shadow-inset-sm: inset 0 1px 0 rgba(255, 255, 255, 0.1),
    inset 0 -1px 0 rgba(0, 0, 0, 0.15);
  --color-border-secondary: rgba(var(--color-gray-400-rgb), 0.2);
  --color-select-caret: rgba(var(--color-gray-200-rgb), 0.8);

  /* Common style patterns - updated for dark mode */
  --focus-ring: 0 0 0 3px var(--color-focus-ring);
  --focus-outline: 2px solid var(--color-primary);
  --status-bg-opacity: 0.15;
  --status-border-opacity: 0.25;
  --select-caret-light: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' viewBox='0 0 24 24' fill='none' stroke='%23134252' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");
  --select-caret-dark: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='16' height='16' viewBox='0 0 24 24' fill='none' stroke='%23f5f5f5' stroke-width='2' stroke-linecap='round' stroke-linejoin='round'%3E%3Cpolyline points='6 9 12 15 18 9'%3E%3C/polyline%3E%3C/svg%3E");

  /* RGB versions for dark mode */
  --color-success-rgb: var(--color-teal-300-rgb);
  --color-error-rgb: var(--color-red-400-rgb);
  --color-warning-rgb: var(--color-orange-400-rgb);
  --color-info-rgb: var(--color-gray-300-rgb);
}

[data-color-scheme="light"] {
  /* RGB versions for opacity control (light mode) */
  --color-brown-600-rgb: 94, 82, 64;
  --color-teal-500-rgb: 33, 128, 141;
  --color-slate-900-rgb: 19, 52, 59;
  
  /* Semantic Color Tokens (Light Mode) */
  --color-background: var(--color-cream-50);
  --color-surface: var(--color-cream-100);
  --color-text: var(--color-slate-900);
  --color-text-secondary: var(--color-slate-500);
  --color-primary: var(--color-teal-500);
  --color-primary-hover: var(--color-teal-600);
  --color-primary-active: var(--color-teal-700);
  --color-secondary: rgba(var(--color-brown-600-rgb), 0.12);
  --color-secondary-hover: rgba(var(--color-brown-600-rgb), 0.2);
  --color-secondary-active: rgba(var(--color-brown-600-rgb), 0.25);
  --color-border: rgba(var(--color-brown-600-rgb), 0.2);
  --color-btn-primary-text: var(--color-cream-50);
  --color-card-border: rgba(var(--color-brown-600-rgb), 0.12);
  --color-card-border-inner: rgba(var(--color-brown-600-rgb), 0.12);
  --color-error: var(--color-red-500);
  --color-success: var(--color-teal-500);
  --color-warning: var(--color-orange-500);
  --color-info: var(--color-slate-500);
  --color-focus-ring: rgba(var(--color-teal-500-rgb), 0.4);

  /* RGB versions for light mode */
  --color-success-rgb: var(--color-teal-500-rgb);
  --color-error-rgb: var(--color-red-500-rgb);
  --color-warning-rgb: var(--color-orange-500-rgb);
  --color-info-rgb: var(--color-slate-500-rgb);
}

/* Base styles */
html {
  font-size: var(--font-size-base);
  font-family: var(--font-family-base);
  line-height: var(--line-height-normal);
  color: var(--color-text);
  background-color: var(--color-background);
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

body {
  margin: 0;
  padding: 0;
}

*,
*::before,
*::after {
  box-sizing: inherit;
}

/* Typography */
h1,
h2,
h3,
h4,
h5,
h6 {
  margin: 0;
  font-weight: var(--font-weight-semibold);
  line-height: var(--line-height-tight);
  color: var(--color-text);
  letter-spacing: var(--letter-spacing-tight);
}

h1 {
  font-size: var(--font-size-4xl);
}
h2 {
  font-size: var(--font-size-3xl);
}
h3 {
  font-size: var(--font-size-2xl);
}
h4 {
  font-size: var(--font-size-xl);
}
h5 {
  font-size: var(--font-size-lg);
}
h6 {
  font-size: var(--font-size-md);
}

p {
  margin: 0 0 var(--space-16) 0;
}

a {
  color: var(--color-primary);
  text-decoration: none;
  transition: color var(--duration-fast) var(--ease-standard);
}

a:hover {
  color: var(--color-primary-hover);
}

code,
pre {
  font-family: var(--font-family-mono);
  font-size: calc(var(--font-size-base) * 0.95);
  background-color: var(--color-secondary);
  border-radius: var(--radius-sm);
}

code {
  padding: var(--space-1) var(--space-4);
}

pre {
  padding: var(--space-16);
  margin: var(--space-16) 0;
  overflow: auto;
  border: 1px solid var(--color-border);
}

pre code {
  background: none;
  padding: 0;
}

/* Buttons */
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: var(--space-8) var(--space-16);
  border-radius: var(--radius-base);
  font-size: var(--font-size-base);
  font-weight: 500;
  line-height: 1.5;
  cursor: pointer;
  transition: all var(--duration-normal) var(--ease-standard);
  border: none;
  text-decoration: none;
  position: relative;
}

.btn:focus-visible {
  outline: none;
  box-shadow: var(--focus-ring);
}

.btn--primary {
  background: var(--color-primary);
  color: var(--color-btn-primary-text);
}

.btn--primary:hover {
  background: var(--color-primary-hover);
}

.btn--primary:active {
  background: var(--color-primary-active);
}

.btn--secondary {
  background: var(--color-secondary);
  color: var(--color-text);
}

.btn--secondary:hover {
  background: var(--color-secondary-hover);
}

.btn--secondary:active {
  background: var(--color-secondary-active);
}

.btn--outline {
  background: transparent;
  border: 1px solid var(--color-border);
  color: var(--color-text);
}

.btn--outline:hover {
  background: var(--color-secondary);
}

.btn--sm {
  padding: var(--space-4) var(--space-12);
  font-size: var(--font-size-sm);
  border-radius: var(--radius-sm);
}

.btn--lg {
  padding: var(--space-10) var(--space-20);
  font-size: var(--font-size-lg);
  border-radius: var(--radius-md);
}

.btn--full-width {
  width: 100%;
}

.btn:disabled {
  opacity: 0.5;
  cursor: not-allowed;
}

/* Form elements */
.form-control {
  display: block;
  width: 100%;
  padding: var(--space-8) var(--space-12);
  font-size: var(--font-size-md);
  line-height: 1.5;
  color: var(--color-text);
  background-color: var(--color-surface);
  border: 1px solid var(--color-border);
  border-radius: var(--radius-base);
  transition: border-color var(--duration-fast) var(--ease-standard),
    box-shadow var(--duration-fast) var(--ease-standard);
}

textarea.form-control {
  font-family: var(--font-family-base);
  font-size: var(--font-size-base);
}

select.form-control {
  padding: var(--space-8) var(--space-12);
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  background-image: var(--select-caret-light);
  background-repeat: no-repeat;
  background-position: right var(--space-12) center;
  background-size: 16px;
  padding-right: var(--space-32);
}

/* Add a dark mode specific caret */
@media (prefers-color-scheme: dark) {
  select.form-control {
    background-image: var(--select-caret-dark);
  }
}

/* Also handle data-color-scheme */
[data-color-scheme="dark"] select.form-control {
  background-image: var(--select-caret-dark);
}

[data-color-scheme="light"] select.form-control {
  background-image: var(--select-caret-light);
}

.form-control:focus {
  border-color: var(--color-primary);
  outline: var(--focus-outline);
}

.form-label {
  display: block;
  margin-bottom: var(--space-8);
  font-weight: var(--font-weight-medium);
  font-size: var(--font-size-sm);
}

.form-group {
  margin-bottom: var(--space-16);
}

/* Card component */
.card {
  background-color: var(--color-surface);
  border-radius: var(--radius-lg);
  border: 1px solid var(--color-card-border);
  box-shadow: var(--shadow-sm);
  overflow: hidden;
  transition: box-shadow var(--duration-normal) var(--ease-standard);
}

.card:hover {
  box-shadow: var(--shadow-md);
}

.card__body {
  padding: var(--space-16);
}

.card__header,
.card__footer {
  padding: var(--space-16);
  border-bottom: 1px solid var(--color-card-border-inner);
}

/* Status indicators - simplified with CSS variables */
.status {
  display: inline-flex;
  align-items: center;
  padding: var(--space-6) var(--space-12);
  border-radius: var(--radius-full);
  font-weight: var(--font-weight-medium);
  font-size: var(--font-size-sm);
}

.status--success {
  background-color: rgba(
    var(--color-success-rgb, 33, 128, 141),
    var(--status-bg-opacity)
  );
  color: var(--color-success);
  border: 1px solid
    rgba(var(--color-success-rgb, 33, 128, 141), var(--status-border-opacity));
}

.status--error {
  background-color: rgba(
    var(--color-error-rgb, 192, 21, 47),
    var(--status-bg-opacity)
  );
  color: var(--color-error);
  border: 1px solid
    rgba(var(--color-error-rgb, 192, 21, 47), var(--status-border-opacity));
}

.status--warning {
  background-color: rgba(
    var(--color-warning-rgb, 168, 75, 47),
    var(--status-bg-opacity)
  );
  color: var(--color-warning);
  border: 1px solid
    rgba(var(--color-warning-rgb, 168, 75, 47), var(--status-border-opacity));
}

.status--info {
  background-color: rgba(
    var(--color-info-rgb, 98, 108, 113),
    var(--status-bg-opacity)
  );
  color: var(--color-info);
  border: 1px solid
    rgba(var(--color-info-rgb, 98, 108, 113), var(--status-border-opacity));
}

/* Container layout */
.container {
  width: 100%;
  margin-right: auto;
  margin-left: auto;
  padding-right: var(--space-16);
  padding-left: var(--space-16);
}

@media (min-width: 640px) {
  .container {
    max-width: var(--container-sm);
  }
}
@media (min-width: 768px) {
  .container {
    max-width: var(--container-md);
  }
}
@media (min-width: 1024px) {
  .container {
    max-width: var(--container-lg);
  }
}
@media (min-width: 1280px) {
  .container {
    max-width: var(--container-xl);
  }
}

/* Utility classes */
.flex {
  display: flex;
}
.flex-col {
  flex-direction: column;
}
.items-center {
  align-items: center;
}
.justify-center {
  justify-content: center;
}
.justify-between {
  justify-content: space-between;
}
.gap-4 {
  gap: var(--space-4);
}
.gap-8 {
  gap: var(--space-8);
}
.gap-16 {
  gap: var(--space-16);
}

.m-0 {
  margin: 0;
}
.mt-8 {
  margin-top: var(--space-8);
}
.mb-8 {
  margin-bottom: var(--space-8);
}
.mx-8 {
  margin-left: var(--space-8);
  margin-right: var(--space-8);
}
.my-8 {
  margin-top: var(--space-8);
  margin-bottom: var(--space-8);
}

.p-0 {
  padding: 0;
}
.py-8 {
  padding-top: var(--space-8);
  padding-bottom: var(--space-8);
}
.px-8 {
  padding-left: var(--space-8);
  padding-right: var(--space-8);
}
.py-16 {
  padding-top: var(--space-16);
  padding-bottom: var(--space-16);
}
.px-16 {
  padding-left: var(--space-16);
  padding-right: var(--space-16);
}

.block {
  display: block;
}
.hidden {
  display: none;
}

/* Accessibility */
.sr-only {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}

:focus-visible {
  outline: var(--focus-outline);
  outline-offset: 2px;
}

/* Dark mode specifics */
[data-color-scheme="dark"] .btn--outline {
  border: 1px solid var(--color-border-secondary);
}

@font-face {
  font-family: 'FKGroteskNeue';
  src: url('https://r2cdn.perplexity.ai/fonts/FKGroteskNeue.woff2')
    format('woff2');
}

/* END PERPLEXITY DESIGN SYSTEM */
/* Custom MagicMitra Dashboard Styles */
:root {
  /* MagicMitra Brand Colors */
  --magic-primary: #6366f1;
  --magic-secondary: #8b5cf6;
  --magic-accent: #f59e0b;
  --magic-gradient: linear-gradient(135deg, #6366f1 0%, #8b5cf6 100%);
  --magic-gradient-hover: linear-gradient(135deg, #5855eb 0%, #7c3aed 100%);
  --magic-dark-bg: #0f172a;
  --magic-dark-surface: #1e293b;
}

body {
  background: var(--magic-gradient);
  min-height: 100vh;
  font-family: var(--font-family-base);
}

/* Header Styles */
.dashboard-header {
  background: rgba(15, 23, 42, 0.95);
  backdrop-filter: blur(10px);
  border-bottom: 2px solid var(--magic-accent);
  padding: var(--space-24) 0;
  position: sticky;
  top: 0;
  z-index: 100;
}

.header-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: var(--space-24);
}

.brand-section {
  display: flex;
  align-items: center;
  gap: var(--space-20);
}

.logo-placeholder {
  width: 80px;
  height: 80px;
  background: var(--magic-gradient);
  border-radius: var(--radius-lg);
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 8px 32px rgba(99, 102, 241, 0.3);
}

.logo-icon {
  font-size: var(--font-size-3xl);
  font-weight: var(--font-weight-bold);
  color: white;
}

.brand-info h1 {
  color: white;
  font-size: var(--font-size-3xl);
  margin-bottom: var(--space-8);
  background: linear-gradient(45deg, #ffffff, var(--magic-accent));
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.brand-tagline {
  color: rgba(255, 255, 255, 0.8);
  font-size: var(--font-size-lg);
  margin-bottom: var(--space-12);
}

.brand-handles {
  display: flex;
  gap: var(--space-16);
  flex-wrap: wrap;
}

.channel-handle, .instagram-handle {
  background: rgba(255, 255, 255, 0.1);
  padding: var(--space-6) var(--space-12);
  border-radius: var(--radius-full);
  color: var(--magic-accent);
  font-weight: var(--font-weight-medium);
  font-size: var(--font-size-sm);
}

.header-stats {
  display: flex;
  gap: var(--space-32);
}

.stat-item {
  text-align: center;
}

.stat-value {
  display: block;
  font-size: var(--font-size-2xl);
  font-weight: var(--font-weight-bold);
  color: var(--magic-accent);
  line-height: 1.2;
}

.stat-label {
  font-size: var(--font-size-sm);
  color: rgba(255, 255, 255, 0.7);
}

/* Main Dashboard */
.dashboard-main {
  background: rgba(255, 255, 255, 0.95);
  margin: var(--space-32) var(--space-16);
  border-radius: var(--radius-lg);
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.1);
  overflow: hidden;
}

/* Navigation */
.dashboard-nav {
  display: flex;
  background: var(--color-surface);
  border-bottom: 1px solid var(--color-border);
  overflow-x: auto;
}

.nav-tab {
  flex: 1;
  padding: var(--space-16) var(--space-24);
  border: none;
  background: transparent;
  color: var(--color-text-secondary);
  font-weight: var(--font-weight-medium);
  cursor: pointer;
  transition: all var(--duration-normal) var(--ease-standard);
  position: relative;
  white-space: nowrap;
}

.nav-tab:hover {
  background: var(--color-secondary);
  color: var(--color-text);
}

.nav-tab.active {
  color: var(--magic-primary);
  background: rgba(99, 102, 241, 0.08);
}

.nav-tab.active::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 3px;
  background: var(--magic-gradient);
}

/* Dashboard Sections */
.dashboard-section {
  display: none;
  padding: var(--space-32);
}

.dashboard-section.active {
  display: block;
}

.section-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: var(--space-32);
  flex-wrap: wrap;
  gap: var(--space-16);
}

.section-header h2 {
  color: var(--magic-dark-bg);
  font-size: var(--font-size-3xl);
}

.section-subtitle {
  color: var(--color-text-secondary);
  margin-top: var(--space-8);
}

.section-controls {
  display: flex;
  gap: var(--space-16);
  align-items: center;
}

/* Trending Topics */
.trending-grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: var(--space-32);
}

.trending-cards {
  display: grid;
  gap: var(--space-20);
}

.trending-card {
  background: var(--color-surface);
  border: 1px solid var(--color-card-border);
  border-radius: var(--radius-lg);
  padding: var(--space-24);
  transition: all var(--duration-normal) var(--ease-standard);
  position: relative;
  overflow: hidden;
}

.trending-card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 4px;
  background: var(--magic-gradient);
}

.trending-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 12px 40px rgba(99, 102, 241, 0.15);
}

.trending-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  margin-bottom: var(--space-16);
}

.trending-title {
  font-size: var(--font-size-xl);
  font-weight: var(--font-weight-semibold);
  color: var(--color-text);
}

.growth-badge {
  background: var(--magic-gradient);
  color: white;
  padding: var(--space-4) var(--space-12);
  border-radius: var(--radius-full);
  font-size: var(--font-size-sm);
  font-weight: var(--font-weight-medium);
}

.trending-stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  gap: var(--space-16);
  margin-bottom: var(--space-16);
}

.stat {
  text-align: center;
  padding: var(--space-12);
  background: var(--color-bg-1);
  border-radius: var(--radius-base);
}

.stat-number {
  display: block;
  font-size: var(--font-size-lg);
  font-weight: var(--font-weight-bold);
  color: var(--magic-primary);
}

.stat-text {
  font-size: var(--font-size-sm);
  color: var(--color-text-secondary);
}

.category-tag {
  display: inline-block;
  background: rgba(99, 102, 241, 0.1);
  color: var(--magic-primary);
  padding: var(--space-4) var(--space-8);
  border-radius: var(--radius-sm);
  font-size: var(--font-size-xs);
  font-weight: var(--font-weight-medium);
}

/* Engagement Metrics */
.metrics-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: var(--space-24);
}

.metric-card {
  background: var(--color-surface);
  border: 1px solid var(--color-card-border);
  border-radius: var(--radius-lg);
  padding: var(--space-24);
}

.metric-card h3 {
  margin-bottom: var(--space-20);
  color: var(--color-text);
  font-size: var(--font-size-xl);
}

.metric-items {
  display: flex;
  flex-direction: column;
  gap: var(--space-16);
}

.metric-item {
  display: flex;
  align-items: center;
  gap: var(--space-16);
}

.metric-label {
  min-width: 100px;
  font-size: var(--font-size-sm);
  color: var(--color-text-secondary);
}

.progress-bar {
  flex: 1;
  height: 24px;
  background: var(--color-bg-2);
  border-radius: var(--radius-full);
  position: relative;
  overflow: hidden;
}

.progress-fill {
  height: 100%;
  background: var(--magic-gradient);
  border-radius: var(--radius-full);
  transition: width var(--duration-normal) var(--ease-standard);
}

.progress-text {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-size: var(--font-size-xs);
  font-weight: var(--font-weight-medium);
  color: var(--color-text);
}

.indicator-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--space-16);
}

.indicator {
  text-align: center;
  padding: var(--space-16);
  background: var(--color-bg-3);
  border-radius: var(--radius-base);
}

.indicator-value {
  font-size: var(--font-size-lg);
  font-weight: var(--font-weight-bold);
  color: var(--magic-primary);
  margin-bottom: var(--space-4);
}

.indicator-label {
  font-size: var(--font-size-sm);
  color: var(--color-text-secondary);
}

/* Posting Calendar */
.timezone-info {
  background: var(--color-bg-4);
  color: var(--color-text);
  padding: var(--space-8) var(--space-16);
  border-radius: var(--radius-base);
  font-size: var(--font-size-sm);
  font-weight: var(--font-weight-medium);
}

.calendar-legend {
  display: flex;
  gap: var(--space-24);
  margin-bottom: var(--space-24);
  flex-wrap: wrap;
}

.legend-item {
  display: flex;
  align-items: center;
  gap: var(--space-8);
}

.legend-color {
  width: 16px;
  height: 16px;
  border-radius: var(--radius-sm);
}

.legend-color.peak {
  background: var(--magic-accent);
}

.legend-color.good {
  background: var(--magic-primary);
}

.legend-color.optimal {
  background: var(--magic-gradient);
}

.weekly-calendar {
  display: grid;
  grid-template-columns: repeat(7, 1fr);
  gap: var(--space-16);
}

.day-card {
  background: var(--color-surface);
  border: 1px solid var(--color-card-border);
  border-radius: var(--radius-base);
  padding: var(--space-16);
  text-align: center;
}

.day-card.optimal {
  border: 2px solid var(--magic-accent);
  background: rgba(245, 158, 11, 0.05);
}

.day-name {
  font-weight: var(--font-weight-semibold);
  color: var(--color-text);
  margin-bottom: var(--space-12);
}

.time-slots {
  display: flex;
  flex-direction: column;
  gap: var(--space-4);
}

.time-slot {
  padding: var(--space-4) var(--space-6);
  border-radius: var(--radius-sm);
  font-size: var(--font-size-xs);
  cursor: pointer;
  transition: all var(--duration-fast) var(--ease-standard);
}

.time-slot.peak {
  background: var(--magic-accent);
  color: white;
}

.time-slot.good {
  background: rgba(99, 102, 241, 0.6);
  color: white;
}

.time-slot:hover {
  transform: scale(1.05);
}

/* Content Gaps */
.gaps-grid {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: var(--space-32);
}

.gaps-cards {
  display: grid;
  gap: var(--space-20);
}

.gap-card {
  background: var(--color-surface);
  border: 1px solid var(--color-card-border);
  border-radius: var(--radius-lg);
  padding: var(--space-24);
  transition: all var(--duration-normal) var(--ease-standard);
}

.gap-card:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 32px rgba(99, 102, 241, 0.1);
}

.gap-header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: var(--space-16);
}

.gap-title {
  font-size: var(--font-size-xl);
  font-weight: var(--font-weight-semibold);
  color: var(--color-text);
}

.opportunity-badge {
  padding: var(--space-4) var(--space-12);
  border-radius: var(--radius-full);
  font-size: var(--font-size-sm);
  font-weight: var(--font-weight-medium);
}

.opportunity-badge.very-high {
  background: rgba(16, 185, 129, 0.1);
  color: #059669;
}

.opportunity-badge.high {
  background: rgba(99, 102, 241, 0.1);
  color: var(--magic-primary);
}

.opportunity-badge.excellent {
  background: rgba(245, 158, 11, 0.1);
  color: var(--magic-accent);
}

.gap-metrics {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: var(--space-12);
  margin-bottom: var(--space-16);
}

.gap-metric {
  text-align: center;
  padding: var(--space-12);
  background: var(--color-bg-5);
  border-radius: var(--radius-base);
}

.gap-metric-value {
  font-weight: var(--font-weight-bold);
  color: var(--magic-primary);
  margin-bottom: var(--space-2);
}

.gap-metric-label {
  font-size: var(--font-size-xs);
  color: var(--color-text-secondary);
}

/* Footer */
.dashboard-footer {
  background: rgba(15, 23, 42, 0.95);
  backdrop-filter: blur(10px);
  border-top: 2px solid var(--magic-accent);
  padding: var(--space-24) 0;
  margin-top: var(--space-32);
}

.footer-content {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: var(--space-16);
}

.footer-brand p {
  color: white;
  margin-bottom: var(--space-8);
  font-weight: var(--font-weight-medium);
}

.footer-links {
  display: flex;
  gap: var(--space-16);
  align-items: center;
}

.footer-links a {
  color: var(--magic-accent);
  text-decoration: none;
  font-size: var(--font-size-sm);
  transition: color var(--duration-fast) var(--ease-standard);
}

.footer-links a:hover {
  color: white;
}

.separator {
  color: rgba(255, 255, 255, 0.5);
}

.footer-actions {
  display: flex;
  gap: var(--space-12);
}

/* Responsive Design */
@media (max-width: 768px) {
  .trending-grid,
  .gaps-grid {
    grid-template-columns: 1fr;
  }
  
  .metrics-grid {
    grid-template-columns: 1fr;
  }
  
  .weekly-calendar {
    grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
  }
  
  .header-content {
    text-align: center;
  }
  
  .brand-section {
    flex-direction: column;
    text-align: center;
  }
  
  .dashboard-main {
    margin: var(--space-16) var(--space-8);
  }
  
  .dashboard-section {
    padding: var(--space-20);
  }
}

/* Loading Animation */
.loading {
  display: inline-block;
  width: 20px;
  height: 20px;
  border: 3px solid rgba(255, 255, 255, 0.3);
  border-radius: 50%;
  border-top-color: var(--magic-accent);
  animation: spin 1s ease-in-out infinite;
}

@keyframes spin {
  to { transform: rotate(360deg); }
}

/* Chart Containers */
.chart-container {
  background: var(--color-surface);
  border-radius: var(--radius-base);
  padding: var(--space-16);
}

/* Custom scrollbars */
::-webkit-scrollbar {
  width: 8px;
  height: 8px;
}

::-webkit-scrollbar-track {
  background: var(--color-bg-1);
  border-radius: var(--radius-sm);
}

::-webkit-scrollbar-thumb {
  background: var(--magic-gradient);
  border-radius: var(--radius-sm);
}

::-webkit-scrollbar-thumb:hover {
  background: var(--magic-gradient-hover);
}

[app.js](https://github.com/user-attachments/files/22113042/app.js)
// MagicMitraVlogs Dashboard JavaScript
class MagicMitraDashboard {
    constructor() {
        this.data = {
            channelBranding: {
                name: "MagicMitraVlogs",
                tagline: "Data-Driven Content Strategy by Nagendra",
                handle: "@MagicMitraVlogs",
                instagram: "@MagicMitraWorld",
                youtube: "https://youtube.com/channel/MagicMitraVogs",
                colors: {
                    primary: "#6366f1",
                    secondary: "#8b5cf6", 
                    accent: "#f59e0b",
                    background: "#0f172a",
                    surface: "#1e293b"
                }
            },
            trendingTopics: [
                {
                    topic: "Barbie/Transformation Videos",
                    growth: "85.6%",
                    monthlySearches: "12.4M",
                    competition: "60%",
                    category: "Entertainment",
                    opportunity: "Very High",
                    description: "Character transformations and Barbie-themed content dominating",
                    avgViews: "500K-2M",
                    engagement: "12.8%"
                },
                {
                    topic: "Dance Challenges",
                    growth: "62.69%",
                    monthlySearches: "8.7M", 
                    competition: "55%",
                    category: "Entertainment",
                    opportunity: "High",
                    description: "Viral dance trends and choreography tutorials",
                    avgViews: "300K-1.5M",
                    engagement: "15.2%"
                },
                {
                    topic: "Food Challenges",
                    growth: "45.2%",
                    monthlySearches: "3.2M",
                    competition: "48%",
                    category: "Lifestyle",
                    opportunity: "Good",
                    description: "Cooking challenges and food reviews trending",
                    avgViews: "200K-800K",
                    engagement: "11.4%"
                },
                {
                    topic: "Educational Content",
                    growth: "38.7%",
                    monthlySearches: "15.6M",
                    competition: "35%",
                    category: "Education",
                    opportunity: "Excellent",
                    description: "Study tips, tutorials, and learning content",
                    avgViews: "100K-500K",
                    engagement: "9.8%"
                },
                {
                    topic: "Tech Reviews",
                    growth: "32.1%",
                    monthlySearches: "6.8M",
                    competition: "65%",
                    category: "Technology",
                    opportunity: "Medium",
                    description: "Gadget reviews and tech tutorials",
                    avgViews: "150K-600K",
                    engagement: "8.9%"
                },
                {
                    topic: "AI & Automation",
                    growth: "89.3%",
                    monthlySearches: "4.1M",
                    competition: "42%",
                    category: "Technology",
                    opportunity: "Very High",
                    description: "AI tools, automation tutorials, ChatGPT content",
                    avgViews: "250K-1M",
                    engagement: "13.7%"
                }
            ],
            postingSchedule: {
                timezone: "IST (India Standard Time)",
                optimalDays: ["Tuesday", "Friday", "Saturday"],
                schedule: {
                    Monday: {
                        morning: ["7:00 AM"],
                        afternoon: ["12:00 PM"],
                        evening: ["8:00 PM", "9:00 PM"]
                    },
                    Tuesday: {
                        morning: ["7:00 AM"],
                        afternoon: ["11:00 AM", "12:00 PM"],
                        evening: ["5:00 PM", "6:00 PM", "7:00 PM", "9:00 PM", "10:00 PM"]
                    },
                    Wednesday: {
                        afternoon: ["12:00 PM"],
                        evening: ["3:00 PM", "4:00 PM", "5:00 PM", "6:00 PM"]
                    },
                    Thursday: {
                        evening: ["7:00 PM", "8:00 PM", "9:00 PM"]
                    },
                    Friday: {
                        morning: ["7:00 AM", "8:00 AM", "9:00 AM"],
                        afternoon: ["11:00 AM", "12:00 PM", "1:00 PM"],
                        evening: ["4:00 PM", "5:00 PM", "6:00 PM", "9:00 PM", "10:00 PM", "11:00 PM"]
                    },
                    Saturday: {
                        morning: ["9:00 AM", "10:00 AM"],
                        afternoon: ["3:00 PM", "4:00 PM", "5:00 PM", "6:00 PM"],
                        evening: ["10:00 PM", "11:00 PM", "12:00 AM"]
                    },
                    Sunday: {
                        morning: ["10:00 AM"],
                        afternoon: ["3:00 PM", "5:00 PM"],
                        evening: ["9:00 PM"]
                    }
                }
            },
            contentGaps: [
                {
                    niche: "Educational Tech",
                    searchVolume: "890K monthly",
                    competition: "45%",
                    opportunity: "Very High",
                    description: "Tech tutorials for beginners, software guides",
                    targetAudience: "Students, professionals",
                    contentIdeas: ["ChatGPT tutorials", "Canva guides", "Excel tips"]
                },
                {
                    niche: "Sustainable Living",
                    searchVolume: "620K monthly", 
                    competition: "38%",
                    opportunity: "High",
                    description: "Eco-friendly lifestyle, zero waste tips",
                    targetAudience: "Environmentally conscious viewers",
                    contentIdeas: ["DIY eco products", "Sustainable fashion", "Green living tips"]
                },
                {
                    niche: "Study Tips & Productivity",
                    searchVolume: "1.2M monthly",
                    competition: "41%",
                    opportunity: "Excellent", 
                    description: "Learning techniques, exam preparation",
                    targetAudience: "Students, learners",
                    contentIdeas: ["Memory techniques", "Time management", "Note-taking methods"]
                },
                {
                    niche: "Creator Mental Health",
                    searchVolume: "340K monthly",
                    competition: "25%",
                    opportunity: "Very High",
                    description: "Burnout prevention, work-life balance",
                    targetAudience: "Content creators",
                    contentIdeas: ["Avoiding burnout", "Imposter syndrome", "Work-life balance"]
                },
                {
                    niche: "Regional Content (Hindi/Local)",
                    searchVolume: "2.8M monthly",
                    competition: "35%",
                    opportunity: "Excellent",
                    description: "Local language content, cultural topics",
                    targetAudience: "Regional audience",
                    contentIdeas: ["Hindi tutorials", "Local festivals", "Cultural content"]
                }
            ]
        };

        this.charts = {};
        this.currentSection = 'trending';
        this.init();
    }

    init() {
        console.log('Initializing MagicMitra Dashboard...');
        this.setupEventListeners();
        this.renderTrendingCards();
        this.renderPostingCalendar();
        this.renderContentGaps();
        this.initializeCharts();
        console.log('Dashboard initialized successfully');
    }

    setupEventListeners() {
        console.log('Setting up event listeners...');
        
        // Tab navigation with more robust event handling
        const navTabs = document.querySelectorAll('.nav-tab');
        console.log('Found nav tabs:', navTabs.length);
        
        navTabs.forEach((tab, index) => {
            console.log(`Setting up tab ${index}:`, tab.dataset.section);
            tab.addEventListener('click', (e) => {
                e.preventDefault();
                const section = e.target.dataset.section;
                console.log('Tab clicked:', section);
                this.switchTab(section);
            });
        });

        // Category filter
        const categoryFilter = document.querySelector('.category-filter');
        if (categoryFilter) {
            console.log('Setting up category filter');
            categoryFilter.addEventListener('change', (e) => {
                console.log('Category changed:', e.target.value);
                this.filterTrendingTopics(e.target.value);
            });
        }

        // Export data button
        const exportBtn = document.getElementById('exportData');
        if (exportBtn) {
            console.log('Setting up export button');
            exportBtn.addEventListener('click', (e) => {
                e.preventDefault();
                console.log('Export button clicked');
                this.exportData();
            });
        }

        // Refresh data button
        const refreshBtn = document.getElementById('refreshData');
        if (refreshBtn) {
            console.log('Setting up refresh button');
            refreshBtn.addEventListener('click', (e) => {
                e.preventDefault();
                console.log('Refresh button clicked');
                this.refreshData();
            });
        }

        console.log('Event listeners setup complete');
    }

    switchTab(sectionId) {
        console.log(`Switching to section: ${sectionId}`);
        
        if (!sectionId) {
            console.error('No section ID provided');
            return;
        }

        // Update current section
        this.currentSection = sectionId;

        // Update nav tabs
        document.querySelectorAll('.nav-tab').forEach(tab => {
            tab.classList.remove('active');
        });
        
        const activeTab = document.querySelector(`[data-section="${sectionId}"]`);
        if (activeTab) {
            activeTab.classList.add('active');
            console.log('Active tab updated');
        }

        // Update sections
        document.querySelectorAll('.dashboard-section').forEach(section => {
            section.classList.remove('active');
            section.style.display = 'none';
        });
        
        const activeSection = document.getElementById(sectionId);
        if (activeSection) {
            activeSection.classList.add('active');
            activeSection.style.display = 'block';
            console.log(`Section ${sectionId} activated`);
        }

        // Initialize charts when switching to sections that need them
        setTimeout(() => {
            if (sectionId === 'engagement' && !this.charts.engagement) {
                console.log('Creating engagement chart');
                this.createEngagementChart();
            }
            if (sectionId === 'gaps' && !this.charts.gaps) {
                console.log('Creating gaps chart');
                this.createGapsChart();
            }
            if (sectionId === 'trending' && !this.charts.trending) {
                console.log('Creating trending chart');
                this.createTrendingChart();
            }
        }, 100);
    }

    renderTrendingCards() {
        const container = document.getElementById('trending-cards');
        if (!container) {
            console.error('Trending cards container not found');
            return;
        }

        console.log('Rendering trending cards...');
        container.innerHTML = this.data.trendingTopics.map(topic => `
            <div class="trending-card" data-category="${topic.category}">
                <div class="trending-header">
                    <h3 class="trending-title">${topic.topic}</h3>
                    <span class="growth-badge">${topic.growth}</span>
                </div>
                <div class="trending-stats">
                    <div class="stat">
                        <span class="stat-number">${topic.monthlySearches}</span>
                        <span class="stat-text">Monthly Searches</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">${topic.competition}</span>
                        <span class="stat-text">Competition</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">${topic.engagement}</span>
                        <span class="stat-text">Engagement</span>
                    </div>
                    <div class="stat">
                        <span class="stat-number">${topic.avgViews}</span>
                        <span class="stat-text">Avg Views</span>
                    </div>
                </div>
                <p class="trending-description">${topic.description}</p>
                <span class="category-tag">${topic.category}</span>
            </div>
        `).join('');
        console.log('Trending cards rendered successfully');
    }

    filterTrendingTopics(category) {
        console.log('Filtering trending topics by category:', category);
        const cards = document.querySelectorAll('.trending-card');
        let visibleCount = 0;
        
        cards.forEach(card => {
            if (category === 'all' || card.dataset.category === category) {
                card.style.display = 'block';
                visibleCount++;
            } else {
                card.style.display = 'none';
            }
        });
        
        console.log(`${visibleCount} cards visible after filtering`);
    }

    renderPostingCalendar() {
        const container = document.getElementById('weekly-calendar');
        if (!container) {
            console.error('Weekly calendar container not found');
            return;
        }

        console.log('Rendering posting calendar...');
        const days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday'];
        
        container.innerHTML = days.map(day => {
            const isOptimal = this.data.postingSchedule.optimalDays.includes(day);
            const daySchedule = this.data.postingSchedule.schedule[day] || {};
            
            const allTimes = [
                ...(daySchedule.morning || []),
                ...(daySchedule.afternoon || []),
                ...(daySchedule.evening || [])
            ];

            return `
                <div class="day-card ${isOptimal ? 'optimal' : ''}">
                    <div class="day-name">${day}</div>
                    <div class="time-slots">
                        ${allTimes.map(time => {
                            const isPeak = day === 'Tuesday' && (time.includes('7:00 PM') || time.includes('9:00 PM'));
                            const isGood = !isPeak && allTimes.length > 2;
                            return `<div class="time-slot ${isPeak ? 'peak' : isGood ? 'good' : ''}" title="Engagement rate varies by time">${time}</div>`;
                        }).join('')}
                    </div>
                </div>
            `;
        }).join('');
        console.log('Posting calendar rendered successfully');
    }

    renderContentGaps() {
        const container = document.getElementById('gaps-cards');
        if (!container) {
            console.error('Content gaps container not found');
            return;
        }

        console.log('Rendering content gaps...');
        container.innerHTML = this.data.contentGaps.map(gap => `
            <div class="gap-card">
                <div class="gap-header">
                    <h3 class="gap-title">${gap.niche}</h3>
                    <span class="opportunity-badge ${gap.opportunity.toLowerCase().replace(' ', '-')}">${gap.opportunity}</span>
                </div>
                <div class="gap-metrics">
                    <div class="gap-metric">
                        <div class="gap-metric-value">${gap.searchVolume}</div>
                        <div class="gap-metric-label">Search Volume</div>
                    </div>
                    <div class="gap-metric">
                        <div class="gap-metric-value">${gap.competition}</div>
                        <div class="gap-metric-label">Competition</div>
                    </div>
                </div>
                <p class="gap-description">${gap.description}</p>
                <div class="gap-ideas">
                    <strong>Content Ideas:</strong> ${gap.contentIdeas.join(', ')}
                </div>
            </div>
        `).join('');
        console.log('Content gaps rendered successfully');
    }

    initializeCharts() {
        console.log('Initializing charts...');
        // Initialize trending chart immediately since it's visible
        setTimeout(() => {
            this.createTrendingChart();
        }, 200);
    }

    createTrendingChart() {
        const ctx = document.getElementById('trendingChart');
        if (!ctx) {
            console.error('Trending chart canvas not found');
            return;
        }
        
        if (this.charts.trending) {
            console.log('Trending chart already exists');
            return;
        }

        console.log('Creating trending chart...');
        
        try {
            this.charts.trending = new Chart(ctx, {
                type: 'doughnut',
                data: {
                    labels: this.data.trendingTopics.map(t => t.topic),
                    datasets: [{
                        data: this.data.trendingTopics.map(t => parseFloat(t.growth)),
                        backgroundColor: [
                            '#1FB8CD', '#FFC185', '#B4413C', '#ECEBD5', '#5D878F', '#DB4545'
                        ],
                        borderWidth: 2,
                        borderColor: '#ffffff'
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            position: 'bottom',
                            labels: {
                                padding: 15,
                                usePointStyle: true,
                                font: {
                                    size: 12
                                }
                            }
                        },
                        title: {
                            display: true,
                            text: 'Growth Distribution by Topic',
                            font: {
                                size: 16,
                                weight: 'bold'
                            }
                        }
                    }
                }
            });
            console.log('Trending chart created successfully');
        } catch (error) {
            console.error('Error creating trending chart:', error);
        }
    }

    createEngagementChart() {
        const ctx = document.getElementById('engagementChart');
        if (!ctx) {
            console.error('Engagement chart canvas not found');
            return;
        }
        
        if (this.charts.engagement) {
            console.log('Engagement chart already exists');
            return;
        }

        console.log('Creating engagement chart...');
        
        try {
            this.charts.engagement = new Chart(ctx, {
                type: 'bar',
                data: {
                    labels: ['Excellent (>12%)', 'Good (8-12%)', 'Average (4-8%)', 'Poor (<4%)'],
                    datasets: [{
                        label: 'Engagement Rate Distribution',
                        data: [25, 35, 30, 10],
                        backgroundColor: ['#1FB8CD', '#FFC185', '#B4413C', '#ECEBD5'],
                        borderRadius: 6,
                        borderSkipped: false
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        }
                    },
                    scales: {
                        y: {
                            beginAtZero: true,
                            title: {
                                display: true,
                                text: 'Percentage of Creators'
                            }
                        }
                    }
                }
            });
            console.log('Engagement chart created successfully');
        } catch (error) {
            console.error('Error creating engagement chart:', error);
        }
    }

    createGapsChart() {
        const ctx = document.getElementById('gapsChart');
        if (!ctx) {
            console.error('Gaps chart canvas not found');
            return;
        }
        
        if (this.charts.gaps) {
            console.log('Gaps chart already exists');
            return;
        }

        console.log('Creating gaps chart...');
        
        try {
            this.charts.gaps = new Chart(ctx, {
                type: 'scatter',
                data: {
                    datasets: [{
                        label: 'Content Opportunities',
                        data: this.data.contentGaps.map(gap => ({
                            x: parseFloat(gap.competition),
                            y: parseFloat(gap.searchVolume.replace(/[^\d.]/g, '')),
                            label: gap.niche
                        })),
                        backgroundColor: '#1FB8CD',
                        borderColor: '#1FB8CD',
                        pointRadius: 8,
                        pointHoverRadius: 10
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    scales: {
                        x: {
                            title: {
                                display: true,
                                text: 'Competition Level (%)'
                            },
                            min: 0,
                            max: 100
                        },
                        y: {
                            title: {
                                display: true,
                                text: 'Search Volume (K)'
                            }
                        }
                    },
                    plugins: {
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    return `${context.raw.label}: ${context.raw.y}K searches, ${context.raw.x}% competition`;
                                }
                            }
                        }
                    }
                }
            });
            console.log('Gaps chart created successfully');
        } catch (error) {
            console.error('Error creating gaps chart:', error);
        }
    }

    exportData() {
        console.log('Exporting data...');
        const exportData = {
            timestamp: new Date().toISOString(),
            dashboard: 'MagicMitraVlogs Analytics',
            data: this.data
        };
        
        const dataStr = JSON.stringify(exportData, null, 2);
        const dataUri = 'data:application/json;charset=utf-8,'+ encodeURIComponent(dataStr);
        
        const exportFileDefaultName = `magicmitra-analytics-${new Date().toISOString().split('T')[0]}.json`;
        
        const linkElement = document.createElement('a');
        linkElement.setAttribute('href', dataUri);
        linkElement.setAttribute('download', exportFileDefaultName);
        linkElement.click();
        
        this.showNotification('Data exported successfully!', 'success');
        console.log('Data export completed');
    }

    refreshData() {
        console.log('Refreshing data...');
        const refreshBtn = document.getElementById('refreshData');
        if (!refreshBtn) {
            console.error('Refresh button not found');
            return;
        }
        
        const originalText = refreshBtn.innerHTML;
        
        refreshBtn.innerHTML = '<span class="loading"></span> Refreshing...';
        refreshBtn.disabled = true;
        
        // Simulate data refresh
        setTimeout(() => {
            // Animate counters and update visual elements
            this.animateCounters();
            
            refreshBtn.innerHTML = originalText;
            refreshBtn.disabled = false;
            
            // Show success message
            this.showNotification('Data refreshed successfully!', 'success');
            console.log('Data refresh completed');
        }, 2000);
    }

    animateCounters() {
        console.log('Animating counters...');
        const statValues = document.querySelectorAll('.stat-value, .stat-number');
        statValues.forEach(element => {
            element.style.transform = 'scale(1.1)';
            element.style.color = '#f59e0b';
            
            setTimeout(() => {
                element.style.transform = 'scale(1)';
                element.style.color = '';
            }, 300);
        });
    }

    showNotification(message, type = 'info') {
        console.log('Showing notification:', message, type);
        const notification = document.createElement('div');
        notification.className = `notification ${type}`;
        notification.textContent = message;
        notification.style.cssText = `
            position: fixed;
            top: 20px;
            right: 20px;
            padding: 12px 20px;
            background: #1FB8CD;
            color: white;
            border-radius: 8px;
            box-shadow: 0 4px 12px rgba(0,0,0,0.1);
            z-index: 1000;
            transform: translateX(100%);
            transition: transform 0.3s ease;
        `;
        
        document.body.appendChild(notification);
        
        setTimeout(() => {
            notification.style.transform = 'translateX(0)';
        }, 100);
        
        setTimeout(() => {
            notification.style.transform = 'translateX(100%)';
            setTimeout(() => {
                document.body.removeChild(notification);
            }, 300);
        }, 3000);
    }
}

// Initialize dashboard when DOM is loaded
document.addEventListener('DOMContentLoaded', () => {
    console.log('DOM loaded, initializing dashboard...');
    try {
        new MagicMitraDashboard();
    } catch (error) {
        console.error('Error initializing dashboard:', error);
    }
});

