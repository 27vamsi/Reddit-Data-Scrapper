# 🚀 Reddit Data Scraper Pro

<div align="center">


*Secure, fast Reddit data collection toolkit* ⚡

</div>

## ✨ Features

- 🔐 **Secure** - No hardcoded credentials, safe input prompts
- ⚡ **Fast** - Async processing with concurrent downloads
- 📊 **Complete** - Posts, comments, images, and metadata
- 🛠️ **Configurable** - Customizable delays, limits, and batch sizes
- 📁 **Organized** - Clean file structure and compressed exports

## 🚀 Quick Start

### Install & Setup
```bash
pip install praw asyncpraw aiohttp aiofiles pillow tqdm nest_asyncio
```

### Choose Your Mode

**📝 Basic Scraper** (Text Only)
```bash
python reddit_basic_scraper.py
# Perfect for: Comments, posts, quick analysis
```

**🚀 Async Scraper** (Images + Text)
```bash
python reddit_async_scraper.py
# Perfect for: Computer vision, large datasets
```

## 📦 Output Format

### Basic Scraper
```json
{
  "post_id": "abc123",
  "title": "Amazing discussion topic",
  "score": 1247,
  "url": "https://reddit.com/r/example/comments/abc123/",
  "created_utc": 1640995200,
  "num_comments": 45,
  "selftext": "Post content here...",
  "image_url": "https://i.redd.it/example.jpg"
}
```

### Async Scraper  
```json
{
  "post_id": "abc123",
  "title": "Amazing discussion topic", 
  "score": 1247,
  "created_utc": 1640995200,
  "images": [
    {
      "local_path": "reddit_data/images/abc123_0.jpg",
      "original_url": "https://i.redd.it/example.jpg",
      "file_size": 2048576,
      "format": "JPEG"
    }
  ],
  "comments": [
    {
      "comment_id": "def456",
      "body": "Great post!",
      "score": 23,
      "created_utc": 1640995300
    }
  ]
}
```

### File Structure
```
reddit_data_subreddit/
├── 📁 images/           # Downloaded images (async only)
├── 📁 processed_data/   # JSON datasets  
├── 📄 posts.csv         # CSV format (basic only)
├── 📄 comments.csv      # CSV format (basic only)
└── 📦 archive.tar.gz    # Compressed bundle
```

## ⚙️ Configuration

| Setting | Description | Default |
|---------|-------------|---------|
| Post limit | Number of posts | User input |
| Delay | Request spacing | 1.0s |
| Batch size | Concurrent processing | 10 |
| File size limit | Max image size | 10MB |

## 🎯 Use Cases

- 🔬 **Research** - Social media analysis
- 🤖 **ML Datasets** - Computer vision training data  
- 📊 **Analytics** - Trend monitoring
- 🎨 **Content** - Image curation

## 🛡️ Best Practices

✅ Start small (10-50 posts) for testing  
✅ Use 1-2 second delays  
✅ Keep API credentials secure  
❌ Don't go below 0.5s delay  
❌ Don't share credentials publicly  

## 📊 Performance

- **Basic**: 100 posts in ~2 minutes
- **Async**: 100 posts + images in ~3 minutes  
- **Memory**: <500MB for 1000 posts
- **Compression**: ~60% size reduction

---

**🌟 Star if this helped you!** • **🐛 Report issues** • **💡 Suggest features**
