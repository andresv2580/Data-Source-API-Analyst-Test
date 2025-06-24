# Data-Source-API-Analyst-Test
Homework assignment for Data Source API Analyst role.
## Objective
This repository contains my solution for the Data Source API Analyst technical assignment, demonstrating proficiency in working with the GitHub API, handling authentication, pagination, rate limits, and error management.

## Structure
- `/API_Analyst_Test.ipynb`: Documentation and Python code



## Implementation Details

### API Endpoints Tested
1. **Repository Search**: `/search/repositories`
2. **Commit History**: `/repos/{owner}/{repo}/commits`
3. **Repository Contents**: `/repos/{owner}/{repo}/contents/{path}`

### Key Features Implemented
- ✅ OAuth2 authentication with personal access tokens
- ✅ Comprehensive error handling (401, 403, 404, 500)
- ✅ Rate limit detection and automatic retry
- ✅ Pagination handling for large datasets
- ✅ Response validation and data cleaning

## Setup Instructions

### Prerequisites
- Python 3.8+
- GitHub Personal Access Token (with `repo` scope)
- Google Colab (for testing)

### How to Run
1. **For Google Colab**:
   - Open `API_Analyst_test.ipynb` in Colab
   - Replace `"your_token_here"` with your GitHub token
   - Execute cells sequentially

## Technical Approach
1. **Authentication**: Implemented via Bearer tokens in headers
2. **Rate Limiting**: 
   - Automatic detection using `/rate_limit` endpoint
   - Queue-based request throttling
3. **Error Handling**:
   - Exponential backoff for 403/429 errors
   - User-friendly error messages
4. **Pagination**: 
   - Link header parsing
   - Automatic page traversal

## Findings and Observations
- The GitHub API provides excellent documentation but has strict rate limits
- Pagination is essential for complete data extraction
- Error responses contain helpful diagnostic information
- The v3 API media type (`application/vnd.github.v3+json`) is required for consistent responses

## Troubleshooting

- 401 Unauthorized errors
- 403 Forbidden (rate limit exceeded)
- 404 Not Found (resource issues)

## Future Improvements
- Implement caching for frequent requests
- Add async request handling
- Create a Dockerized version for easy deployment
- Build a dashboard for API monitoring

## Author
[Andres Vasquez] 
[andresvasquez2580@gmail.com]  
[https://github.com/andresv2580/Data-Source-API-Analyst-Test.git]
