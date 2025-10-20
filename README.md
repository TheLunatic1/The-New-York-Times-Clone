<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The New York Times</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: "Georgia", "Times New Roman", serif;
        }
        
        body {
            color: #121212;
            line-height: 1.5;
            background-color: #fff;
            max-width: 1400px;
            margin: 0 auto;
        }
        
        a {
            color: #121212;
            text-decoration: none;
        }
        
        a:hover {
            text-decoration: underline;
        }
        
        
        .site-header {
            padding: 10px 0;
            position: sticky;
            top: 0;
            background-color: white;
            z-index: 100;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 0 20px;
        }
        
        .date {
            font-size: 14px;
            color: #666;
        }
        
        .nyt-logo {
            font-family: "Old English Text MT", "Times New Roman", serif;
            font-size: 36px;
            font-weight: normal;
            text-align: center;
            margin: 0;
        }
        
        .header-buttons {
            display: flex;
            gap: 10px;
        }
        
        .subscribe-btn {
            background-color: #567b95;
            color: white;
            border: none;
            padding: 8px 12px;
            border-radius: 3px;
            font-weight: bold;
            cursor: pointer;
            font-size: 12px;
        }
        
        .login-btn {
            background-color: white;
            color: #567b95;
            border: 1px solid #567b95;
            padding: 8px 12px;
            border-radius: 3px;
            font-weight: bold;
            cursor: pointer;
            font-size: 12px;
        }
        
        
        .site-nav {
            border-bottom: 1px solid #000000;
            padding: 10px 0;
        }
        
        .nav-container {
            padding: 0 20px;
        }
        
        .nav-list {
            display: flex;
            list-style: none;
            justify-content: space-between;
            flex-wrap: wrap;
        }
        
        .nav-item a {
            font-size: 13px;
            font-weight: bold;
        }
        
        
        .container {
            border-top: 1px solid #000000;
            margin-top: 2px;
            display: grid;
            grid-template-columns: 1fr 2fr 1fr;
            gap: 20px;
            padding: 20px;
        }
        
        
        .left-column {
            padding-right: 20px;
        }
        
        
        .center-column {
            border-right: 1px solid #e2e2e2;
            padding-right: 20px;
        }
        
        .featured-article {
            margin-bottom: 30px;
        }
        
        .featured-title {
            font-size: 28px;
            font-weight: bold;
            margin-bottom: 10px;
            line-height: 1.2;
        }
        
        
        
        .featured-summary {
            font-size: 16px;
            margin-bottom: 10px;
            color: #333;
        }
        
        .featured-meta {
            color: #666;
            font-size: 12px;
        }
        
        
        .article-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 20px;
        }
        
        .article-card {
            margin-bottom: 20px;
        }
        
        .article-title {
            font-size: 18px;
            font-weight: bold;
            margin-bottom: 8px;
            line-height: 1.3;
        }
        
        
        
        .article-summary {
            font-size: 14px;
            margin-bottom: 8px;
            color: #333;
        }
        
        .article-meta {
            color: #666;
            font-size: 12px;
        }
        
        
        .column-section {
            margin-bottom: 30px;
        }
        
        
        
        .sidebar-list {
            list-style: none;
        }
        
        .sidebar-item {
            margin-bottom: 15px;
            padding-bottom: 15px;
            border-bottom: 1px solid #f5f5f5;
        }
        
        .sidebar-item:last-child {
            border-bottom: none;
        }
        
        .sidebar-item-title {
            font-weight: bold;
            margin-bottom: 5px;
            font-size: 15px;
        }
        
        .sidebar-item-meta {
            color: #666;
            font-size: 12px;
        }
        
        
        .opinion-section {
            margin-top: 30px;
        }
        
        .opinion-grid {
            display: grid;
            grid-template-columns: 1fr;
            gap: 15px;
        }
        
        .opinion-card {
            margin-bottom: 15px;
        }
        
        .opinion-author {
            font-weight: bold;
            margin-bottom: 5px;
            font-size: 14px;
        }
        
        .opinion-title {
            font-size: 16px;
            margin-bottom: 5px;
            line-height: 1.3;
        }
        
        .opinion-meta {
            color: #666;
            font-size: 12px;
        }
        
        .site-footer {
            border-top: 2px solid #e2e2e2;
            margin-top: 40px;
            padding: 30px 20px;
            background-color: #f5f5f5;
        }
        
        .footer-links {
            display: flex;
            justify-content: space-between;
            margin-bottom: 20px;
            flex-wrap: wrap;
        }
        
        .footer-column {
            flex: 1;
            min-width: 150px;
            margin-bottom: 20px;
        }
        
        .footer-column-title {
            font-weight: bold;
            margin-bottom: 10px;
            font-size: 14px;
        }
        
        .footer-list {
            list-style: none;
        }
        
        .footer-item {
            margin-bottom: 5px;
        }
        
        .footer-item a {
            font-size: 12px;
            color: #666;
        }
        
        .footer-bottom {
            border-top: 1px solid #e2e2e2;
            padding-top: 20px;
            font-size: 12px;
            color: #666;
            text-align: center;
        }
        
        
        @media (max-width: 1024px) {
            .container {
                grid-template-columns: 1fr 1fr;
            }
            
            .right-column {
                grid-column: span 2;
                border-top: 1px solid #e2e2e2;
                padding-top: 20px;
                margin-top: 20px;
            }
        }
        
        @media (max-width: 768px) {
            .container {
                grid-template-columns: 1fr;
            }
            
            .left-column, .center-column, .right-column {
                border-right: none;
                padding-right: 0;
            }
            
            .right-column {
                grid-column: span 1;
            }
            
            .article-grid {
                grid-template-columns: 1fr;
            }
            
            .nav-list {
                gap: 10px;
            }
        }
    </style>
</head>
<body>
    <header class="site-header">
        <div class="header-container">
            <div class="date">Wednesday, October 20, 2025 <br>Today’s Paper</div>
            
            <h1 class="nyt-logo">The New York Times</h1>
            <div class="header-buttons">
                <button class="subscribe-btn">SUBSCRIBE</button>
                <button class="login-btn">LOG IN</button>
            </div>
        </div>
    </header>
    
    <nav class="site-nav">
        <div class="nav-container">
            <ul class="nav-list">
                <li class="nav-item"><a href="">World</a></li>
                <li class="nav-item"><a href="">U.S.</a></li>
                <li class="nav-item"><a href="">Politics</a></li>
                <li class="nav-item"><a href="">N.Y.</a></li>
                <li class="nav-item"><a href="">Business</a></li>
                <li class="nav-item"><a href="">Opinion</a></li>
                <li class="nav-item"><a href="">Science</a></li>
                <li class="nav-item" style="border-right: 2px #363232"><a href="">Health</a></li>
                <li class="nav-item" style="border-left: 2px #363232"><a href="">Sports</a></li>
                <li class="nav-item"><a href="">Arts</a></li>
                <li class="nav-item"><a href="">Books</a></li>
                <li class="nav-item"><a href="">Style</a></li>
                <li class="nav-item"><a href="">Food</a></li>
                <li class="nav-item"><a href="">Travel</a></li>
                <li class="nav-item"><a href="">Magazine</a></li>
                <li class="nav-item"><a href="">T Magazine</a></li>
            </ul>
        </div>
    </nav>
    
    <main class="container">
        <div class="left-column">
            <div class="column-section">
                <article class="article-card">
                    <h4 class="article-title">Federal Reserve Signals Potential Interest Rate Pause</h4>
                    <div class="article-image"><img src="https://placehold.co/310x130" alt=""></div>
                    <p class="article-summary">Central bank officials point to cooling inflation as reason to hold rates steady at next meeting.</p>
                    <div class="article-meta">3 MIN READ</div>
                </article>
                
                <article class="article-card">
                    <h4 class="article-title">New Study Reveals Benefits of Mediterranean Diet</h4>
                    <div class="article-image"><img src="https://placehold.co/310x130" alt=""></div>
                    <p class="article-summary">Research confirms significant heart health advantages and potential cognitive benefits for older adults.</p>
                    <div class="article-meta">2 MIN READ</div>
                </article>
            </div>
            
            <div class="column-section">
                <ul class="sidebar-list">
                    <li class="sidebar-item">
                        <div class="sidebar-item-title">The Secret Life of Urban Squirrels</div>
                        <div class="sidebar-item-meta">2 hours ago</div>
                    </li>
                    <li class="sidebar-item">
                        <div class="sidebar-item-title">Why Everyone Is Talking About This New Restaurant</div>
                        <div class="sidebar-item-meta">4 hours ago</div>
                    </li>
                    <li class="sidebar-item">
                        <div class="sidebar-item-title">The Complicated Legacy of a Literary Giant</div>
                        <div class="sidebar-item-meta">6 hours ago</div>
                    </li>
                    <li class="sidebar-item">
                        <div class="sidebar-item-title">How to Negotiate a Better Salary in Any Economy</div>
                        <div class="sidebar-item-meta">8 hours ago</div>
                    </li>
                </ul>
            </div>
        </div>
        
        <div class="center-column">
            <article class="featured-article">
                <h2 class="featured-title">Major Climate Summit Concludes With New Global Agreement</h2>
                <div class="featured-image"><img src="https://placehold.co/650x400" alt=""></div>
                <p class="featured-summary">World leaders have reached a landmark agreement to accelerate carbon emission reductions, though critics say the measures don't go far enough to address the climate crisis. The pact includes commitments from nearly 200 countries.</p>
                <div class="featured-meta">5 MIN READ</div>
            </article>
            
            <div class="article-grid">
                <article class="article-card">
                    <h3 class="article-title">Tech Giants Report Mixed Quarterly Results</h3>
                    <div class="article-image"><img src="https://placehold.co/310x130" alt=""></div>
                    <p class="article-summary">While some companies beat expectations, others face challenges in the competitive digital advertising market.</p>
                    <div class="article-meta">4 MIN READ</div>
                </article>
                
                <article class="article-card">
                    <h3 class="article-title">Major Film Festival Announces Competition Lineup</h3>
                    <div class="article-image"><img src="https://placehold.co/310x130" alt=""></div>
                    <p class="article-summary">International directors dominate this year's selection, with several surprising omissions from established filmmakers.</p>
                    <div class="article-meta">3 MIN READ</div>
                </article>
                
                <article class="article-card">
                    <h3 class="article-title">Breakthrough in Renewable Energy Storage</h3>
                    <div class="article-image"><img src="https://placehold.co/310x130" alt=""></div>
                    <p class="article-summary">Scientists develop new battery technology that could make solar and wind power more reliable.</p>
                    <div class="article-meta">3 MIN READ</div>
                </article>
                
                <article class="article-card">
                    <h3 class="article-title">Historic Peace Deal Signed After Decades of Conflict</h3>
                    <div class="article-image"><img src="https://placehold.co/310x130" alt=""></div>
                    <p class="article-summary">The agreement ends one of the world's longest-running territorial disputes, with international observers praising the diplomatic breakthrough.</p>
                    <div class="article-meta">6 MIN READ</div>
                </article>
            </div>
        </div>

        <div class="right-column">
            <div class="column-section">
                <div class="opinion-grid">
                    <article class="opinion-card">
                        <div class="opinion-author">By Paul Krugman</div>
                        <h4 class="opinion-title">The Economic Case for Climate Action</h4>
                        <div class="opinion-meta">Today</div>
                    </article>
                    
                    <article class="opinion-card">
                        <div class="opinion-author">By Gail Collins</div>
                        <h4 class="opinion-title">What We're Getting Wrong About Education</h4>
                        <div class="opinion-meta">Today</div>
                    </article>
                    
                    <article class="opinion-card">
                        <div class="opinion-author">By Bret Stephens</div>
                        <h4 class="opinion-title">The Dangers of Digital Isolation</h4>
                        <div class="opinion-meta">Yesterday</div>
                    </article>
                    
                    <article class="opinion-card">
                        <div class="opinion-author">By Maureen Dowd</div>
                        <h4 class="opinion-title">A Return to Civility in Politics?</h4>
                        <div class="opinion-meta">Yesterday</div>
                    </article>
                </div>
            </div>
            
            <div class="column-section">
                <ul class="sidebar-list">
                    <li class="sidebar-item">
                        <div class="sidebar-item-title">The Photographer Who Captured a Changing Nation</div>
                        <div class="sidebar-item-meta">Sept. 28</div>
                    </li>
                    <li class="sidebar-item">
                        <div class="sidebar-item-title">Rediscovering the Lost Art of Letter Writing</div>
                        <div class="sidebar-item-meta">Sept. 25</div>
                    </li>
                    <li class="sidebar-item">
                        <div class="sidebar-item-title">A Chef's Journey From Refugee to Restaurant Owner</div>
                        <div class="sidebar-item-meta">Sept. 22</div>
                    </li>
                </ul>
            </div>
            
            
        </div>
    </main>
    
    <footer class="site-footer">
        <div class="footer-links">
            <div class="footer-column">
                <h4 class="footer-column-title">NEWS</h4>
                <ul class="footer-list">
                    <li class="footer-item"><a href="#">Home Page</a></li>
                    <li class="footer-item"><a href="#">World</a></li>
                    <li class="footer-item"><a href="#">U.S.</a></li>
                    <li class="footer-item"><a href="#">Politics</a></li>
                    <li class="footer-item"><a href="#">New York</a></li>
                    <li class="footer-item"><a href="#">Business</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h4 class="footer-column-title">OPINION</h4>
                <ul class="footer-list">
                    <li class="footer-item"><a href="#">Today's Opinion</a></li>
                    <li class="footer-item"><a href="#">Op-Ed Columnists</a></li>
                    <li class="footer-item"><a href="#">Editorials</a></li>
                    <li class="footer-item"><a href="#">Op-Ed Contributors</a></li>
                    <li class="footer-item"><a href="#">Letters</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h4 class="footer-column-title">ARTS</h4>
                <ul class="footer-list">
                    <li class="footer-item"><a href="#">Today's Arts</a></li>
                    <li class="footer-item"><a href="#">Art & Design</a></li>
                    <li class="footer-item"><a href="#">Books</a></li>
                    <li class="footer-item"><a href="#">Dance</a></li>
                    <li class="footer-item"><a href="#">Movies</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h4 class="footer-column-title">LIVING</h4>
                <ul class="footer-list">
                    <li class="footer-item"><a href="#">Automotive</a></li>
                    <li class="footer-item"><a href="#">Crossword</a></li>
                    <li class="footer-item"><a href="#">Food</a></li>
                    <li class="footer-item"><a href="#">Health</a></li>
                    <li class="footer-item"><a href="#">Magazine</a></li>
                </ul>
            </div>
            
            <div class="footer-column">
                <h4 class="footer-column-title">MORE</h4>
                <ul class="footer-list">
                    <li class="footer-item"><a href="#">Reader Center</a></li>
                    <li class="footer-item"><a href="#">The Athletic</a></li>
                    <li class="footer-item"><a href="#">Wirecutter</a></li>
                    <li class="footer-item"><a href="#">Cooking</a></li>
                    <li class="footer-item"><a href="#">Games</a></li>
                </ul>
            </div>
        </div>
        
        <div class="footer-bottom">
            <p>© 2025 The New York Times Company. All rights reserved.</p>
        </div>
    </footer>
</body>
</html>
