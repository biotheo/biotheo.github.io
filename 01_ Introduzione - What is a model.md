# 01_ Introduzione - What is a model?
Due tipologie di modello:
- **Modello *deterministico*** Lotka-Volterra è un modello matematico che descrive un fenomeno
- **Modello *statistico*** Modello maxent di species distribution basato su un regression model, usando predictor var. proviamo a prevedere un effetto, non fanno assunzioni sulle relazioni tra le variabili; a differenza dei primi necessitano di molti dati

=> A model is an idealised representation of reality
" All models are false, but some are useful" cit. George E.P. Box [inventore dei boxplot]
The art of modelling is the art of deciding what to include and what to leave out

## Linear Model: esprime la relazione tra due variabili
formula y = m x + q + E   --- dove E (epsilon) descrive la normalitÃ  della distribuzione
E = N ( 0, sigma_piccolo^2) cioè che ha una distr. norm da 0 ad una SD^2

Different inference methods to estimate the parameters:
i. Frequentists (MLE)  ii. Bayesian (MCMC)
For both approaches the concept of Likelihood!

Likelihood example: we visiti a lake 11 times, we find frogs 7 time
n = 11   total number of visits
y = 7    total number of visits w/ frogs
n-y = 4  total number of visits w\ frogs
P => probability to see a frog
(l-p) => probability of not seeing it
L = p p p p p p p (l-p) (l-p) (l-p) (l-p)
Likelihood probabilità che io effettivamente veda delle rane se vado in quel sito
$$L= \frac{n!} {y!(n-y)!} * p^y * (l-p)^{(n-y)}$$

Maximum likelihood find the set of parameters (e.g. intercepts and coeff) that make the observed data most likely to have occurerd. This estimaeted parametes are thus the MAXIMUM LIKELIHOOD ESTIMATES of our statistical model. For linear regression, the max likelihood estimates are equivalent to the ordinary least squares estimates.
