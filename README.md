# 3nt.lat

A minimalist, single-file web application for benchmarking browser-to-server latency and local CPU performance.

## Features

- **Latency Tester**: Measure round-trip time to multiple popular sites using `fetch`.
- **Customizable**: Add your own URLs, remove sites, or reset to the default list.
- **CPU Speed Test**: Benchmark local execution speed via a prime number calculation (1M primes).
- **Persistent State**: Site list and theme preference are stored in `localStorage`.
- **UI/UX**:
  - Ultra-compact, minimalist design.
  - Light and Dark mode support.
  - Color-coded results (Green/Orange/Red) based on performance.
  - Responsive two-column grid layout.

## How to Run

Since this is a single-file static HTML application, you can run it in any modern browser:

### Option 1: Local File
Simply open `index.html` directly in your browser.

### Option 2: Local Server (Recommended)
To avoid potential CORS issues with some sites and ensure full functionality, serve it via a local web server:

```bash
# Using Python
python3 -m http.server 8000

# Using Node.js (if 'serve' is installed)
npx serve .
```

Then visit `http://localhost:8000`.

## Technical Details

- **Tech Stack**: Vanilla HTML5, CSS3, and JavaScript.
- **Latency Method**: Uses `fetch` with `mode: 'no-cors'` to bypass most CORS restrictions for simple connectivity testing.
- **CPU Benchmark**: Synchronous prime number generation up to 1,000,000.
