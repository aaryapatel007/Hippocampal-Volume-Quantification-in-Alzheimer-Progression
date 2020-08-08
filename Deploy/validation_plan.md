# Validation Plan
## What is the intended use of the product?
 The intended use is to build an end-to-end AI system which features a machine learning algorithm that integrates into a clinical-grade viewer and automatically measures hippocampal volumes of new patients.
## How was the training data collected?
We are using the "Hippocampus" dataset from the Medical Decathlon competition. This dataset is stored as a collection of NIFTI files, with one file per volume, and one file per corresponding segmentation mask. The original images here are T2 MRI scans of the full brain. Our radiology department runs a HippoCrop tool which cuts out a rectangular portion of a brain scan from every image series, and our committed radiologists have collected and annotated a dataset of relevant volumes.
## How did you label your training data?
The training data has been labeled and verified by expert radiologists.
## How was the training performance of the algorithm measured and how is the real-world performance going to be estimated?
The training performance of the algorithm is measured by using the following evaluation metrics:
* Dice Similarity Coefficient
* Jaccard Distance
* Sensitivity
* Specificity

The real-world performance is estimated by expert radiologists.
## What data will the algorithm perform well in the real world and what data it might not perform well on?
Below we can see the performance of our model on real-world data. We see that our model performs well on most of the volumes. The performance of hippocampus_280 ID isn't up to the mark. It's dice score is 0.82 and jaccard score is 0.695.

```
{
  "volume_stats": [
    {
      "filename": "hippocampus_019.nii.gz",
      "dice": 0.8799207023506089,
      "jaccard": 0.7855878634639697,
      "sensitivity": 0.9258045292014303,
      "specificity": 0.9958431644691187
    },
    {
      "filename": "hippocampus_319.nii.gz",
      "dice": 0.8828369905956113,
      "jaccard": 0.7902490354261662,
      "sensitivity": 0.9302229562345169,
      "specificity": 0.9967682642038178
    },
    {
      "filename": "hippocampus_171.nii.gz",
      "dice": 0.9147826086956522,
      "jaccard": 0.842948717948718,
      "sensitivity": 0.9305933587370713,
      "specificity": 0.997265295018828
    },
    {
      "filename": "hippocampus_327.nii.gz",
      "dice": 0.9241680305510093,
      "jaccard": 0.859026369168357,
      "sensitivity": 0.9300027449903925,
      "specificity": 0.9979070042346658
    },
    {
      "filename": "hippocampus_157.nii.gz",
      "dice": 0.9065064478311841,
      "jaccard": 0.8290002680246583,
      "sensitivity": 0.9227326968973747,
      "specificity": 0.9973699550324765
    },
    {
      "filename": "hippocampus_154.nii.gz",
      "dice": 0.9313068097153926,
      "jaccard": 0.8714445064138315,
      "sensitivity": 0.9594719066625729,
      "specificity": 0.9976517276575091
    },
    {
      "filename": "hippocampus_033.nii.gz",
      "dice": 0.9027474923680767,
      "jaccard": 0.8227344992050875,
      "sensitivity": 0.9070990359333918,
      "specificity": 0.9973357622680178
    },
    {
      "filename": "hippocampus_149.nii.gz",
      "dice": 0.9237432327919567,
      "jaccard": 0.8582926128197758,
      "sensitivity": 0.9500477251034044,
      "specificity": 0.997455027456921
    },
    {
      "filename": "hippocampus_335.nii.gz",
      "dice": 0.8661095636025998,
      "jaccard": 0.7638388470357026,
      "sensitivity": 0.9210110584518167,
      "specificity": 0.9959467869923759
    },
    {
      "filename": "hippocampus_251.nii.gz",
      "dice": 0.8969086987778576,
      "jaccard": 0.8130865484880083,
      "sensitivity": 0.8724475524475525,
      "specificity": 0.9981860009313251
    },
    {
      "filename": "hippocampus_144.nii.gz",
      "dice": 0.9068251533742331,
      "jaccard": 0.8295334970185899,
      "sensitivity": 0.9571023876972885,
      "specificity": 0.9972220800771969
    },
    {
      "filename": "hippocampus_385.nii.gz",
      "dice": 0.9115312454899697,
      "jaccard": 0.8374436488994962,
      "sensitivity": 0.9296438033559022,
      "specificity": 0.9973278652215228
    },
    {
      "filename": "hippocampus_328.nii.gz",
      "dice": 0.9300380228136882,
      "jaccard": 0.8692253020611229,
      "sensitivity": 0.9272175890826384,
      "specificity": 0.9982596198851613
    },
    {
      "filename": "hippocampus_351.nii.gz",
      "dice": 0.8844221105527639,
      "jaccard": 0.7927927927927928,
      "sensitivity": 0.8979591836734694,
      "specificity": 0.9964622303703916
    },
    {
      "filename": "hippocampus_333.nii.gz",
      "dice": 0.868161094224924,
      "jaccard": 0.76703591809332,
      "sensitivity": 0.8671726755218216,
      "specificity": 0.9974044200312375
    },
    {
      "filename": "hippocampus_190.nii.gz",
      "dice": 0.9147063068263819,
      "jaccard": 0.8428191489361702,
      "sensitivity": 0.9576911453611363,
      "specificity": 0.9969576978339618
    },
    {
      "filename": "hippocampus_228.nii.gz",
      "dice": 0.8649685017803341,
      "jaccard": 0.762065637065637,
      "sensitivity": 0.8602560610187959,
      "specificity": 0.9968014822729087
    },
    {
      "filename": "hippocampus_067.nii.gz",
      "dice": 0.9333818711321441,
      "jaccard": 0.875085324232082,
      "sensitivity": 0.912130914265386,
      "specificity": 0.9991772961388227
    },
    {
      "filename": "hippocampus_368.nii.gz",
      "dice": 0.8820760133195544,
      "jaccard": 0.7890304026294166,
      "sensitivity": 0.8727561917745967,
      "specificity": 0.9969123354512817
    },
    {
      "filename": "hippocampus_280.nii.gz",
      "dice": 0.8200820472748583,
      "jaccard": 0.6950331125827814,
      "sensitivity": 0.803291236127057,
      "specificity": 0.9972673376348706
    },
    {
      "filename": "hippocampus_180.nii.gz",
      "dice": 0.9181203275186899,
      "jaccard": 0.8486344192168477,
      "sensitivity": 0.9630321135175504,
      "specificity": 0.9975751306473931
    },
    {
      "filename": "hippocampus_336.nii.gz",
      "dice": 0.8702400288756542,
      "jaccard": 0.7702875399361022,
      "sensitivity": 0.9298110296953336,
      "specificity": 0.9960708562899225
    },
    {
      "filename": "hippocampus_146.nii.gz",
      "dice": 0.9314460172078823,
      "jaccard": 0.8716883116883117,
      "sensitivity": 0.9528676888131743,
      "specificity": 0.9977211777620298
    },
    {
      "filename": "hippocampus_243.nii.gz",
      "dice": 0.8768942618763834,
      "jaccard": 0.78077622801698,
      "sensitivity": 0.8711096075778079,
      "specificity": 0.9974909763183378
    },
    {
      "filename": "hippocampus_289.nii.gz",
      "dice": 0.8736254440872949,
      "jaccard": 0.7756082907780114,
      "sensitivity": 0.9430241051862673,
      "specificity": 0.9957972436745317
    },
    {
      "filename": "hippocampus_172.nii.gz",
      "dice": 0.9156414762741653,
      "jaccard": 0.8444084278768234,
      "sensitivity": 0.9296456793270457,
      "specificity": 0.9970740573809858
    },
    {
      "filename": "hippocampus_393.nii.gz",
      "dice": 0.9009105516871987,
      "jaccard": 0.8196881091617934,
      "sensitivity": 0.9136338946224878,
      "specificity": 0.9970648378705468
    },
    {
      "filename": "hippocampus_236.nii.gz",
      "dice": 0.893188359449952,
      "jaccard": 0.8069921987864779,
      "sensitivity": 0.9041761087730658,
      "specificity": 0.9974943251853997
    },
    {
      "filename": "hippocampus_360.nii.gz",
      "dice": 0.8915071183112421,
      "jaccard": 0.804251550044287,
      "sensitivity": 0.9293756397134084,
      "specificity": 0.99665524854584
    },
    {
      "filename": "hippocampus_160.nii.gz",
      "dice": 0.9181561618062088,
      "jaccard": 0.8486956521739131,
      "sensitivity": 0.9307056579783852,
      "specificity": 0.9977666436474235
    },
    {
      "filename": "hippocampus_308.nii.gz",
      "dice": 0.9386937358087352,
      "jaccard": 0.884470173672288,
      "sensitivity": 0.9616858237547893,
      "specificity": 0.9979012329434057
    },
    {
      "filename": "hippocampus_152.nii.gz",
      "dice": 0.9330949948927477,
      "jaccard": 0.874581139301101,
      "sensitivity": 0.9148723084626941,
      "specificity": 0.9987174303996877
    },
    {
      "filename": "hippocampus_361.nii.gz",
      "dice": 0.8728760226557584,
      "jaccard": 0.774427694025684,
      "sensitivity": 0.8933977455716586,
      "specificity": 0.9966955545856974
    },
    {
      "filename": "hippocampus_252.nii.gz",
      "dice": 0.9090647482014389,
      "jaccard": 0.833289369559483,
      "sensitivity": 0.8836363636363637,
      "specificity": 0.9985403136973989
    },
    {
      "filename": "hippocampus_345.nii.gz",
      "dice": 0.891856247939334,
      "jaccard": 0.8048199940493901,
      "sensitivity": 0.9077181208053692,
      "specificity": 0.9970255753677044
    },
    {
      "filename": "hippocampus_098.nii.gz",
      "dice": 0.9277150916784203,
      "jaccard": 0.8651759289707334,
      "sensitivity": 0.9103806228373702,
      "specificity": 0.9989842730489298
    },
    {
      "filename": "hippocampus_017.nii.gz",
      "dice": 0.921122599704579,
      "jaccard": 0.8537787513691129,
      "sensitivity": 0.8964922369177688,
      "specificity": 0.9987560944224417
    },
    {
      "filename": "hippocampus_001.nii.gz",
      "dice": 0.9163228255487704,
      "jaccard": 0.8455680779774596,
      "sensitivity": 0.9416553595658074,
      "specificity": 0.9976141640315642
    },
    {
      "filename": "hippocampus_024.nii.gz",
      "dice": 0.9051294820717132,
      "jaccard": 0.8267000227427792,
      "sensitivity": 0.901985111662531,
      "specificity": 0.9975794430740413
    }
  ],
  "overall": {
    "mean_dice": 0.9013032933247428,
    "mean_jaccard": 0.8212850238885452,
    "mean_sensitivity": 0.9157399992552947,
    "mean_specificity": 0.9973857931301461
  },
  "config": {
    "name": "Recursive_unet",
    "root_dir": "../data/train",
    "n_epochs": 10,
    "learning_rate": 0.0003,
    "batch_size": 16,
    "patch_size": 64,
    "test_results_dir": "../out"
  }
}
```