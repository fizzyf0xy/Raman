# Experiment design

For measuring glucose concentration in blood by Raman Spectroscopy, we need to ensure that our instruments are into proper condition and they can measure the results correctly.

The experiment design are divided as two sections below

1. Glucose concentration in water (distilled water)
2. Glucose concentration in blood 

Before we do both experiments aboved, we need to measure all of the noises of instrument as a reference to remove background noises in preprocessing process.

## 1. Glucose concentration in water
This experimant design is based on the paper name [Rapid, Sensitive and Selective Optical Glucose Sensing with Stimulated Raman Scattering (SRS)](https://github.com/fizzyf0xy/Raman/blob/main/review%20literature.md#1-rapid-sensitive-and-selective-optical-glucose-sensing-with-stimulated-raman-scattering-srs)

**Glucose concentration preparation**
  Reference concentration: 75, 50, 25, 10, 5, 2.5 $mol/m^3$

  Converted reference concentration: 13.5 ,9 ,4.5 , 1.8, 0.9 ,0.45 mg/ml
### 1.1) Prepare glucose concentration
| Glucose concentration (mg/ml) | Preparation |
|:----:|------|
|13.5|  **We prepare the maximum concentration first** |
|      |weigh glucose 0.135 g. in 13.5 ml of distilled water|
|9| Take 6 ml from the first stock, and dilute with diluent to a final volume of exactly 9 ml.|
|4.5| Take 5 ml from the first stock, and dilute with diluent to a final volume of exactly 10 ml.|
|1.8| Take 4 ml from the first stock, and dilute with diluent to a final volume of exactly 10 ml.|
|0.9| Take 5 ml from the first stock, and dilute with diluent to a final volume of exactly 10 ml.|
|0.45| Take 5 ml from the first stock, and dilute with diluent to a final volume of exactly 10 ml.|

We measure each concentration by our instrument but it's not same as actual condition of the reference paper,
(They recorded a linear calibration curve for glucose concentrations below 100 mol/m^3 with a theoretical limit of detection (LOD) of 3.5 $mol/m^3$ in a 0.6 s integration time.)

### 1.2) Prepare instrument condition
After we prepared all of glucose concentration, we'll set the first parameters of our instrument

| Parameters | Value |
|:----:|:----:|
|Laser|785 nm|
|Grating|600 nm|
|Accumulation time|1|
|Exposure time|1|

### 1.3) Measure all of glucose concentration
Then we collect three measuements on every sample for improving accuracy

## 2. Glucose concentration in blood
