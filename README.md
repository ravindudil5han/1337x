# 1337x Torrent Search

[![npm version](https://img.shields.io/npm/v/@dil5han/1337x)](https://www.npmjs.com/package/@dil5han/1337x)
[![License](https://img.shields.io/github/license/dil5han/1337x)](LICENSE)

A Node.js library for scraping torrent data from 1337x.to.

## Installation

You can install the `1337x` library via npm:

```bash
npm install @dil5han/1337x
```

## Usage

```javascript
const t1337x = require('@dil5han/1337x');

t1337x('search', 'pages') // t1337x('cars', '1') Replace the word "cars" with the word you want to search
    .then((data) => {
        if (data === null) {
            console.log('Error: Failed to fetch data from 1337x.');

        } else if (data.length === 0) {
            console.log('No search results .');

        } else {
            console.log(data);
        }
    })
    .catch((error) => {
        console.log('Error:', error);
    });
```

## API

### t1337x(search, page)

Performs a search on 1337x.to with the given query and returns an array of torrent objects.

- `search` (string): The search query.
- `page` (string, optional): The page number to retrieve. Defaults to '1'.

Returns: `Promise<Array<Object>>`

Each torrent object in the returned array has the following properties:

- `Name` (string): The name of the torrent.
- `img` (string): The URL of the torrent's image.
- `site_url` (string): The URL of the torrent on 1337x.to.
- `Category` (string): The category of the torrent.
- `Type` (string): The type of the torrent.
- `Language` (string): The language of the torrent.
- `Size` (string): The size of the torrent.
- `Uploaded_By` (string): The uploader of the torrent.
- `Downloads` (string): The number of downloads.
- `Last_checked` (string): The last time the torrent was checked.
- `Date_uploaded` (string): The date the torrent was uploaded.
- `Seeds` (string): The number of seeders.
- `Leechs` (string): The number of leechers.
- `Mag_torrent_url` (string): The magnet URL of the torrent.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please refer to the [Contributing Guidelines](CONTRIBUTING.md) for more details.

## Issues

If you encounter any issues or have suggestions, please [open an issue](https://github.com/dil5han/1337x/issues).

## Credits

This library is developed and maintained by Dilshan.

## Disclaimer

This library is intended for educational and personal use only. Please respect the legal rights of content creators and use torrents responsibly.
