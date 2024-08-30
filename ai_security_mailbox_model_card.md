# Model Card for Abnormal Security AI Security Mailbox

The Abnormal Security Security AI Security Mailbox (AISM) is a conversational AI model for end-users to ask to submit potential phishing emails and chat with an AI analyst.

## Model Details

### Model Description

Our AISM model is derived from OpenAI’s GPT4o model hosted on Azure. No finetuning is done and control of the model is performed through prompting and via in-context learning. The prompt context includes details from the end user, reported message, Abnormal detection signals encoded as text, and formatting instructions. The output is the analysts reply in markdown that’s rendered as HTML for the end user.

- **Developed by:** OpenAI
- **Model type:** Large Multimodal Model
- **Language(s) (NLP):** Multilingual
- **License:** Azure OpenAI License

## Uses

### Direct Use

This model can be used to converse on cybersecurity related topics and questions around Abnormal judgment on a reported email.

### Out-of-Scope Use

This model is not intended for conversations on topics outside of Abnormal, cybersecurity, or a customer’s IT context. 

This model does not classify messages and instead relies on the Abnormal Security Detection Engine model for a message’s judgment.

## Bias, Risks, and Limitations

Our application of the base model has no known additional biases.

For details on the base model, see OpenAI’s GPT4o system card: https://openai.com/index/gpt-4o-system-card/

### Recommendations

This model should be used to generate responses on end-user submitted phishing reports. 

## How to Get Started with the Model

Customers who use the Abnormal Security product and purchase our AI Security Mailbox product will have access to use and configure this model.

## Training Details

### Training Data

No additional training was done on the base model. In context learning is done with human witten text-based instructions that specify the tone, formatting, and use case context to the model.

See https://openai.com/index/gpt-4o-system-card/ for details on the base model.

### Training Procedure

#### Training Hyperparameters

N/A

## Evaluation

### Testing Data, Factors & Metrics

#### Testing Data

We use artificial reported messages and end user questions to simulate and score the model’s conversational efficacy. 

#### Factors

The model does not use any disaggregation factors.

#### Metrics

We use a variety of validation steps to ensure the performance of the model. Our primary release metric is an automated (LLM-based) score of responses against a human-defined rubric on response expectations.

### Results

On our curated artificial test set, released models are expected to score roughly >= 8.0 (of 10) on average against the rubric.

#### Summary

### Compute Infrastructure

N/A

#### Hardware

N/A

#### Software

This model is accessed over the Azure OpenAI API.

## Model Card Contact

info@abnormalsecurity.com



