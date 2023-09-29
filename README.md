# Bayesian Statistics Introduction COVID-19 Vaccine Efficacy
Project 1 for STA 141A: Statistical Data Science

In this report, we are replicating a study done by Pfizer:

https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjpmLK7ys6BAxXiUEEAHVHlCGQQFnoECA4QAQ&url=https%3A%2F%2Fmedia.tghn.org%2Fmedialibrary%2F2020%2F11%2FC4591001_Clinical_Protocol_Nov2020_Pfizer_BioNTech.pdf&usg=AOvVaw1pAYzP6iVhj0n_KqOVSBH5&opi=89978449

In [A PHASE 1/2/3, PLACEBO-CONTROLLED, RANDOMIZED, OBSERVER-BLIND, DOSE-FINDING STUDY TO EVALUATE THE SAFETY, TOLERABILITY, IMMUNOGENICITY, AND EFFICACY OF SARS-COV-2 RNA VACCINE CANDIDATES AGAINST COVID-19 IN HEALTHY INDIVIDUALS], an experiment by the Pfizer Corporation, researchers aim to find the effectiveness of their SARS-COV-2 RNA vaccine against COVID-19. To do so, they use Bayesian statistics to estimate the probability that a subject who fell ill with COVID-19 is vaccinated or not.

As a newcomer to the field of Bayesian Statistics, I feel the need to define some key terms.

A posterior probability is the probability of assigning observations to groups given the data. A prior probability is the probability that an observation will fall into a group before you collect the data.

The central variable that we are trying to measure is VE, vaccine efficacy. According to Page 99 of the Pfizer report, VE is initially defined as VE = 100 × (1 – IRR). IRR is calculated as the ratio of first confirmed COVID-19 illness rate in the vaccine group to the corresponding illness rate in the placebo group. This can be expressed equivalently with variables set for the two population probabilities of infection.

Let πv and πc be the population probabilities that a vaccinated subject or a subject in the control group, respectively, fall ill to Covid-19. Then the population vaccine efficacy is given by VE=1−πv*πc.

In Phase 2/3, the assessment of VE will be based on posterior probabilities of VE1 > 30% and VE2 > 30%. VE1 represents VE for prophylactic BNT162b2 against confirmed COVID-19 in participants without evidence of infection before vaccination, and VE2 represents VE for prophylactic BNT162b2 against confirmed COVID-19 in all participants after vaccination.

The criteria for success at an interim analysis is based on these posterior probabilities. Overwhelming efficacy will be declared if the posterior probability is higher than the success threshold.

Using the above formulas, we can rewrite θ using VE’s equivalencies as θ = πvπc+πc.
