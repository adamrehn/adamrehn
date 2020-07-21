## Contents

- [About me](#about-me)
- [Unreal Engine projects](#unreal-engine-projects)
  - [Community websites and educational resources](#community-websites-and-educational-resources)
  - [Container-related infrastructure projects](#container-related-infrastructure-projects)
  - [Build tooling infrastructure projects](#build-tooling-infrastructure-projects)
  - [Examples and demonstrations](#examples-and-demonstrations)
  - [Multimedia streaming](#multimedia-streaming)
  - [Miscellaneous projects](#miscellaneous-projects)
- [Container utilities (not specific to the Unreal Engine)](#container-utilities-not-specific-to-the-unreal-engine)
- [Research-related projects](#research-related-projects)
- [Other utilities](#other-utilities)


## About me

I'm Dr Adam Rehn, a scientific researcher and software developer living in [Cairns, Australia](https://www.google.com.au/maps/place/Cairns+QLD). I run the applied research company [TensorWorks](https://tensorworks.com.au) and work as a university lecturer on a part-time basis. To the best of my knowledge, I am considered the world's foremost expert on Unreal Engine containers, as a result of my role as creator and primary maintainer of the projects and initiatives listed in the [Unreal Engine projects](#unreal-engine-projects) section below. I am passionate about automation, tooling and infrastructure, with a current focus on [integrating the Unreal Engine with cloud native technologies](https://adamrehn.com/articles/cloud-native-unreal-engine-vision-and-status/).

You can find more details regarding my education and employment history in my [curriculum vitae](https://adamrehn.com/curriculum-vitae). I am not actively seeking new employment opportunities at the current time.


## Unreal Engine projects

### Community websites and educational resources

- [**unrealcontainers.github.io**](https://github.com/UnrealContainers/unrealcontainers.github.io): the source code for the [Unreal Containers community hub](https://unrealcontainers.com), which acts as the central hub for developers running the Unreal Engine inside containers. The hub provides comprehensive documentation and community-curated educational resources, social links, and a list of support providers who offer professional assistance in using Unreal Engine containers. 

- [**ue4research.github.io**](https://github.com/UE4Research/ue4research.github.io): the source code for the [Unreal Engine For Research ("UE4Research") project website](https://ue4research.org/), which provides information and community resources for academics or industry researchers who wish to use the Unreal Engine to conduct scientific research. The site includes a list of resources for getting started, a literature review of publications which cite the Unreal Engine, and a discussion of the rationale for utilising the Unreal Engine within various research use cases.

### Container-related infrastructure projects

- [**ue4-docker**](https://github.com/adamrehn/ue4-docker): command-line tool and accompanying Dockerfiles that provides functionality for building both Windows and Linux container images for the Unreal Engine.

- [**ue4-runtime**](https://github.com/adamrehn/ue4-runtime): a set of Linux container images that provide minimal, pre-configured environments for running packaged Unreal Engine projects with full GPU acceleration via the [NVIDIA Container Toolkit](https://github.com/NVIDIA/nvidia-docker).

### Build tooling infrastructure projects

- [**ue4cli**](https://github.com/adamrehn/ue4cli): library and associated command-line tool that provides a convenient and platform-agnostic interface for working with the Unreal Engine. Commands are provided for key workflow tasks relating to Unreal projects and plugins, and for querying the details of third-party libraries that are bundled with the Unreal Engine.

- [**conan-ue4cli**](https://github.com/adamrehn/conan-ue4cli): a plugin for ue4cli that provides functionality for integrating third-party libraries into Unreal Engine projects and plugins using the [Conan C++ package management system](https://conan.io/).

- [**ue4-conan-recipes**](https://github.com/adamrehn/ue4-conan-recipes): contains the default recipes that ship with conan-ue4cli. Includes recipes for a growing number of popular open source libraries and frameworks.

- [**ue4-ci-helpers**](https://github.com/adamrehn/ue4-ci-helpers): a Python package designed to provide abstractions that simplify the process of writing platform-agnostic build scripts for Unreal projects and plugins, which can be run as part of Continuous Integration (CI) pipelines.

### Examples and demonstrations

- [**ue4-example-dockerfiles**](https://github.com/adamrehn/ue4-example-dockerfiles): a collection of example Dockerfiles that demonstrate various uses of Unreal Engine containers, including building projects and plugins, packaging dedicated servers, and packaging projects that use [Pixel Streaming for Linux](https://adamrehn.com/articles/pixel-streaming-in-linux-containers/).

- [**ue4-grpc-demo**](https://github.com/adamrehn/ue4-grpc-demo): an example project with accompanying Dockerfiles demonstrating how to build a simple Unreal-based microservice that uses Google's popular [gRPC](https://grpc.io/) framework for communication, and run the microservice inside a Linux container. **(Note that this demo has not yet been updated to reflect the extensive overhaul of conan-ue4cli that occurred in early 2020.)**

- [**ue4-opencv-demo**](https://github.com/adamrehn/ue4-opencv-demo): an old example project demonstrating how to use conan-ue4cli to build a custom OpenCV package that links against the Unreal-bundled versions of zlib and libpng, and then consume the custom-built OpenCV package in a simple Unreal project. **(Note that this demo has not yet been updated to reflect the extensive overhaul of conan-ue4cli that occurred in early 2020.)**

- [**ue4-cloud-rendering-demo**](https://github.com/adamrehn/ue4-cloud-rendering-demo): **[NOTE THAT THIS DEMO USES THE NOW-DEPRECATED UE4CAPTURE PLUGIN, WHICH HAS BEEN REPLACED BY PIXEL STREAMING AND [PIXEL STREAMING FOR LINUX](https://adamrehn.com/articles/pixel-streaming-in-linux-containers/)]** An old example project with accompanying Dockerfiles that demonstrates how to use the deprecated UE4Capture plugin inside GPU-accelerated Linux containers to stream audio and video to a web browser via WebRTC.

### Multimedia streaming

- [**pixel-streaming-linux**](https://github.com/adamrehn/pixel-streaming-linux): this repository acts as the public issue tracker for [Pixel Streaming For Linux](https://adamrehn.com/articles/pixel-streaming-in-linux-containers/). Note that this repository does not contain the actual source code for the Linux implementation of Pixel Streaming, which is stored in the various branches of [my fork of the official Unreal Engine repository](https://github.com/adamrehn/UnrealEngine). *(You will need to be logged in with a GitHub account that [has been granted access](https://www.unrealengine.com/en-US/ue4-on-github) to the upstream Unreal Engine repository in order to access the fork.)*

- [**UE4Capture**](https://github.com/adamrehn/UE4Capture): **[NOTE THAT THIS PROJECT IS DEPRECATED AND HAS BEEN REPLACED BY PIXEL STREAMING AND [PIXEL STREAMING FOR LINUX](https://adamrehn.com/articles/pixel-streaming-in-linux-containers/)]** An old proof-of-concept prototype that provided a cross-platform implementation of audio and framebuffer capture, designed for use with standardised streaming protocols such as WebRTC. This plugin predated the release of Epic's official Pixel Streaming system by several months, and development was discontinued when Pixel Streaming was unveiled.

### Miscellaneous projects

- [**ue4-utils**](https://github.com/adamrehn/ue4-utils): a collection of assorted utilities for working with or understanding the internals of Unreal Engine 4. The most useful tool in this collection is [switchfinder](https://github.com/adamrehn/ue4-utils/tree/master/switchfinder), which assists in identifying all of the Unreal Engine's supported command-line switches (many of which are undocumented.)


## Container utilities (not specific to the Unreal Engine)

- [**docker-shell**](https://github.com/adamrehn/docker-shell): command-line tool that makes it quick and easy to start interactive shells inside both Windows and Linux containers while automatically bind-mounting the current working directory from the host system. Automatically activates common features when supported by the host system (e.g GPU acceleration) and highly configurable using Docker image labels. See the [**developer-images**](https://github.com/adamrehn/developer-images) repository for examples of container images designed for use with docker-shell.

- [**dll-diagnostics**](https://github.com/adamrehn/dll-diagnostics): command-line tool that provides functionality to assist in identifying the DLL dependencies of an application or library and diagnosing dependency loading issues. Primarily intended for use when migrating existing applications to Windows containers, where traditional GUI-based tools are unavailable.


## Research-related projects

- [**charcoal-morphotypes**](https://github.com/adamrehn/charcoal-morphotypes): source code for the charcoal particle segmentation and classification system presented in the journal article: [Emma Rehn, Adam Rehn, and Aidan Possemiers. Fossil charcoal particle identification and classification by two convolutional neural networks. *Quaternary Science Reviews*, 226:106038, 2019.](https://www.sciencedirect.com/science/article/pii/S0277379119305074)

- [**VideoAnnotator**](https://github.com/adamrehn/VideoAnnotator): GUI tool to facilitate annotation of video files with custom metadata that can then be ingested by data processing pipelines and used as training data for machine learning algorithms. Primarily intended for use by artificial intelligence and computer vision researchers.

- [**Taxonomist**](https://github.com/adamrehn/taxonomist): GUI tool to facilitate manually categorising images into classes so that they can be used as training data for image classification algorithms. Primarily intended for use by artificial intelligence and computer vision researchers.

- [**ClimateQuery**](https://github.com/adamrehn/ClimateQuery): GUI tool to facilitate processing and querying weather data obtained from the [Australian Bureau of Meteorology](http://www.bom.gov.au/). Allows researchers to extract data for specific weather stations and time periods, and then run queries against the extracted datasets to produce summarised data that is suitable for further statistical analysis.


## Other utilities

- [**gen-invoice**](https://github.com/adamrehn/gen-invoice): library and associated command-line tool that provides a flexible, template-driven system for generating invoices and quotes in both HTML and PDF format.

- [**mergetiff (Python version)**](https://github.com/adamrehn/mergetiff) and [**mergetiff (C++ version)**](https://github.com/adamrehn/mergetiff-cxx): libraries and associated command-line tool that provides functionality to merge raster bands from multiple GeoTiff files into a single dataset. Primarily useful when working with multispectral image data or raster bands representing per-pixel labels for training machine learning models.
