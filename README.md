![License](https://img.shields.io/badge/license-MIT-blue.svg)

# (ƒ , $\Gamma$)-Divergence
Visualized examples from [Dupui's and Mao's](https://arxiv.org/pdf/2011.08441.pdf) and [Birrell's](https://arxiv.org/pdf/2011.05953.pdf) papers.

* Dirac Masses: Example 3.1, in [page 13](https://arxiv.org/pdf/2011.05953.pdf)
* Gaussian: Theorem 6.8, in [page 114](https://arxiv.org/pdf/2011.08441.pdf)
* Unifrom: Example 1, section (4.1) in [page 42](https://arxiv.org/pdf/2011.08441.pdf).

### Special cases of (ƒ , $\Gamma$)-divergences
![Alt-txt](cases.png)

# Mass Redistribution/Transport
## Dirac Masses
Here we consider a simple example involving Dirac masses where the (f, Γ)-divergence can be explicitly computed
using [Theorem 3.3](https://arxiv.org/pdf/2011.05953.pdf). This example further illustrates the two-stage mass-redistribution/mass-transport interpretation of
the infimal convolution formula and demonstrates how the location and distribution of probability mass impacts
the result.

|Case 1                               |  Case 2                                   |
|:-----------------------------------:|:-----------------------------------------:|
|![Alt-txt](gif/dirac/dirac_case1.gif)|![Alt-txt](gif/dirac/dirac_case2.gif)      |


## Gaussian

<img src="gaussian_cases_formula.png" width="350"/>


|1) P ~ N(1, 0.5),  Q ~ N(3, 0.5)            |2) P ~ N(1, 0.5),  Q ~ N(3, 1)              |3) P ~ N(1, 1),  Q ~ N(3, 0.5)                |
|:------------------------------------------:|:------------------------------------------:|:------------------------------------------:|
|![Alt-txt](gif/gaussian/Gaussian_case_1.gif)|![Alt-txt](gif/gaussian/Gaussian_case_2.gif)|![Alt-txt](gif/gaussian/Gaussian_case_3.gif)|


## Uniform
For given c, b solves: exp(1 − b) − (1 − b) = 1 + c <br />
When c = 0, b = 1 solves the equation. When c > 0 is small, 1 − b is also close to 0. Moreover, 1 − b can be written as an analytic function of √c
around 0 as 1-b = √2√c - c/3 + O(c^(3/2)). <br />

<img src="uniform.png" width="350"/> <img src="gif/uniform.gif" width="380" height="320"/>

# Run Examples
To reproduce the achieved results run the file of your choice with the corresponding arguments. The output is a gif visualizing the Mass Redistribution and Transport respectivly to the chosen case (Dirac, Gaussian or Uniform).

## Dirac Masses (Case 2)
| Argument   | Default Value  | Info                                            |Choices                                |
|:----------:|:--------------:|:-----------------------------------------------:|:--------------------------------------:|
| `--h`      | 0.1            | [float] Position of $\eta^*(x_2)$ from 0.5      | -0.5 < h < 0.5                        |

`Note`: [Dirac case 1](scripts/Dirac_case1.py) has no arguments.

## Gaussian
| Argument   | Default Value  | Info                                            |Choices
|:----------:|:--------------:|-------------------------------------------------|:---------:|
| `--m1`     | 1.0            | [float] Mean of distribution P                  | -  
| `--sd1`    | 0.5            | [float] Standard deviation of distribution P    | -  
| `--m2`     | 3.0            | [float] Mean of distribution Q                  | -
| `--sd2`    | 1.0            | [float] Standard deviation of distribution Q    | -

`Note`: Default values corresponds to Case 2.

## Uniform
| Argument   | Default Value  | Info                                            |Choices
|:----------:|:--------------:|-------------------------------------------------|:---------:|
| `--c`      | 0.5            | [float] Parameter of distribution P             | 0 < c < e-2

`Note`: c value must be positive and less than e-2, thus 1-b ≥ 0.

# References
```
@article{dupuis2022formulation,
  title={Formulation and properties of a divergence used to compare probability measures without absolute continuity},
  author={Dupuis, Paul and Mao, Yixiang},
  journal={ESAIM: Control, Optimisation and Calculus of Variations},
  volume={28},
  pages={10},
  year={2022},
  publisher={EDP Sciences}
}
```


```
@article{JMLR:v23:21-0100,
  author  = {Jeremiah Birrell and Paul Dupuis and Markos A. Katsoulakis and Yannis Pantazis and Luc Rey-Bellet},
  title   = {(f,Gamma)-Divergences: Interpolating between f-Divergences and Integral Probability Metrics},
  journal = {Journal of Machine Learning Research},
  year    = {2022},
  volume  = {23},
  number  = {39},
  pages   = {1--70},
  url     = {http://jmlr.org/papers/v23/21-0100.html}
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

