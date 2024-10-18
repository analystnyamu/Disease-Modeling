\# SIR Model with Deaths for Cholera in Nairobi

This project involves simulating the \*\*SIR Model with Deaths\*\* for a cholera outbreak in Nairobi, Kenya. The model provides insights into the transmission dynamics of cholera and calculates important metrics such as the basic reproduction number (\\(R_0\\)) and the percentage of the population that needs to be vaccinated to achieve herd immunity.

\## Table of Contents

\- [Introduction](#introduction)

\- [Model Parameters](#model-parameters)

\- [Key Results](#key-results)

\- [How to Render the Document](#how-to-render-the-document)

\- [Viewing the Output](#viewing-the-output)

\- [Dependencies](#dependencies)

\- [Contact](#contact)

\## Introduction

This project uses a Quarto file (\`SIR_Model_Cholera.qmd\`) that implements the SIR model with deaths applied to a cholera outbreak in Nairobi. The model divides the population into four compartments:

\- \*\*Susceptible (S):\*\* Individuals who can contract the disease.

\- \*\*Infected (I):\*\* Individuals who have contracted the disease and can transmit it.

\- \*\*Recovered (R):\*\* Individuals who have recovered from the disease and gained immunity.

\- \*\*Deceased (D):\*\* Individuals who have died from the disease.

The document also includes Python code to simulate the spread of cholera, estimate \\(R_0\\), and calculate the percentage of the population that needs to be vaccinated to achieve herd immunity.

\## Model Parameters

The initial conditions used for the cholera outbreak in Nairobi are:

\- Total population (\\(N = 4,400,000\\))

\- Initial infected individuals (\\(I_0 = 1,172\\))

\- Initial recovered individuals (\\(R_0 = 0\\))

\- Initial deaths (\\(D_0 = 58\\))

\- Initial susceptible population (\\(S_0 = N - I_0 - R_0 - D_0 = 4,398,770\\))

\- Recovery rate (\\(\\gamma = 1/7 = 0.14286\\))

\- Death rate (\\(\\mu = 0.04949\\))

\## Key Results

\- The basic reproduction number \\(R_0\\) was estimated to be approximately \*\*2.45\*\*. This means, on average, each infected individual will spread the disease to 2.45 others in a fully susceptible population.

\- The model estimates that \*\*59.18%\*\* of the population needs to be vaccinated to achieve herd immunity and prevent further transmission of cholera in Nairobi.

\## How to Render the Document

\### Requirements

Before rendering the document, ensure that you have the following installed:

\- \*\*Quarto\*\*: If not installed, download it from [[https://quarto.org](https://quarto.org).](https://quarto.org%5D(https://quarto.org).)

\- \*\*Python 3.x\*\*: Ensure Python is installed on your machine.

\- Required Python packages: \`numpy\`, \`scipy\`, and \`matplotlib\`. You can install these packages by running:

\`\`\`bash

pip install numpy scipy matplotlib
