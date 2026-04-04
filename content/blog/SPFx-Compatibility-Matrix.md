---
title: "SPFx Compatibility Matrix" # Title of the blog post.
date: 2022-04-27T00:00:00-04:00 # Date of post creation.
description: "Understanding what SharePoint Framework (SPFx) is and how to develop with it is important to be able to customize and expand your SharePoint capabilities." # Description used for search engine.
featured: false # Sets if post is a featured post, making appear on the home page side bar.
draft: true # Sets whether to render this page. Draft of true will not be rendered.
#toc: false # Controls if a table of contents should be generated for first-level links automatically.
# menu: main
#usePageBundles: false # Set to true to group assets like images in the same folder as this post.
featureImage: "/images/blog/getting-started-with-sharepoint-framework-spfx/featured-getting-started-with-sharepoint-framework-spfx.jpg" # Sets featured image on blog post.
#featureImageAlt: 'Description of image' # Alternative text for featured image.
#featureImageCap: 'This is the featured image.' # Caption (optional).
thumbnail: "/images/blog/getting-started-with-sharepoint-framework-spfx/thumbnail-getting-started-with-sharepoint-framework-spfx.png" # Sets thumbnail image appearing inside card on homepage.
#shareImage: "/images/path/share.png" # Designate a separate image for social media sharing.
#codeMaxLines: 10 # Override global value for how many lines within a code block before auto-collapsing.
#codeLineNumbers: false # Override global value for showing of line numbers within code block.
#figurePositionShow: true # Override global value for showing the figure label.
redirectUrl: 'https://www.marathonus.com/about/blog/getting-started-with-sharepoint-framework-spfx/'
categories:
  - Getting Started
tags:
  - SharePoint
  - SPFx
  - ReactJS
  - Webpart
comment: false # Disable comment if false.
---
## SPFx Compatibility Matrix

As each new version of the SPFx is released, support for newer library versions is updated to ensure the toolset remains current.

> [!IMPORTANT]
> **React Version Compatibility**
> 
> Using incompatible React versions can cause silent runtime failures without clear error messages during the build process. Always use the exact React version specified in the compatibility table below for your SPFx version.
>
> When installing React packages, use the `--save-exact` flag to prevent npm from installing newer patch versions:
>
> ```console
> npm install react@17.0.1 react-dom@17.0.1 --save-exact
> ```

The following table lists the SPFx and compatible versions of common tools and libraries:

| SPFx                                                                                          | Node.js (LTS) | TypeScript     | React       | Release Date       |
| --------------------------------------------------------------------------------------------- | ------------- | -------------- | ----------- | ------------------ |
| [1.22.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.22.md)       | v22           | v2.9 - v5.8    | v17.0.1     | November 19, 2025  |
| [1.21.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.21.1.md)     | v22           | v5.3           | v17.0.1     | May 3, 2025        |
| [1.21.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.21.md)       | v22           | v5.3           | v17.0.1     | April 23, 2025     |
| [1.20.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.20.md)       | v18           | v4.5, v4.7     | v17.0.1     | September 26, 2024 |
| [1.19.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.19.md)       | v18           | v4.5, v4.7     | v17.0.1     | April 30, 2024     |
| [1.18.2](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.18.2.md)     | v16, v18      | v4.5, v4.7     | v17.0.1     | November 21, 2023  |
| [1.18.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.18.1.md)     | v16, v18      | v4.5, v4.7     | v17.0.1     | November 7, 2023   |
| [1.18](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.18.md)         | v16, v18      | v4.5, v4.7     | v17.0.1     | September 12, 2023 |
| [1.17.4](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.17.4.md)     | v16.13+       | v4.5           | v17.0.1     | June 21, 2023      |
| [1.17.3](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.17.3.md)     | v16.13+       | v4.5           | v17.0.1     | May 31, 2023       |
| [1.17.2](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.17.2.md)     | v16.13+       | v4.5           | v17.0.1     | May 8, 2023        |
| [1.17.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.17.1.md)     | v16.13+       | v4.5           | v17.0.1     | April 12, 2023     |
| [1.17.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.17.md)       | v16.13+       | v4.5           | v17.0.1     | April 4, 2023      |
| [1.16.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.16.1.md)     | v16.13+       | v4.5           | v17.0.1     | November 30, 2022  |
| [1.16.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.16.md)       | v16.13+       | v4.5           | v17.0.1     | November 15, 2022  |
| [1.15.2](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.15.2.md)     | v12, v14, v16 | v4.5           | v16.13.1    | August 2, 2022     |
| [1.15.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.15.md)       | v12, v14, v16 | v4.5           | v16.13.1    | June 21, 2022      |
| [1.14.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.14.md)       | v12, v14      | v3.9           | v16.13.1    | February 17, 2022  |
| [1.13.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.13.1.md)     | v12, v14      | v3.9           | v16.13.1    | November 23, 2021  |
| [1.13.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.13.md)       | v12, v14      | v3.9           | v16.13.1    | October 21, 2021   |
| [1.12.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.12.1.md)     | v10, v12, v14 | v3.7           | v16.9.0     | April 28, 2021     |
| ~~[1.12.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.12.0.md)~~ | ~~v12, v10~~  | ~~v3.7~~       | ~~v16.9.0~~ | March 15, 2021     |
| [1.11.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.11.0.md)     | v10           | v3.3           | v16.8.5     | July 16, 2020      |
| [1.10.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.10.0.md)     | v8, v10       | v3.3           | v16.8.5     | January 7, 2020    |
| [1.9.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.9.1.md)       | v8, v10       | v2.9           | v16.8.5     | August 14, 2019    |
| [1.8.2](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.8.2.md)       | v8, v10       | v2.9           | v16.7.0     | May 7, 2019        |
| [1.8.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.8.1.md)       | v8            | v2.7, v2.9, v3 | v16.7.0     | April 16, 2019     |
| [1.8.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.8.0.md)       | v8            | v2.7, v2.9, v3 | v16.7.0     | March 14, 2019     |
| [1.7.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.7.1.md)       | v8            | v2.4           | v16.3.2     | December 18, 2018  |
| [1.7.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.7.md)         | v8            | v2.4           | v16.3.2     | November 8, 2018   |
| [1.6.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.6.md)         | v6, v8        | v2.4           | v15         | September 5, 2018  |
| [1.5.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.5.1.md)       | v6, v8        | v2.4           | v15         | June 26, 2018      |
| [1.5.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.5.md)         | v6, v8        | v2.4           | v15         | June 5, 2018       |
| [1.4.1](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.4.1.md)       | v6, v8        | v2.4           | v15         | February 15, 2018  |
| [1.4.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.4.md)         | v6            | v2.4           | v15         | December 7, 2017   |
| [1.3.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.3.md)         | v6            | v2.4           | v15         | September 25, 2017 |
| [1.1.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.1.md)         | v6            | v2.4           | v15         | June 6, 2017       |
| [1.0.0](https://github.com/SharePoint/sp-dev-docs/blob/main/docs/spfx/release-1.0.0.md)       | v6            | v2.4           | v15         | February 22, 2017  |

