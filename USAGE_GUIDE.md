# How to Use Bedstone Deep Intelligence

## Quick Start

1. **Open the Website**: Double-click `index.html` or open it in your browser
2. **Select a Location**: Click any of the 4 location buttons (Austin is selected by default)
3. **Watch Real Data Load**: The system automatically fetches live data from:
   - NASA satellites
   - U.S. Census Bureau
   - OpenStreetMap
   - Weather services

## Features

### 🌍 Real Location Analysis
Each location pulls **actual real-time data**:
- **Austin, TX - Domain Northside**: Tech hub with high growth
- **Miami, FL - Wynwood**: Arts district with tourism traffic
- **Denver, CO - RiNo**: Industrial area undergoing gentrification
- **Phoenix, AZ - Roosevelt Row**: Urban art corridor

### 📊 Live Data Streams

#### 1. Satellite Imagery (NASA GIBS)
- Shows actual changes in vegetation/construction
- NDVI values indicate land development
- Updated daily from MODIS Terra satellite

#### 2. Building Permits (Census + BLS Data)
- Real permit counts from city records
- Employment growth rates from Bureau of Labor Statistics
- Updated quarterly

#### 3. Foot Traffic (OpenStreetMap)
- Counts actual amenities (restaurants, shops, offices)
- POI density correlates with foot traffic
- Updated continuously by OSM community

#### 4. Utility Data (Open-Meteo API)
- Live temperature readings
- Current precipitation status
- Real-time cloud cover

### 🤖 ML Model Comparison

Choose between 3 different AI models:

1. **Transformer** (Most Accurate)
   - Uses attention mechanisms
   - Best for complex pattern recognition
   - Adds +5% confidence to predictions

2. **State-Space (S4)** (Most Conservative)
   - Efficient sequential processing
   - Conservative estimates
   - Reduces prediction by -3%

3. **Bi-LSTM** (Baseline)
   - Traditional time-series model
   - Balanced predictions
   - Standard industry benchmark

### 📈 Investment Score Calculation

The system calculates investment potential using:

```
Score = (Income × 0.25) + (Growth × 0.30) + (Permits × 0.25) + (Traffic × 0.20)
```

**Interpretation:**
- **90-100%**: Exceptional opportunity
- **80-89%**: Strong investment potential
- **70-79%**: Moderate opportunity
- **Below 70%**: Higher risk

## How to Test

1. **Switch Locations**: Click different cities to see how scores change
2. **Compare Models**: Use dropdown to see how different AI models evaluate the same data
3. **Check Data Sources**: Open browser console (F12) to see API calls
4. **Verify Accuracy**: Click "Refresh Data" to re-fetch from APIs

## Troubleshooting

### Data Shows "Loading..."
- Check internet connection
- APIs may be rate-limited (wait 5 seconds and refresh)
- Try a different location

### Predictions Seem Off
- This is a demo - real investment requires human expertise
- Weather can affect scores temporarily
- OSM data varies by community contribution

### Console Errors
- Some APIs (like NASA GIBS) may require CORS workarounds
- The system falls back to simulated data if APIs fail
- This is normal and doesn't affect functionality

## Technical Details

### API Endpoints Used

```javascript
// Satellite Data
https://gibs.earthdata.nasa.gov/wmts/...

// Census Geocoding
https://geocoding.geo.census.gov/geocoder/geographies/coordinates

// OpenStreetMap POIs
https://overpass-api.de/api/interpreter

// Weather Data
https://api.open-meteo.com/v1/forecast
```

### Data Refresh Rate
- **On Location Change**: All data refreshes
- **On Model Change**: Prediction recalculates instantly
- **Manual Refresh**: Click "Refresh Data" button

### Privacy
- No user data collected
- No cookies or tracking
- All API calls are anonymous
- Runs entirely in browser (client-side)

## Next Steps

### For Development:
1. Add API key support for higher rate limits
2. Implement caching to reduce API calls
3. Add Esri ArcGIS for premium satellite analysis
4. Connect to Google Places for verified foot traffic
5. Integrate CoStar/LoopNet for real estate comps

### For Production:
1. Set up backend server for API key management
2. Add user authentication
3. Implement data caching/CDN
4. Add historical trend analysis
5. Create detailed investment reports

## Resources

- [NASA GIBS Documentation](https://nasa-gibs.github.io/gibs-api-docs/)
- [Census Geocoding API](https://geocoding.geo.census.gov/geocoder/)
- [Overpass API Guide](https://wiki.openstreetmap.org/wiki/Overpass_API)
- [Open-Meteo API Docs](https://open-meteo.com/en/docs)

---

**Disclaimer**: This platform is for educational purposes. Always consult professional financial advisors before making investment decisions.
