# One Million Impressions (OMI) Dataset

![alt text](https://github.com/jcpeterson/omi/blob/main/data_example.png?raw=true)

Authors: [Joshua Peterson](https://twitter.com/joshuacpeterson/), [Stefan Uddenberg](https://www.stefanuddenberg.com), [Thomas Griffiths](https://cocosci.princeton.edu/), [Alexander Todorov](https://tlab.uchicago.edu/), [Jordan Suchow](https://suchow.io/)

The One Million Impressions (OMI) dataset contains over a million human judgments of over 1,000 synthetic face images along 34 attributes. When making use of the data in your research, please cite the associated publication:

> Peterson, J. C., Uddenberg, S., Griffiths, T., Todorov, A., & Suchow, J. W. (2022). Deep models of superficial face judgments. *Proceedings of the National Academy of Sciences (PNAS).*

BibTeX entry:

```
@article{peterson2022omi,
  title={Deep models of superficial face judgments},
  author={Peterson, Joshua C and Uddenberg, Stefan and Griffiths, 
  Thomas L and Todorov, Alex and Suchow, Jordan W},
  journal={Proceedings of the National Academy of Sciences},
  year={2022},
  publisher={National Acad Sciences}
}
```
## License

The data is distributed under the Creative Commons BY-NC-SA 4.0 license. If you intend to use it, please see [LICENSE.txt](https://github.com/jcpeterson/omi/blob/main/LICENSE.txt) for more information.

## Future Updates

Please make sure to check the [main repository](https://github.com/jcpeterson/omi/) link for any updated or corrected versions of this dataset.

## Repository Contents

Mean judgements on each of the 34 attributes for each of the 1,004 face stimuli can be found in `attribute_ratings.csv`. The corresponding synthetic face stimuli are located in the `images` folder.

## Validation Data

We also include data from the additional validation experiments reported in Peterson et al. (2022). The aggregated data is provided in `processed_validation_data.csv`, and the more fine-grained trial-level data is provided in `raw_validation_data.csv`, the legend for which is below:

- `rt` = how long it took for the participant to complete the trial
- `condition` = attribute we manipulated the faces along
- `response` = the rating from 0 to 100 that the participant gave for that face
- `stimulus_type` = real or artificial face
- `stimulus_index` = the ID of the face. for those from the Chicago Face Dataset, they start with "CFD", while artificial faces are some arbitrary number greater than 1004
- `stimulus_level` = 0, 1, or 2 for low, medium, and high levels of that attribute. In practice 1 is mean, 0 is -0.5 SD, and 2 is +0.5 SD
- `repeat` = whether this is a repeat showing of the face

The face image stimuli for these experiments are located in the `validation_images` folder.

## Credits

The face dataset used to create underlying model components that in turn were used to generate our synthetic faces can be found at:

https://github.com/NVlabs/ffhq-dataset

The above-mentioned model components themselves can be found at:

https://github.com/NVlabs/stylegan2
