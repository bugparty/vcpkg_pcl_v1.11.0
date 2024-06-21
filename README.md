# vcpkg Port Overlay for PCL (Point Cloud Library)

This repository provides an overlay port for the Point Cloud Library (PCL) to be used with vcpkg. This allows for the installation of PCL version 1.11.0, specifically tailored for use on Ubuntu 20.04.

## Purpose

The primary purpose of this overlay is to enable the installation and usage of PCL 1.11.0, the latest version, on Ubuntu 20.04. This ensures compatibility and optimizes performance for users running this specific version of Ubuntu.

## Usage

To install the PCL library using this overlay, follow the steps below:

1. Clone this repository to your local machine and place it under your current user's folder.

    ```sh
    git clone https://github.com/yourusername/bowman-ports.git
    ```

2. Navigate to your vcpkg directory.

    ```sh
    cd path/to/vcpkg
    ```

3. Install PCL using the overlay ports.

    ```sh
    ./vcpkg install pcl --overlay-ports=bowman-ports
    ```

## PCL Overview

The Point Cloud Library (PCL) is an open-source library for 2D/3D image and point cloud processing. PCL contains numerous state-of-the-art algorithms including filtering, feature estimation, surface reconstruction, registration, model fitting, and segmentation.

### Key Features

- Extensive set of algorithms for 3D point cloud processing.
- Support for 2D/3D image processing.
- Open source and community-driven.

### Dependencies

The following dependencies are required by PCL and are specified in the `vcpkg.json`:

- Boost libraries (`asio`, `date-time`, `dynamic-bitset`, `filesystem`, `foreach`, `graph`, `interprocess`, `iostreams`, `multi-array`, `property-map`, `ptr-container`, `random`, `signals2`, `sort`, `system`, `thread`, `uuid`)
- `eigen3`
- `flann`
- `libpng`
- `qhull`
- `vcpkg-cmake` (host)
- `vcpkg-cmake-config` (host)

### Optional Features

PCL can be built with additional features by specifying them during the installation process. The available features include:

- `qt`: Qt support for PCL.
- `openni2`: OpenNI2 support for PCL.
- `visualization`: Build visualization tools.
- `vtk`: Alias for visualization.

