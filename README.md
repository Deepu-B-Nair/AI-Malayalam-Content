<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Malayalam News Automation System - Dashboard</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@fortawesome/fontawesome-free@6.4.0/css/all.min.css">
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <style>
        .news-card {
            transition: all 0.3s ease;
        }
        .news-card:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(0,0,0,0.1);
        }
        .status-indicator {
            animation: pulse 2s infinite;
        }
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.5; }
        }
        .malayalam-text {
            font-family: 'Noto Sans Malayalam', sans-serif;
        }
    </style>
</head>
<body class="bg-gray-50">
    <!-- Header -->
    <header class="bg-white shadow-sm border-b">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
            <div class="flex items-center justify-between">
                <div class="flex items-center">
                    <div class="w-10 h-10 bg-red-600 rounded-lg flex items-center justify-center mr-3">
                        <i class="fas fa-broadcast-tower text-white"></i>
                    </div>
                    <div>
                        <h1 class="text-xl font-bold text-gray-900">Malayalam News Automation</h1>
                        <p class="text-sm text-gray-500">AI-Powered Content Creation & Distribution</p>
                    </div>
                </div>
                <div class="flex items-center space-x-4">
                    <div class="flex items-center text-green-600">
                        <div class="w-2 h-2 bg-green-500 rounded-full status-indicator mr-2"></div>
                        <span class="text-sm font-medium">System Active</span>
                    </div>
                    <button class="bg-blue-600 text-white px-4 py-2 rounded-lg hover:bg-blue-700 transition-colors">
                        <i class="fas fa-cog mr-2"></i>Settings
                    </button>
                </div>
            </div>
        </div>
    </header>

    <!-- Main Dashboard -->
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-6">
        
        <!-- Stats Overview -->
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mb-8">
            <div class="bg-white rounded-lg shadow p-6">
                <div class="flex items-center">
                    <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mr-4">
                        <i class="fas fa-newspaper text-blue-600 text-xl"></i>
                    </div>
                    <div>
                        <p class="text-sm font-medium text-gray-500">News Monitored Today</p>
                        <p class="text-2xl font-bold text-gray-900">247</p>
                        <p class="text-xs text-green-600">+18% from yesterday</p>
                    </div>
                </div>
            </div>
            
            <div class="bg-white rounded-lg shadow p-6">
                <div class="flex items-center">
                    <div class="w-12 h-12 bg-green-100 rounded-lg flex items-center justify-center mr-4">
                        <i class="fas fa-share-alt text-green-600 text-xl"></i>
                    </div>
                    <div>
                        <p class="text-sm font-medium text-gray-500">Posts Created</p>
                        <p class="text-2xl font-bold text-gray-900">89</p>
                        <p class="text-xs text-green-600">5.2 posts/hour avg</p>
                    </div>
                </div>
            </div>
            
            <div class="bg-white rounded-lg shadow p-6">
                <div class="flex items-center">
                    <div class="w-12 h-12 bg-purple-100 rounded-lg flex items-center justify-center mr-4">
                        <i class="fas fa-heart text-purple-600 text-xl"></i>
                    </div>
                    <div>
                        <p class="text-sm font-medium text-gray-500">Total Engagement</p>
                        <p class="text-2xl font-bold text-gray-900">12.4K</p>
                        <p class="text-xs text-green-600">+24% engagement rate</p>
                    </div>
                </div>
            </div>
            
            <div class="bg-white rounded-lg shadow p-6">
                <div class="flex items-center">
                    <div class="w-12 h-12 bg-orange-100 rounded-lg flex items-center justify-center mr-4">
                        <i class="fas fa-clock text-orange-600 text-xl"></i>
                    </div>
                    <div>
                        <p class="text-sm font-medium text-gray-500">Next Post</p>
                        <p class="text-2xl font-bold text-gray-900">14m</p>
                        <p class="text-xs text-blue-600">Breaking news ready</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Main Content Area -->
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-8">
            
            <!-- Live News Monitoring -->
            <div class="lg:col-span-2">
                <div class="bg-white rounded-lg shadow">
                    <div class="p-6 border-b border-gray-200">
                        <div class="flex items-center justify-between">
                            <h2 class="text-lg font-semibold text-gray-900">Live News Monitoring</h2>
                            <div class="flex items-center space-x-2">
                                <div class="w-2 h-2 bg-red-500 rounded-full status-indicator"></div>
                                <span class="text-sm text-gray-500">Live</span>
                            </div>
                        </div>
                    </div>
                    
                    <div class="p-6">
                        <div class="space-y-4">
                            <!-- News Item 1 -->
                            <div class="news-card border border-gray-200 rounded-lg p-4">
                                <div class="flex items-start justify-between">
                                    <div class="flex-1">
                                        <div class="flex items-center mb-2">
                                            <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0IiBmaWxsPSIjRUY0NDQ0Ii8+CjxwYXRoIGQ9Ik0xMiA4VjE2TTggMTJIMTZNMjEgMTJBOSA5IDAgMTEzIDEyQTkgOSAwIDAxMjEgMTJaIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K" alt="Asianet News" class="w-6 h-6 rounded mr-2">
                            <span class="text-sm font-medium text-gray-900">Asianet News</span>
                            <span class="ml-2 text-xs text-gray-500">2 min ago</span>
                        </div>
                        <h3 class="font-semibold text-gray-900 mb-2">കേരളത്തിൽ പുതിയ IT പാർക്ക് പ്രഖ്യാപനം - 5000 തൊഴിലവസരങ്ങൾ സൃഷ്ടിക്കും</h3>
                        <p class="text-sm text-gray-600 mb-3">തിരുവനന്തപുരം ടെക്നോപാർക്കിൽ പുതിയ IT കമ്പ്ലക്സിന് അനുമതി. അടുത്ത രണ്ട് വർഷത്തിനുള്ളിൽ 5000 നേരിട്ടുള്ള തൊഴിലവസരങ്ങൾ സൃഷ്ടിക്കാൻ സാധിക്കും എന്ന് അധികൃതർ അറിയിച്ചു.</p>
                        <div class="flex items-center justify-between">
                            <div class="flex items-center space-x-2">
                                <span class="bg-green-100 text-green-800 text-xs px-2 py-1 rounded">Technology</span>
                                <span class="bg-blue-100 text-blue-800 text-xs px-2 py-1 rounded">Kerala</span>
                            </div>
                            <div class="flex items-center space-x-2">
                                <span class="text-xs text-gray-500">Engagement Score: 8.5/10</span>
                                <button class="bg-green-500 text-white px-3 py-1 rounded text-xs hover:bg-green-600">Create Post</button>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- News Item 2 -->
                <div class="news-card border border-gray-200 rounded-lg p-4">
                    <div class="flex items-start justify-between">
                        <div class="flex-1">
                            <div class="flex items-center mb-2">
                                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0IiBmaWxsPSIjMzMzM0ZGIi8+CjxwYXRoIGQ9Ik0xMiA4VjE2TTggMTJIMTZNMjEgMTJBOSA5IDAgMTEzIDEyQTkgOSAwIDAxMjEgMTJaIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K" alt="Manorama News" class="w-6 h-6 rounded mr-2">
                                <span class="text-sm font-medium text-gray-900">Manorama News</span>
                                <span class="ml-2 text-xs text-gray-500">5 min ago</span>
                            </div>
                            <h3 class="font-semibold text-gray-900 mb-2">കൊച്ചി മെട്രോയിൽ പുതിയ റൂട്ട് വിപുലീകരണം - ഇൻഫോപാർക്ക് വരെ എത്തും</h3>
                            <p class="text-sm text-gray-600 mb-3">കൊച്ചി മെട്രോയുടെ പുതിയ ഫേസ് പ്രവർത്തനങ്ങൾ ആരംഭിച്ചു. അടുത്ത വർഷം മുതൽ യാത്രക്കാർക്ക് ഇൻഫോപാർക്ക് വരെ നേരിട്ട് യാത്ര ചെയ്യാൻ കഴിയും.</p>
                            <div class="flex items-center justify-between">
                                <div class="flex items-center space-x-2">
                                    <span class="bg-purple-100 text-purple-800 text-xs px-2 py-1 rounded">Transport</span>
                                    <span class="bg-orange-100 text-orange-800 text-xs px-2 py-1 rounded">Kochi</span>
                                </div>
                                <div class="flex items-center space-x-2">
                                    <span class="text-xs text-gray-500">Engagement Score: 7.8/10</span>
                                    <button class="bg-green-500 text-white px-3 py-1 rounded text-xs hover:bg-green-600">Create Post</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>

                <!-- News Item 3 -->
                <div class="news-card border border-gray-200 rounded-lg p-4">
                    <div class="flex items-start justify-between">
                        <div class="flex-1">
                            <div class="flex items-center mb-2">
                                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0IiBmaWxsPSIjRkY2NjAwIi8+CjxwYXRoIGQ9Ik0xMiA4VjE2TTggMTJIMTZNMjEgMTJBOSA5IDAgMTEzIDEyQTkgOSAwIDAxMjEgMTJaIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K" alt="24 News" class="w-6 h-6 rounded mr-2">
                                <span class="text-sm font-medium text-gray-900">24 News</span>
                                <span class="ml-2 text-xs text-gray-500">8 min ago</span>
                            </div>
                            <h3 class="font-semibold text-gray-900 mb-2">മലയാളം സിനിമയ്ക്ക് ദേശീയ അവാർഡ് - 'മിന്നാൽ മുരളി' മികച്ച ചിത്രത്തിന് അംഗീകാരം</h3>
                            <p class="text-sm text-gray-600 mb-3">കേരള സിനിമയുടെ വീണ്ടുമൊരു നേട്ടം. 'മിന്നാൽ മുരളി' എന്ന ചിത്രത്തിന് ദേശീയ ചലച്ചിത്ര അവാർഡ് ലഭിച്ചു. സംവിധായകൻ രാഹുൽ സാദാശിവൻ സന്തോഷം പങ്കുവച്ചു.</p>
                            <div class="flex items-center justify-between">
                                <div class="flex items-center space-x-2">
                                    <span class="bg-pink-100 text-pink-800 text-xs px-2 py-1 rounded">Entertainment</span>
                                    <span class="bg-yellow-100 text-yellow-800 text-xs px-2 py-1 rounded">Awards</span>
                                </div>
                                <div class="flex items-center space-x-2">
                                    <span class="text-xs text-gray-500">Engagement Score: 9.2/10</span>
                                    <button class="bg-green-500 text-white px-3 py-1 rounded text-xs hover:bg-green-600">Create Post</button>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Content Creation Panel -->
        <div class="bg-white rounded-lg shadow">
            <div class="p-6 border-b border-gray-200">
                <h3 class="text-lg font-semibold text-gray-900">AI Content Creation Studio</h3>
                <p class="text-sm text-gray-500 mt-1">Generate original posts with images and captions</p>
            </div>
            
            <div class="p-6">
                <div class="bg-blue-50 rounded-lg p-4 mb-4">
                    <div class="flex items-center mb-3">
                        <i class="fas fa-robot text-blue-600 mr-2"></i>
                        <h4 class="font-semibold text-blue-900">Currently Creating:</h4>
                    </div>
                    <div class="space-y-3">
                        <div class="flex items-center justify-between bg-white rounded p-3">
                            <div>
                                <h5 class="font-medium text-gray-900">IT Park News Post</h5>
                                <p class="text-sm text-gray-600">Creating Instagram story + post with custom graphics</p>
                            </div>
                            <div class="flex items-center">
                                <div class="w-4 h-4 border-2 border-blue-600 border-t-transparent rounded-full animate-spin mr-2"></div>
                                <span class="text-sm text-blue-600">85% Complete</span>
                            </div>
                        </div>
                        
                        <div class="flex items-center justify-between bg-white rounded p-3">
                            <div>
                                <h5 class="font-medium text-gray-900">Metro Extension Update</h5>
                                <p class="text-sm text-gray-600">Generating Twitter/X thread with infographic</p>
                            </div>
                            <div class="flex items-center">
                                <span class="text-sm text-green-600 bg-green-100 px-2 py-1 rounded">Ready to Post</span>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                    <div class="text-center p-4 border-2 border-dashed border-gray-300 rounded-lg">
                        <i class="fas fa-image text-3xl text-gray-400 mb-2"></i>
                        <p class="text-sm font-medium text-gray-900">Instagram Posts</p>
                        <p class="text-xs text-gray-500">23 created today</p>
                    </div>
                    
                    <div class="text-center p-4 border-2 border-dashed border-gray-300 rounded-lg">
                        <i class="fab fa-twitter text-3xl text-gray-400 mb-2"></i>
                        <p class="text-sm font-medium text-gray-900">Twitter/X Threads</p>
                        <p class="text-xs text-gray-500">18 created today</p>
                    </div>
                    
                    <div class="text-center p-4 border-2 border-dashed border-gray-300 rounded-lg">
                        <i class="fab fa-youtube text-3xl text-gray-400 mb-2"></i>
                        <p class="text-sm font-medium text-gray-900">YouTube Shorts</p>
                        <p class="text-xs text-gray-500">7 created today</p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Scheduling & Analytics Section -->
    <div class="lg:col-span-1 space-y-6">
        <!-- Posting Schedule -->
        <div class="bg-white rounded-lg shadow">
            <div class="p-6 border-b border-gray-200">
                <h3 class="text-lg font-semibold text-gray-900">Posting Schedule</h3>
                <p class="text-sm text-gray-500">Next 24 hours</p>
            </div>
            
            <div class="p-6">
                <div class="space-y-4">
                    <div class="flex items-center justify-between p-3 bg-green-50 rounded-lg border border-green-200">
                        <div class="flex items-center">
                            <div class="w-2 h-2 bg-green-500 rounded-full mr-3"></div>
                            <div>
                                <p class="text-sm font-medium text-gray-900">2:45 PM - Today</p>
                                <p class="text-xs text-gray-600">Instagram + Twitter</p>
                            </div>
                        </div>
                        <i class="fab fa-instagram text-pink-500"></i>
                    </div>
                    
                    <div class="flex items-center justify-between p-3 bg-blue-50 rounded-lg border border-blue-200">
                        <div class="flex items-center">
                            <div class="w-2 h-2 bg-blue-500 rounded-full mr-3"></div>
                            <div>
                                <p class="text-sm font-medium text-gray-900">3:30 PM - Today</p>
                                <p class="text-xs text-gray-600">YouTube Short</p>
                            </div>
                        </div>
                        <i class="fab fa-youtube text-red-500"></i>
                    </div>
                    
                    <div class="flex items-center justify-between p-3 bg-gray-50 rounded-lg border border-gray-200">
                        <div class="flex items-center">
                            <div class="w-2 h-2 bg-gray-400 rounded-full mr-3"></div>
                            <div>
                                <p class="text-sm font-medium text-gray-900">4:15 PM - Today</p>
                                <p class="text-xs text-gray-600">All Platforms</p>
                            </div>
                        </div>
                        <i class="fas fa-share-alt text-gray-500"></i>
                    </div>
                </div>
                
                <div class="mt-4 p-3 bg-yellow-50 rounded-lg border border-yellow-200">
                    <div class="flex items-center">
                        <i class="fas fa-exclamation-triangle text-yellow-600 mr-2"></i>
                        <p class="text-sm text-yellow-800">Breaking news detected - Auto-posting in 5 minutes</p>
                    </div>
                </div>
            </div>
        </div>

        <!-- Platform Status -->
        <div class="bg-white rounded-lg shadow">
            <div class="p-6 border-b border-gray-200">
                <h3 class="text-lg font-semibold text-gray-900">Platform Status</h3>
            </div>
            
            <div class="p-6">
                <div class="space-y-4">
                    <div class="flex items-center justify-between">
                        <div class="flex items-center">
                            <i class="fab fa-instagram text-pink-500 mr-3"></i>
                            <span class="text-sm font-medium">Instagram</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-2 h-2 bg-green-500 rounded-full mr-2"></div>
                            <span class="text-xs text-green-600">Connected</span>
                        </div>
                    </div>
                    
                    <div class="flex items-center justify-between">
                        <div class="flex items-center">
                            <i class="fab fa-twitter text-blue-500 mr-3"></i>
                            <span class="text-sm font-medium">Twitter/X</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-2 h-2 bg-green-500 rounded-full mr-2"></div>
                            <span class="text-xs text-green-600">Connected</span>
                        </div>
                    </div>
                    
                    <div class="flex items-center justify-between">
                        <div class="flex items-center">
                            <i class="fab fa-youtube text-red-500 mr-3"></i>
                            <span class="text-sm font-medium">YouTube</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-2 h-2 bg-green-500 rounded-full mr-2"></div>
                            <span class="text-xs text-green-600">Connected</span>
                        </div>
                    </div>
                    
                    <div class="flex items-center justify-between">
                        <div class="flex items-center">
                            <i class="fas fa-globe text-purple-500 mr-3"></i>
                            <span class="text-sm font-medium">Website</span>
                        </div>
                        <div class="flex items-center">
                            <div class="w-2 h-2 bg-green-500 rounded-full mr-2"></div>
                            <span class="text-xs text-green-600">Active</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Quick Actions -->
        <div class="bg-white rounded-lg shadow">
            <div class="p-6 border-b border-gray-200">
                <h3 class="text-lg font-semibold text-gray-900">Quick Actions</h3>
            </div>
            
            <div class="p-6">
                <div class="space-y-3">
                    <button class="w-full bg-red-600 text-white py-2 px-4 rounded-lg hover:bg-red-700 transition-colors">
                        <i class="fas fa-bolt mr-2"></i>Post Breaking News
                    </button>
                    
                    <button class="w-full bg-blue-600 text-white py-2 px-4 rounded-lg hover:bg-blue-700 transition-colors">
                        <i class="fas fa-pause mr-2"></i>Pause Auto-Posting
                    </button>
                    
                    <button class="w-full bg-green-600 text-white py-2 px-4 rounded-lg hover:bg-green-700 transition-colors">
                        <i class="fas fa-chart-bar mr-2"></i>View Analytics
                    </button>
                    
                    <button class="w-full bg-purple-600 text-white py-2 px-4 rounded-lg hover:bg-purple-700 transition-colors">
                        <i class="fas fa-edit mr-2"></i>Custom Post
                    </button>
                </div>
            </div>
        </div>
    </div>
</div>

<!-- Analytics Dashboard -->
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
    <div class="bg-white rounded-lg shadow">
        <div class="p-6 border-b border-gray-200">
            <h2 class="text-xl font-semibold text-gray-900">Performance Analytics</h2>
            <p class="text-sm text-gray-500 mt-1">Last 7 days performance overview</p>
        </div>
        
        <div class="p-6">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                <!-- Engagement Chart -->
                <div>
                    <h3 class="text-lg font-medium text-gray-900 mb-4">Daily Engagement</h3>
                    <div style="height: 300px;">
                        <canvas id="engagementChart"></canvas>
                    </div>
                </div>
                
                <!-- Platform Distribution -->
                <div>
                    <h3 class="text-lg font-medium text-gray-900 mb-4">Platform Performance</h3>
                    <div style="height: 300px;">
                        <canvas id="platformChart"></canvas>
                    </div>
                </div>
            </div>
            
            <!-- Content Categories Performance -->
            <div class="mt-8">
                <h3 class="text-lg font-medium text-gray-900 mb-4">Top Performing Content Categories</h3>
                <div class="grid grid-cols-1 md:grid-cols-3 gap-4">
                    <div class="bg-gradient-to-r from-blue-500 to-blue-600 rounded-lg p-4 text-white">
                        <h4 class="font-semibold">Technology</h4>
                        <p class="text-2xl font-bold mt-2">8.9/10</p>
                        <p class="text-sm opacity-90">Average Engagement</p>
                    </div>
                    
                    <div class="bg-gradient-to-r from-green-500 to-green-600 rounded-lg p-4 text-white">
                        <h4 class="font-semibold">Breaking News</h4>
                        <p class="text-2xl font-bold mt-2">9.5/10</p>
                        <p class="text-sm opacity-90">Average Engagement</p>
                    </div>
                    
                    <div class="bg-gradient-to-r from-purple-500 to-purple-600 rounded-lg p-4 text-white">
                        <h4 class="font-semibold">Entertainment</h4>
                        <p class="text-2xl font-bold mt-2">7.8/10</p>
                        <p class="text-sm opacity-90">Average Engagement</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<!-- System Configuration -->
<div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-8">
    <div class="bg-white rounded-lg shadow">
        <div class="p-6 border-b border-gray-200">
            <h2 class="text-xl font-semibold text-gray-900">System Configuration</h2>
            <p class="text-sm text-gray-500 mt-1">Automation settings and content guidelines</p>
        </div>
        
        <div class="p-6">
            <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
                <!-- Monitoring Settings -->
                <div>
                    <h3 class="text-lg font-medium text-gray-900 mb-4">News Source Monitoring</h3>
                    <div class="space-y-3">
                        <div class="flex items-center justify-between p-3 border rounded-lg">
                            <div class="flex items-center">
                                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0IiBmaWxsPSIjRUY0NDQ0Ii8+CjxwYXRoIGQ9Ik0xMiA4VjE2TTggMTJIMTZNMjEgMTJBOSA5IDAgMTEzIDEyQTkgOSAwIDAxMjEgMTJaIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K" alt="Asianet" class="w-6 h-6 rounded mr-3">
                                <span class="font-medium">Asianet News</span>
                            </div>
                            <label class="relative inline-flex items-center cursor-pointer">
                                <input type="checkbox" checked class="sr-only peer">
                                <div class="w-11 h-6 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-blue-600"></div>
                            </label>
                        </div>
                        
                        <div class="flex items-center justify-between p-3 border rounded-lg">
                            <div class="flex items-center">
                                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0IiBmaWxsPSIjMzMzM0ZGIi8+CjxwYXRoIGQ9Ik0xMiA4VjE2TTggMTJIMTZNMjEgMTJBOSA5IDAgMTEzIDEyQTkgOSAwIDAxMjEgMTJaIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K" alt="Manorama" class="w-6 h-6 rounded mr-3">
                                <span class="font-medium">Manorama News</span>
                            </div>
                            <label class="relative inline-flex items-center cursor-pointer">
                                <input type="checkbox" checked class="sr-only peer">
                                <div class="w-11 h-6 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-blue-600"></div>
                            </label>
                        </div>
                        
                        <div class="flex items-center justify-between p-3 border rounded-lg">
                            <div class="flex items-center">
                                <img src="data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHJlY3Qgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0IiBmaWxsPSIjRkY2NjAwIi8+CjxwYXRoIGQ9Ik0xMiA4VjE2TTggMTJIMTZNMjEgMTJBOSA5IDAgMTEzIDEyQTkgOSAwIDAxMjEgMTJaIiBzdHJva2U9IndoaXRlIiBzdHJva2Utd2lkdGg9IjIiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIvPgo8L3N2Zz4K" alt="24 News" class="w-6 h-6 rounded mr-3">
                                <span class="font-medium">24 News</span>
                            </div>
                            <label class="relative inline-flex items-center cursor-pointer">
                                <input type="checkbox" checked class="sr-only peer">
                                <div class="w-11 h-6 bg-gray-200 peer-focus:outline-none peer-focus:ring-4 peer-focus:ring-blue-300 rounded-full peer peer-checked:after:translate-x-full peer-checked:after:border-white after:content-[''] after:absolute after:top-[2px] after:left-[2px] after:bg-white after:border-gray-300 after:border after:rounded-full after:h-5 after:w-5 after:transition-all peer-checked:bg-blue-600"></div>
                            </label>
                        </div>
                    </div>
                    
                    <div class="mt-6">
                        <h4 class="font-medium text-gray-900 mb-3">Posting Frequency</h4>
                        <div class="space-y-3">
                            <div class="flex items-center justify-between">
                                <span class="text-sm text-gray-600">Posts per hour (Normal)</span>
                                <div class="flex items-center space-x-2">
                                    <input type="range" min="1" max="10" value="3" class="w-24">
                                    <span class="text-sm font-medium w-8 text-center">3</span>
                                </div>
                            </div>
                            
                            <div class="flex items-center justify-between">
                                <span class="text-sm text-gray-600">Posts per hour (Breaking News)</span>
                                <div class="flex items-center space-x-2">
                                    <input type="range" min="1" max="10" value="7" class="w-24">
                                    <span class="text-sm font-medium w-8 text-center">7</span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                
                <!-- Content Guidelines -->
                <div>
                    <h3 class="text-lg font-medium text-gray-900 mb-4">Content Guidelines</h3>
                    <div class="space-y-4">
                        <div class="border rounded-lg p-4">
                            <h4 class="font-medium text-gray-900 mb-2">Safety Filters</h4>
                            <div class="space-y-2">
                                <div class="flex items-center">
                                    <input type="checkbox" checked class="mr-2">
                                    <span class="text-sm">Avoid sensitive political content</span>
                                </div>
                                <div class="flex items-center">
                                    <input type="checkbox" checked class="mr-2">
                                    <span class="text-sm">Skip unverified information</span>
                                </div>
                                <div class="flex items-center">
                                    <input type="checkbox" checked class="mr-2">
                                    <span class="text-sm">Content moderation enabled</span>
                                </div>
                                <div class="flex items-center">
                                    <input type="checkbox" checked class="mr-2">
                                    <span class="text-sm">Fact-check integration</span>
                                </div>
                            </div>
                        </div>
                        
                        <div class="border rounded-lg p-4">
                            <h4 class="font-medium text-gray-900 mb-2">Hashtag Strategy</h4>
                            <div class="space-y-2">
                                <div class="flex items-center justify-between">
                                    <span class="text-sm text-gray-600">Malayalam hashtags</span>
                                    <span class="text-sm font-medium">70%</span>
                                </div>
                                <div class="flex items-center justify-between">
                                    <span class="text-sm text-gray-600">English hashtags</span>
                                    <span class="text-sm font-medium">30%</span>
                                </div>
                                <div class="mt-2">
                                    <input type="text" placeholder="Custom hashtags (comma separated)" class="w-full p-2 border rounded-lg text-sm" value="#kerala #malayalam #news #breaking">
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</div>

<!-- Footer -->
<footer class="bg-gray-800 text-white py-8 mt-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
            <div>
                <h3 class="text-lg font-semibold mb-4">Malayalam News Automation</h3>
                <p class="text-gray-300 text-sm">Powered by AI technology for seamless news content creation and distribution across multiple platforms.</p>
            </div>
            
            <div>
                <h4 class="font-medium mb-4">Features</h4>
                <ul class="space-y-2 text-sm text-gray-300">
                    <li>• Real-time news monitoring</li>
                    <li>• AI-powered content creation</li>
                    <li>• Multi-platform posting</li>
                    <li>• Engagement optimization</li>
                    <li>• Legal compliance checks</li>
                </ul>
            </div>
            
            <div>
                <h4 class="font-medium mb-4">System Status</h4>
                <div class="space-y-2 text-sm">
                    <div class="flex items-center text-green-300">
                        <div class="w-2 h-2 bg-green-500 rounded-full mr-2"></div>
                        <span>All systems operational</span>
                    </div>
                    <div class="flex items-center text-blue-300">
                        <div class="w-2 h-2 bg-blue-500 rounded-full mr-2"></div>
                        <span>6 news sources active</span>
                    </div>
                    <div class="flex items-center text-purple-300">
                        <div class="w-2 h-2 bg-purple-500 rounded-full mr-2"></div>
                        <span>4 platforms connected</span>
                    </div>
                </div>
            </div>
        </div>
        
        <div class="border-t border-gray-700 mt-8 pt-8 text-center">
            <p class="text-gray-400 text-sm">© 2024 Malayalam News Automation System. All rights reserved.</p>
        </div>
    </div>
</footer>

<script>
// Initialize Charts
document.addEventListener('DOMContentLoaded', function() {
    // Engagement Chart
    const engagementCtx = document.getElementById('engagementChart').getContext('2d');
    new Chart(engagementCtx, {
        type: 'line',
        data: {
            labels: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun'],
            datasets: [{
                label: 'Total Engagement',
                data: [1200, 1900, 1500, 2200, 2800, 3100, 2400],
                borderColor: 'rgb(59, 130, 246)',
                backgroundColor: 'rgba(59, 130, 246, 0.1)',
                tension: 0.4
            }, {
                label: 'Posts Created',
                data: [45, 68, 52, 78, 89, 95, 72],
                borderColor: 'rgb(16, 185, 129)',
                backgroundColor: 'rgba(16, 185, 129, 0.1)',
                tension: 0.4
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    position: 'bottom'
                }
            },
            scales: {
                y: {
                    beginAtZero: true
                }
            }
        }
    });

    // Platform Performance Chart
    const platformCtx = document.getElementById('platformChart').getContext('2d');
    new Chart(platformCtx, {
        type: 'doughnut',
        data: {
            labels: ['Instagram', 'Twitter/X', 'YouTube', 'Website'],
            datasets: [{
                data: [35, 25, 20, 20],
                backgroundColor: [
                    'rgb(236, 72, 153)',
                    'rgb(29, 161, 242)',
                    'rgb(255, 0, 0)',
                    'rgb(107, 114, 128)'
                ]
            }]
        },
        options: {
            responsive: true,
            maintainAspectRatio: false,
            plugins: {
                legend: {
                    position: 'bottom'
                }
            }
        }
    });

    // Auto-refresh simulation
    setInterval(function() {
        // Simulate live updates
        const statusElements = document.querySelectorAll('.status-indicator');
        statusElements.forEach(el => {
            el.style.animationDuration = Math.random() * 2 + 1 + 's';
        });
    }, 5000);

    // Simulate news updates
    const newsContainer = document.querySelector('.space-y-4');
    setInterval(function() {
        const timeElements = document.querySelectorAll('.text-xs.text-gray-500');
        timeElements.forEach(el => {
            if (el.textContent.includes('min ago')) {
                let minutes = parseInt(el.textContent) + 1;
                el.textContent = minutes + ' min ago';
            }
        });
    }, 60000);
});
</script>

</body>
</html>
