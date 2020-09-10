## MEgATrack: Monochrome Egocentric Articulated Hand-Tracking for Virtual Reality

Overview
It is a real-time hand-tracking system which can drive virtual and augmented reality (VR/AR) experiences. Using four fisheye monochrome cameras, the system generates accurate and low-jitter 3D hand motion across a large working volume for a diverse set of users.

Related Work
RGB-based approaches
Early RGB-based methods [de La Gorce et al. 2008; Prisacariu and Reid 2011; Stenger et al. 2006] follow an analysis-by-synthesis paradigm, fitting a hand model to low level visual cues such as edges, skin color, silhouettes and optical flow. This is extremely challenging given the self-similarity, subtle color variation, and severe self-occlusion exhibited by hands.
Depth-based approaches
Depth sensors have been widely applied to hand-tracking [Mueller et al. 2019; Oikonomidis et al. 2012; Sharp et al. 2015; Tagliasacchi et al. 2015; Taylor et al. 2016, 2017; Zhang et al. 2019a]. Model-based approaches can reliably fit a hand mesh to the reconstructed point cloud provided by the depth sensor, but this approach does not generalize to RGB images.
Data Generation
In this work, depth tracker has been used to generate ground truth hand poses for training the keypoint estimation network. This model based tracker requires minimal human intervention (2D bounding boxes) if the tracker fails. The system maximizes the quality of the ground truth data without sacrificing mobility. As a result, training set is larger and more diverse in terms of hand shape, pose and background variation than any previously proposed RGB datasets.
Data Generation At Scale
Since existing RGB hand pose datasets do not generalise well to new environments and camera configuration. Therefore, there was need to find there own datasets for DETNET and KEYNET neural network. The two tasks have different requirements: hand detection requires only that the annotated bounding boxes be accurate, but needs a camera configuration as similar as possible to the target configuration, while keypoint estimation is less sensitive to the camera configuration (since the network sees only a crop) but needs accurate annotation of the entire hand pose. We therefore developed two scalable methods for generating high quality data for training DetNet and KeyNet in real-world scenarios.
1. Keypoint labels from depth-based hand-tracking 2. Semi-automatic bounding box labeling
Applications
Typical Failures and Future Works
The failures for hand-hand and hand-object interactions reflect both the limitation of our system design and the fundamental difficulty of these tasks. We believe jointly reasoning about the two hands and handheld objects is an important direction for a better hand-tracking system.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/VaishnaveeSharma/VR-Presentation-MEgATrack/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
