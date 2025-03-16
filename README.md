<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Five Horizon's Comprehensive Analysis</title>
  <!-- Include React, ReactDOM, and Babel for JSX -->
  <script src="https://unpkg.com/react@17/umd/react.development.js"></script>
  <script src="https://unpkg.com/react-dom@17/umd/react-dom.development.js"></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  <!-- Basic styling -->
  <style>
    body {
      font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
      margin: 0;
      padding: 0;
      background-color: #f7f7f7;
    }
    
    .container {
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 1rem;
    }
    
    .navbar {
      position: sticky;
      top: 0;
      background-color: white;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
      padding: 1rem 0;
      z-index: 50;
    }
    
    .navbar-inner {
      display: flex;
      align-items: center;
    }
    
    .navbar-brand {
      font-size: 1.25rem;
      font-weight: bold;
      margin-right: 2rem;
    }
    
    .navbar-nav {
      display: flex;
      gap: 1rem;
    }
    
    .nav-button {
      padding: 0.5rem 1rem;
      border: none;
      background: none;
      border-radius: 0.25rem;
      cursor: pointer;
      font-weight: 500;
    }
    
    .nav-button:hover {
      background-color: #f3f4f6;
    }
    
    .section {
      margin-bottom: 2rem;
      padding-top: 2rem;
    }
    
    .section-title {
      font-size: 1.875rem;
      font-weight: bold;
      margin-bottom: 1rem;
    }
    
    .card {
      background-color: white;
      border-radius: 0.5rem;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.1);
      margin-bottom: 1rem;
      overflow: hidden;
    }
    
    .card-header {
      padding: 1rem;
      border-bottom: 1px solid #e5e7eb;
    }
    
    .card-title {
      font-size: 1.25rem;
      font-weight: bold;
      margin: 0;
    }
    
    .card-content {
      padding: 1rem;
    }
    
    .text-muted {
      color: #6b7280;
    }
    
    .grid {
      display: grid;
      gap: 1rem;
    }
    
    @media (min-width: 768px) {
      .grid-cols-2 {
        grid-template-columns: repeat(2, 1fr);
      }
    }
    
    .progress-bar {
      height: 0.5rem;
      background-color: #e5e7eb;
      border-radius: 9999px;
      overflow: hidden;
    }
    
    .progress-value {
      height: 100%;
      background-color: #3b82f6;
      border-radius: 9999px;
    }
    
    .flex {
      display: flex;
    }
    
    .justify-between {
      justify-content: space-between;
    }
    
    .items-center {
      align-items: center;
    }
    
    .gap-2 {
      gap: 0.5rem;
    }
    
    .mt-4 {
      margin-top: 1rem;
    }
    
    .mb-2 {
      margin-bottom: 0.5rem;
    }
    
    .my-4 {
      margin-top: 1rem;
      margin-bottom: 1rem;
    }
    
    .space-y-4 > * + * {
      margin-top: 1rem;
    }
    
    hr {
      border: 0;
      border-top: 1px solid #e5e7eb;
    }
    
    ul {
      padding-left: 1.5rem;
    }
  </style>
</head>
<body>
  <div id="root"></div>

  <script type="text/babel">
    // Main App Component
    function App() {
      return (
        <div>
          <Navbar />
          <main className="container">
            <div id="summary" className="section">
              <StreamSummary />
            </div>
            <div id="content" className="section">
              <ContentBreakdown />
            </div>
            <div id="viewership" className="section">
              <ViewershipAnalysis />
            </div>
            <div id="technical" className="section">
              <TechnicalPerformance />
            </div>
            <div id="improvements" className="section">
              <AreasImprovement />
            </div>
          </main>
        </div>
      );
    }

    // Navigation Component
    function Navbar() {
      const navItems = [
        { href: "#summary", label: "Stream Summary" },
        { href: "#content", label: "Content Breakdown" },
        { href: "#viewership", label: "Viewership" },
        { href: "#technical", label: "Technical" },
        { href: "#improvements", label: "Improvements" }
      ];

      const scrollToSection = (id) => {
        const element = document.querySelector(id);
        if (element) {
          element.scrollIntoView({ behavior: "smooth" });
        }
      };

      return (
        <nav className="navbar">
          <div className="container">
            <div className="navbar-inner">
              <div className="navbar-brand">
                Five Horizon's Comprehensive Analysis
              </div>
              <div className="navbar-nav">
                {navItems.map((item) => (
                  <button
                    key={item.href}
                    className="nav-button"
                    onClick={() => scrollToSection(item.href)}
                  >
                    {item.label}
                  </button>
                ))}
              </div>
            </div>
          </div>
        </nav>
      );
    }

    // Stream Summary Component
    function StreamSummary() {
      return (
        <div>
          <h2 className="section-title">Stream Summary</h2>
          <div className="card">
            <div className="card-header">
              <h3 className="card-title">Overview</h3>
            </div>
            <div className="card-content">
              <p>
                Our stream was a mix of gaming and real discussion about procrastination. We started things off by officially introducing the topic. After that, we jumped into "Mega Fun Obby" — a game in Roblox — while sharing our personal struggles with procrastination.
              </p>
              <p>
                We had some pretty relatable discussions about why we procrastinate, how it affects us, and whether it sometimes works in our favor. Everyone agreed that distractions, stress, and mood play a huge role in why we procrastinate.
              </p>
              <p>
                To wrap things up, we shared tips on overcoming procrastination, such as setting goals, breaking tasks into smaller steps and having better time management skills. Ashanti—our host—ended the stream with a reminder that procrastination is not just laziness—it is about mindset and habits, and small changes can make a big difference.
              </p>
            </div>
          </div>
        </div>
      );
    }

    // Content Breakdown Component
    function ContentBreakdown() {
      return (
        <div>
          <h2 className="section-title">Content Breakdown</h2>
          <div className="card">
            <div className="card-header">
              <h3 className="card-title">Stream Structure</h3>
            </div>
            <div className="card-content">
              <div>
                <h4 className="mb-2">Introduction (0:00 - 2:12)</h4>
                <p className="text-muted">Stream preparation and topic introduction</p>
              </div>
              <hr className="my-4" />
              <div>
                <h4 className="mb-2">Main Discussion (2:12 - 19:40)</h4>
                <p className="text-muted">
                  Gameplay of Mega Fun Obby while discussing personal experiences with procrastination
                </p>
              </div>
              <hr className="my-4" />
              <div>
                <h4 className="mb-2">Causes & Impact (19:40+)</h4>
                <p className="text-muted">
                  Deep dive into causes of procrastination, its impact on different aspects of life, and strategies to overcome it
                </p>
              </div>
              <hr className="my-4" />
              <div>
                <h4 className="mb-2">Closing</h4>
                <p className="text-muted">
                  Final thoughts and takeaways about procrastination, mindset, and habits
                </p>
              </div>
            </div>
          </div>
        </div>
      );
    }

    // Viewership Analysis Component
    function ViewershipAnalysis() {
      return (
        <div>
          <h2 className="section-title">Viewership Analysis</h2>
          <div className="grid grid-cols-2">
            <div className="card">
              <div className="card-header">
                <h3 className="card-title">Total Views</h3>
              </div>
              <div className="card-content">
                <div style={{ fontSize: '2rem', fontWeight: 'bold', marginBottom: '1rem' }}>371</div>
                <div className="space-y-4">
                  <div>
                    <div className="flex justify-between mb-2">
                      <span>Live Viewers</span>
                      <span>13</span>
                    </div>
                    <div className="progress-bar">
                      <div className="progress-value" style={{ width: '3.5%' }}></div>
                    </div>
                  </div>
                  <div>
                    <div className="flex justify-between mb-2">
                      <span>Replay Views</span>
                      <span>358</span>
                    </div>
                    <div className="progress-bar">
                      <div className="progress-value" style={{ width: '96.5%' }}></div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
            <div className="card">
              <div className="card-header">
                <h3 className="card-title">Engagement</h3>
              </div>
              <div className="card-content">
                <div className="space-y-4">
                  <div>
                    <div style={{ fontSize: '0.875rem', fontWeight: '500' }}>Comments</div>
                    <div style={{ fontSize: '1.5rem', fontWeight: 'bold' }}>10</div>
                  </div>
                  <div>
                    <div style={{ fontSize: '0.875rem', fontWeight: '500' }}>Reactions</div>
                    <div style={{ fontSize: '1.5rem', fontWeight: 'bold' }}>16</div>
                  </div>
                  <div>
                    <div style={{ fontSize: '0.875rem', fontWeight: '500' }}>Peak Concurrent Viewers</div>
                    <div style={{ fontSize: '1.5rem', fontWeight: 'bold' }}>13</div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      );
    }

    // Technical Performance Component
    function TechnicalPerformance() {
      return (
        <div>
          <h2 className="section-title">Technical Performance</h2>
          <div className="grid grid-cols-2">
            <div className="card">
              <div className="card-header">
                <h3 className="card-title">Video Quality</h3>
              </div>
              <div className="card-content">
                <p className="text-muted">
                  Video resolution was clear and smooth though limited by connectivity issues. Webcam functionality was unavailable due to application constraints.
                </p>
              </div>
            </div>
            <div className="card">
              <div className="card-header">
                <h3 className="card-title">Audio Performance</h3>
              </div>
              <div className="card-content">
                <div className="flex items-center gap-2">
                  <span style={{ color: '#f59e0b' }}>⚠️</span>
                  <span>Audio buffering and volume issues</span>
                </div>
                <p className="text-muted">
                  Audio experienced buffering, muffled quality, and low volume. Some parts of discussions were cut off.
                </p>
              </div>
            </div>
            <div className="card">
              <div className="card-header">
                <h3 className="card-title">Streaming Setup</h3>
              </div>
              <div className="card-content">
                <p className="text-muted">
                  Basic streaming setup using Streamlabs with 2 laptops (one for webcam and mic). Successfully managed stream despite initial software issues.
                </p>
              </div>
            </div>
          </div>
        </div>
      );
    }

    // Areas for Improvement Component
    function AreasImprovement() {
      return (
        <div>
          <h2 className="section-title">Areas for Improvement</h2>
          <div className="grid grid-cols-2">
            <div className="card">
              <div className="card-header">
                <h3 className="card-title">Technical Execution</h3>
              </div>
              <div className="card-content">
                <ul className="text-muted">
                  <li>Improve video quality and resolution</li>
                  <li>Fix audio issues and ensure consistent volume</li>
                  <li>Resolve webcam functionality</li>
                  <li>Enhance streaming setup with better equipment</li>
                </ul>
              </div>
            </div>
            <div className="card">
              <div className="card-header">
                <h3 className="card-title">Audience Engagement</h3>
              </div>
              <div className="card-content">
                <ul className="text-muted">
                  <li>Maintain consistent viewer interaction</li>
                  <li>Balance Q&A segments with live engagement</li>
                  <li>Implement more interactive elements</li>
                  <li>Develop strategies to retain viewers</li>
                </ul>
              </div>
            </div>
            <div className="card" style={{ gridColumn: '1 / span 2' }}>
              <div className="card-header">
                <h3 className="card-title">Overall Improvements</h3>
              </div>
              <div className="card-content">
                <div className="space-y-4">
                  <div className="flex items-start gap-2">
                    <span style={{ color: '#3b82f6' }}>ℹ️</span>
                    <p className="text-muted">
                      Focus on a better balance between content delivery and viewer interaction.
                    </p>
                  </div>
                  <div className="flex items-start gap-2">
                    <span style={{ color: '#3b82f6' }}>ℹ️</span>
                    <p className="text-muted">
                      Consider a structured approach for addressing technical issues and engagement challenges.
                    </p>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      );
    }

    // Render the App
    ReactDOM.render(<App />, document.getElementById('root'));
  </script>
</body>
</html>

