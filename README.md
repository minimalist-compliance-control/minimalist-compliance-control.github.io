# Research Paper Website Template

This is a website template for academic research papers, based on the [Nerfies](https://nerfies.github.io/) project page.

## Quick Start

1. **Edit `index.html`** and replace the placeholder content:
   - Update paper title, authors, and affiliations
   - Add your resource links (paper PDF, arXiv, video, code, data)
   - Write your abstract
   - Update the BibTeX citation

2. **Add your media files** to the appropriate folders:
   - `static/videos/` - Your video files (teaser.mp4, etc.)
   - `static/images/` - Your images (favicon.svg, interpolation frames, etc.)

3. **Replace video placeholders** in index.html:
   ```html
   <!-- Replace this -->
   <div class="video-placeholder">Placeholder text</div>
   
   <!-- With this -->
   <video autoplay muted loop playsinline height="100%">
     <source src="./static/videos/your-video.mp4" type="video/mp4">
   </video>
   ```

4. **For YouTube embeds:**
   ```html
   <iframe src="https://www.youtube.com/embed/YOUR_VIDEO_ID?rel=0&amp;showinfo=0"
           frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
   ```

5. **Deploy** via GitHub Pages or any static file host.

## File Structure

```
├── index.html                  # Main page
├── README.md                   # This file
└── static/
    ├── css/
    │   ├── bulma.min.css       # Bulma CSS framework
    │   ├── bulma-carousel.min.css
    │   ├── bulma-slider.min.css
    │   ├── fontawesome.all.min.css
    │   └── index.css           # Custom styles
    ├── js/
    │   ├── bulma-carousel.min.js
    │   ├── bulma-slider.min.js
    │   ├── fontawesome.all.min.js
    │   └── index.js            # Custom scripts
    ├── images/                 # Your images
    │   ├── favicon.svg
    │   ├── interpolate_start.jpg
    │   └── interpolate_end.jpg
    └── videos/                 # Your videos
        ├── teaser.mp4
        └── ...
```

## Features

- **Responsive design** using Bulma CSS framework
- **Video carousel** for showcasing multiple results
- **Interpolation slider** for interactive demos
- **Publication links** with icons (PDF, arXiv, YouTube, GitHub, Data)
- **Mobile-friendly** navigation

## Customization

### Changing the Method Name Style
The `.dnerf` class applies small-caps styling. Find and replace `YourMethod` with your method name:
```html
<span class="dnerf">YourMethod</span>
```

### Interpolation Slider
To enable the interpolation slider:
1. Create interpolation frames as JPG files named `000000.jpg` to `000239.jpg`
2. Place them in `./static/interpolation/stacked/`
3. Uncomment the interpolation images in index.html
4. Adjust `NUM_INTERP_FRAMES` in `static/js/index.js` if needed

### Adding Google Analytics
Uncomment the analytics section in the `<head>` and replace `YOUR-GA-ID` with your tracking ID.

## License

This template is licensed under [CC BY-SA 4.0](http://creativecommons.org/licenses/by-sa/4.0/).

**Requirements:**
- Link back to the [Nerfies source code](https://github.com/nerfies/nerfies.github.io) in your footer
- Remove the analytics code if you don't want tracking

## Credits

- Original template: [Nerfies: Deformable Neural Radiance Fields](https://nerfies.github.io/) by Park et al.
- CSS Framework: [Bulma](https://bulma.io/)
- Icons: [Font Awesome](https://fontawesome.com/) and [Academicons](https://jpswalsh.github.io/academicons/)

## Citation

If you use this template, please cite the Nerfies paper:

```bibtex
@article{park2021nerfies,
  author    = {Park, Keunhong and Sinha, Utkarsh and Barron, Jonathan T. and Bouaziz, Sofien and Goldman, Dan B and Seitz, Steven M. and Martin-Brualla, Ricardo},
  title     = {Nerfies: Deformable Neural Radiance Fields},
  journal   = {ICCV},
  year      = {2021},
}
```
