# YTLinkView - YouTube Video Customizer

A web application that allows users to create customized YouTube video pages with personal messages above and below the video, with permanent sharing capabilities.

## Features

- 📺 **YouTube Video Integration**: Paste any YouTube URL and embed it
- ✏️ **Custom Text**: Add personalized messages above and below videos
- 👀 **Preview Mode**: View your customized video in a new tab
- 🔗 **Permanent Share Links**: Generate shareable links that work forever without sign-in
- 🎵 **Full Volume Playback**: Videos play with full audio (no muting)
- 📱 **Responsive Design**: Works on all devices
- 🎬 **Auto-play**: Videos start playing automatically in preview mode
- 🚀 **No Database Required**: Everything works through URL parameters
- 🔒 **Code Protection**: Obfuscated and domain-locked for security

## File Structure

```
ytlinkview/
├── index.html          # Homepage - main input form (obfuscated)
├── preview.html        # Preview page - displays customized video (obfuscated)
└── README.md          # This file
```

## Setup Instructions

### 1. Download Files

Save the following files in the same directory:

- **index.html** - The main homepage
- **preview.html** - The video preview page  

### 2. Local Development

**Important**: This application is domain-locked to Vercel. For development purposes, contact the developer for access to unobfuscated code.

### 3. Deployment

This application is designed for **Vercel deployment only**:

1. **Upload to Vercel**: Deploy both HTML files to your Vercel project
2. **Access via Vercel Domain**: Application will work on `*.vercel.app` domains
3. **Domain Lock**: Code will not execute on other hosting platforms

## How to Use

### Creating a Custom Video

1. **Start on Homepage**: Open `index.html` in your browser
2. **Add YouTube URL**: Paste any YouTube video URL in the input field
3. **Add Custom Text**: 
   - Enter text for above the video (optional)
   - Enter text for below the video (optional)
4. **Preview**: Click "Preview Video" button
   - Opens in a new tab
   - Video starts playing automatically with full volume
   - Shows your custom text

### Sharing Your Custom Video

1. **In Preview Mode**: Click the "Get Share Link" button
2. **Instant Link Generation**: No sign-in required - link generates immediately
3. **Copy & Share**: Copy the link and share it with anyone
4. **Permanent Links**: Links work forever and from any device

### How Sharing Works

The sharing system is completely **stateless** and requires no database:

- All customization data (video ID, custom text) is encoded directly in the URL
- Share links are permanent and work from any device
- No user accounts, databases, or server storage needed
- Links look like: `preview.html?videoId=ABC123&topText=Hello&bottomText=World`

### Features in Detail

#### Homepage (`index.html`)
- Clean, modern interface
- YouTube URL validation
- Custom text input areas
- Preview button that opens new tab

#### Preview Page (`preview.html`)
- Displays video with custom text
- Auto-plays video with **full volume** (no muting)
- Instant share link generation
- Copy-to-clipboard functionality with visual feedback
- Responsive design for all screen sizes
- Permanent, shareable URLs

## Technical Details

### YouTube Integration
- Extracts video ID from YouTube URLs
- Supports various YouTube URL formats:
  - `https://www.youtube.com/watch?v=VIDEO_ID`
  - `https://youtu.be/VIDEO_ID`
  - `https://www.youtube.com/embed/VIDEO_ID`

### Sharing System
- **URL-based storage**: All data stored in URL parameters
- **No backend required**: Completely client-side application
- **Permanent links**: URLs work indefinitely without expiration
- **Cross-device compatibility**: Links work on any device with internet
- **No authentication**: Share immediately without sign-in

### Audio Playback
- Videos play with **full volume** by default
- Removed mute parameter from YouTube embed
- Complies with browser autoplay policies where possible

## Code Protection

### Security Features
- **Code Obfuscation**: JavaScript code is obfuscated to protect intellectual property
- **Domain Lock**: Application only runs on authorized domains (*.vercel.app)
- **Anti-tampering**: Self-defending code with debug protection
- **Console Protection**: Developer tools access is restricted
- **String Encoding**: All strings are encoded to prevent easy modification
- **Control Flow Flattening**: Code logic is restructured to prevent analysis

### Development vs Production
- **Production Version**: Uses obfuscated, protected code
- **Development**: Original unobfuscated code kept separately for maintenance
- **Domain Restriction**: Code only executes on Vercel domains
- **Unauthorized Access**: Code will not function on non-authorized domains

## Browser Compatibility

- **Chrome**: Full support
- **Firefox**: Full support
- **Safari**: Full support (may require user interaction for autoplay)
- **Edge**: Full support

**Note**: Application only works when accessed through authorized Vercel domains.

## Advantages of This Approach

### No Sign-in Required
- **Instant sharing**: Generate links immediately
- **No user management**: No accounts or passwords needed
- **Privacy-friendly**: No personal data collection
- **Simple workflow**: Create → Preview → Share

### Permanent Links
- **No expiration**: Links work forever
- **No server dependency**: No database downtime concerns
- **Lightweight**: Minimal server resources required
- **Portable**: Easy to host on Vercel

### Code Security
- **IP Protection**: Obfuscated code protects intellectual property
- **Domain Control**: Prevents unauthorized hosting
- **Anti-reverse Engineering**: Multiple layers of code protection

## Limitations & Notes

### Current Implementation
- **URL length limits**: Very long custom text may hit browser URL limits
- **No edit history**: Can't modify shared links after creation
- **No analytics**: No tracking of link usage or views
- **Domain Restricted**: Only works on authorized Vercel domains
- **Code Protected**: Obfuscated code makes customization more difficult

### For Production Use
To enhance this for production, you could optionally add:

1. **URL Shortening**: Create shorter, more user-friendly links
2. **Analytics**: Track link clicks and usage statistics
3. **Link Management**: Allow users to edit or delete their links
4. **Custom Domains**: Use branded short domains
5. **Enhanced Security**: Additional input sanitization and validation

## Customization

### Styling
- All CSS is embedded in HTML files
- Uses CSS Grid and Flexbox for responsive design
- Custom color scheme with gradient backgrounds
- Smooth animations and transitions

### Functionality
- **Limited Customization**: Due to code obfuscation, modifications require access to source code
- **Contact Developer**: For customization requests or feature additions
- **Protected Code**: Direct modification of obfuscated code is not recommended

## Troubleshooting

### Common Issues

1. **Video Not Loading**
   - Check if YouTube URL is valid
   - Ensure video is not private or restricted
   - Try different video URL

2. **Share Links Not Working**
   - Ensure accessing via Vercel domain
   - Check that all files are properly deployed
   - Verify URL parameters are properly encoded

3. **Copy to Clipboard Not Working**
   - Try using a different browser
   - Ensure page is served over HTTPS
   - Manual copy-paste is always available

4. **Code Not Working on Other Domains**
   - Application is domain-locked to Vercel
   - Will not function on localhost or other hosting platforms
   - Contact developer for authorized domain additions

5. **Console Errors or Blank Pages**
   - Code includes debug protection
   - Developer tools may be restricted
   - This is normal behavior for protected code

### Browser Console Errors
- Console access may be limited due to protection features
- Debug protection may clear console output
- This is intentional behavior for code security

## Deployment

### Vercel Deployment (Recommended)
This application is optimized for Vercel deployment:

1. **Upload Files**: Deploy both HTML files to Vercel
2. **Automatic Domain**: Works with your-app.vercel.app domain
3. **Instant Deployment**: No server configuration needed
4. **Protected Code**: Obfuscated code provides security

### Domain Requirements
- **Authorized Domains**: *.vercel.app only
- **No Other Hosting**: Will not work on other platforms
- **Contact Developer**: For additional domain authorization

## Development

### Code Maintenance
- Original source code is kept separately for development
- Production version uses obfuscated code for protection
- Changes require re-obfuscation before deployment
- Development environment uses unobfuscated code

### Domain Authorization
- Currently authorized for: *.vercel.app domains
- Contact developer for additional domain authorization
- Unauthorized domains will show blank pages or errors

## Support

For issues, customization requests, or questions:
1. Check that you're accessing via a Vercel domain
2. Verify all files are properly deployed
3. Contact developer for technical support or feature requests
4. For code modifications, source code access may be required

## License

© 2025 Drishti Madaan. All rights reserved.

**Important**: This code is protected by obfuscation and domain locks. Unauthorized copying, redistribution, reverse engineering, or hosting on non-authorized domains is prohibited. The application is designed exclusively for Vercel deployment.

**Contact**: For licensing inquiries, custom deployments, or source code access, please contact the developer.
