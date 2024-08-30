# Model Card for Abnormal Security Detection Engine

The Abnormal Security Detection Engine detects cyberattacks in an email environment.

## Model Details

### Model Description

This model consumes a vast array of information associated with an email to make a decision about whether the email is attack, safe, spam, or graymail. This is a multimodal model that can process data in a variety of modalities, including the headers, body text, links, and attachments in an email, as well as the contextual information associated with the email recipient and the threat intelligence associated with the email.

- **Developed by:** Abnormal Security
- **Model type:** Multimodal Neural Network Model
- **Language(s) (NLP):** Multilingual
- **License:** Proprietary

## Uses

### Direct Use

This model can be used directly to determine if an email is attack, safe, spam, or graymail. 

### Out-of-Scope Use

This model is not useful for applications outside of cyberattack detection. 

## Bias, Risks, and Limitations

This model is limited in its scope, and does not have any known biases.

### Recommendations

This model should be used to protect an email ecosystem.

## How to Get Started with the Model

Customers who use the Abnormal Security product will have their email environments protected by this model

## Training Details

### Training Data

This model is trained on a dataset of hundreds of millions of attacks that Abnormal has processed in the past. This dataset includes attacks detected by the attack detection system, attacks reported to the AI Security Mailbox product, and attacks reported to the D360 product.

### Training Procedure

#### Training Hyperparameters

The model uses a deep and cross network architecture with float32 precision.

## Evaluation

### Testing Data, Factors & Metrics

#### Testing Data

The last week of training data is held out as testing data for the model. 

#### Factors

The model does not use any disaggregation factors.

#### Metrics

This model must detect attacks with extremely high precision in order to avoid causing damage to customer environments. In order to accomplish this the model is evaluated based on the recall over all attacks in the testing dataset at a threshold that yields a precision of at least 95%.

### Results

This model is capable of detecting 92% of all known advanced attacks at a 95% precision. 


#### Hardware

This model is trained on a single r6id.32xlarge AWS instance.

#### Software

This model is trained using tensorflow, keras and numpy

## Model Card Contact

info@abnormalsecurity.com

