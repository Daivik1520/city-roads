# city-roads

Render every single road in any city at once.

![demo](https://i.imgur.com/6bFhX3e.png)

## Overview

This project is a high-performance visualization tool that renders every single road within a selected city. By leveraging WebGL and efficient data structures, it allows users to explore urban infrastructure on a massive scale, from small towns to megacities like Tokyo or Seattle.

Developed by **DAIVIK REDDY**, this tool demonstrates the power of modern web technologies in handling large-scale geospatial data.

## Modular Design

The architecture of `city-roads` is built with modularity and extensibility as core principles. The codebase is organized into distinct, loosely coupled components, making it easy to:

*   **Extend Functionality**: Add new features or data layers without disrupting existing logic.
*   **Replace Modules**: Swap out rendering engines, data fetchers, or UI components with minimal refactoring.
*   **Maintain Code**: Clear separation of concerns ensures that the codebase remains clean, readable, and easy to debug.

Whether you are looking to integrate new data sources or customize the rendering pipeline, the modular design provides a robust foundation for future development.

## How It Works

The data is fetched from OpenStreetMap using the [Overpass API](http://overpass-turbo.eu/). While powerful, fetching thousands of roads for a large area can be resource-intensive. To optimize performance:

1.  **Caching**: Common queries are cached to reduce load times and API strain.
2.  **Efficient Storage**: Data is stored in a compact protobuf format to minimize bandwidth usage.
3.  **Smart Resolution**: City name resolution is handled by [Nominatim](https://nominatim.openstreetmap.org/), with intelligent fallback mechanisms.

## Scripting & API

Beyond the visual interface, `city-roads` offers a powerful scripting API for developers. You can programmatically interact with the scene, load additional data, or automate visualizations.

The Scene API is fully documented here: [API.md](./API.md)

## Limitations

*   **Performance**: Rendering millions of road segments (e.g., Tokyo or Washington state) depends heavily on the client's GPU and memory.
*   **Data Volume**: Extremely large areas may cause browser instability due to memory constraints.

## Local Development

To run this project locally:

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

## Contact

*   **GitHub**: [Daivik1520](https://github.com/Daivik1520)
*   **Email**: [daivik1520@gmail.com](mailto:daivik1520@gmail.com)
*   **Instagram**: [@daivik_warrior](https://instagram.com/daivik_warrior)

## License

The source code is licensed under the MIT license.

Copyright (c) 2020-2025 DAIVIK REDDY
