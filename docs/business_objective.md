# Karachi House Prices Predictor - Business Objective

## 1) Problem Statement
Build a machine learning system that predicts residential property prices in Karachi using:
- Structured listing features (for example: covered area, number of rooms, location, building age, floors, and property type)
- Text-derived features extracted from listing descriptions (for example: west open, corner plot, near airport, sea view)

The model is intended to support faster and more consistent pricing decisions in a noisy real-estate market where listing quality and feature format vary significantly.

## 2) Target Users and Decision Context
- Buyers: estimate whether an asking price is likely fair.
- Sellers: set competitive listing prices.
- Agents: benchmark listings and explain expected value ranges to clients.

This is a decision-support tool, not a replacement for expert appraisal.

## 3) Product Output
For each property listing, the system should return:
- Predicted price (PKR)
- Optional confidence caveat (for example: low/medium/high confidence based on data completeness and similarity to training data)

## 4) Success Criteria
### Primary Metric (Model Quality)
- Mean Absolute Percentage Error (MAPE) on a holdout test set
- Initial milestone target: MAPE <= 15-20%

Rationale:
- MAPE is interpretable for non-technical stakeholders because it expresses error in percentage terms.

### Secondary Metric (Fairness/Robustness Across Segments)
- Error stability across:
  - Key Karachi locations
  - Price bands (lower, mid, upper range)

Rationale:
- A model that performs well on average but fails in specific locations or price bands is not reliable for practical use.

## 5) Business Rules and Non-Goals
### Business Rules
- Predictions are advisory and should be reviewed with domain judgment.
- Model output should include caveats for uncertain or uncommon listings.

### Non-Goals
- This project does not produce legally binding valuations.
- This project does not replace certified appraisal or due diligence.

## 6) Scope for Initial Milestone
Included in early phase:
- Establish a clean objective, metrics, and documentation baseline.
- Prepare data workflow for structured plus text-engineered features.

Not included yet:
- Full production deployment
- Real-time monitoring and automated retraining loops

## 7) Stakeholder Explanation (Non-Technical Version)
We are building a system that estimates house prices in Karachi by learning from previous listings. It looks at both standard fields (size, rooms, area, age) and important clues written in descriptions (such as "corner" or "west open"). The result helps buyers, sellers, and agents make better pricing decisions, while still requiring human judgment for final decisions.

## 8) Why Defining This Now Matters
Freezing the objective before modeling prevents random experimentation, keeps evaluation aligned with business value, and makes future model decisions explainable to both technical and non-technical stakeholders.
