# IcecreamPunks

A fun and interactive React web application that lets users create custom ice cream punk characters using layered image composition. Mix and match different character elements like hair, clothing, accessories, and backgrounds to create unique punk-style avatars with an ice cream theme.

## Features

- **Character Creator**: Build custom characters by selecting from various image layers
- **Canvas-based Image Composition**: Real-time layered image rendering using HTML5 Canvas
- **Download Functionality**: Save your creations as PNG images
- **Social Sharing**: Share your punk characters using the Web Share API
- **Twitter Integration**: View recent tweets from influencers (requires backend API)
- **Responsive Design**: Works on both desktop and mobile devices
- **Modern UI**: Clean interface with neon-glow styling effects

## Screenshots

*Note: Add screenshots here showing the character creator interface, example creations, and the Twitter feed section.*

## Getting Started

### Prerequisites

- Node.js (version 14 or higher)
- npm or yarn package manager

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/icecreampunks.git
cd icecreampunks
```

2. Install dependencies:
```bash
npm install
```

3. (Optional) Set up environment variables for Twitter functionality:
```bash
cp .env.example .env
# Edit .env and add your Twitter API endpoint
REACT_APP_TWEET_FETCH_URL=your_twitter_api_endpoint
```

### Running the Application

Start the development server:
```bash
npm start
```

The application will open in your browser at `http://localhost:3000`.

### Building for Production

Create a production build:
```bash
npm run build
```

The build files will be created in the `build/` directory.

## Usage

### Creating Characters

1. Navigate to the **Ice Cream** section
2. Select different character elements from the checkbox list:
   - **Background**: Choose scene backgrounds
   - **Body**: Select base character bodies
   - **Clothing**: Pick different outfits and styles
   - **Hair**: Choose various hairstyles
   - **Eyes**: Select eye types
   - **Accessories**: Add ice cream cones and other props
3. Watch your character update in real-time on the canvas
4. Click **Download** to save your creation as a PNG image
5. Use the **Share** button to share via social media (on supported devices)

### Viewing Tweets

1. Navigate to the **Tweets** section
2. Click **Pull Data** to fetch recent tweets from influencers
3. Browse through the curated content

## Project Structure

```
src/
├── components/
│   ├── button/              # Reusable button component
│   ├── check-item/          # Checkbox items for character elements
│   ├── header/              # Application header
│   ├── home/                # Home page component
│   ├── icecream/            # Main character creator
│   ├── image/               # Image rendering components
│   ├── layer/               # Layer management
│   └── tweet/               # Twitter feed components
├── localData/
│   └── imageData.json       # Character element image URLs and metadata
├── services/
│   └── twitter/             # Twitter API integration
└── App.js                   # Main application component
```

## Testing

Run the test suite:
```bash
npm test
```

Run tests in watch mode during development:
```bash
npm test -- --watch
```

### Manual Testing

1. **Character Creator Testing**:
   - Test selecting different combinations of character elements
   - Verify layering order (background should be behind, accessories in front)
   - Test download functionality
   - Test share functionality on mobile devices

2. **Responsiveness Testing**:
   - Test on different screen sizes
   - Verify mobile layout adjustments
   - Check canvas scaling on smaller screens

3. **Cross-browser Testing**:
   - Test in Chrome, Firefox, Safari, and Edge
   - Verify Canvas API compatibility
   - Test Web Share API fallback behavior

## Technologies Used

- **React** (v17.0.2) - Frontend framework
- **React Router DOM** - Client-side routing
- **React Bootstrap** - UI components
- **HTML5 Canvas** - Image composition
- **Bootstrap** (v5.1.0) - CSS framework
- **Font Awesome** - Icons
- **Web Share API** - Social sharing functionality

## API Dependencies

The Twitter functionality requires a backend API endpoint that provides tweet data in the following format:
```json
{
  "data": [...], // Tweet objects
  "includes": {
    "users": [...] // User data for tweet authors
  }
}
```

## Contributing

1. Fork the repository
2. Create a feature branch: `git checkout -b feature-name`
3. Commit your changes: `git commit -am 'Add new feature'`
4. Push to the branch: `git push origin feature-name`
5. Submit a pull request

## Deployment

### GitHub Pages

This project is configured for GitHub Pages deployment:
```bash
npm run deploy
```

### Other Platforms

The built files can be deployed to any static hosting service like Netlify, Vercel, or AWS S3.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Character images are hosted on Cloudinary
- Font: Comic Neue from Google Fonts
- Icons: Font Awesome
- UI Framework: Bootstrap

## Contact

- Project Link: [https://github.com/yourusername/icecreampunks](https://github.com/yourusername/icecreampunks)
- Live Demo: [https://yourusername.github.io/icecreampunks](https://yourusername.github.io/icecreampunks)
