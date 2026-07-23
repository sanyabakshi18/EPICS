# Early Alert: An Explainable ML-Based Symptom Triage System for Cardiovascular and Neurological Risk Screening
1. Problem Statement
Timely recognition of disease risk from everyday symptoms is a major challenge for individuals in underserved or rural areas who lack easy access to doctors. Cardiovascular and neurological symptoms are two of the most common yet consequential complaint categories: cardiovascular symptoms can signal life-threatening emergencies if ignored, while neurological symptoms are frequently misjudged or self-diagnosed incorrectly. Most existing symptom-checker tools are either static rule-based systems that cannot adapt to nuanced symptom combinations, or opaque ML classifiers that give a label without explanation. This lack of transparency reduces user trust, and most tools remain English-only, limiting accessibility for a large section of the target population.
2. Proposed Solution
This project proposes Early Alert, a web-based symptom triage system that uses trained ML/DL models, rather than static rules, to predict probable causes and urgency from user-reported symptoms, while explaining its reasoning in plain language. The system covers two well-researched, high-impact categories: cardiovascular symptoms (e.g., chest pain, breathlessness) and neurological symptoms (e.g., headache, dizziness). Users can select symptoms from a structured, picture-guided interface or describe them in free text, in either English or Hindi, making the tool usable for non-English-literate users. For cardiovascular symptoms, a rule-based safety-override layer ensures high-risk combinations always trigger an immediate 'seek medical attention' recommendation regardless of model confidence. The system concludes by directing users to nearby doctors or clinics.
3. Objectives
●	Design an ML classification pipeline predicting probable causes and severity of cardiovascular and neurological symptoms from structured and free-text input.
●	Build an NLP component to extract structured symptoms from free-text descriptions in English or Hindi.
●	Incorporate an explainability layer (SHAP) that communicates model reasoning in plain language.
●	Implement a safety-override mechanism for high-risk cardiovascular symptom patterns.
●	Evaluate predictive performance against existing benchmark symptom-checker studies.
4. Methodology
●	Data Collection: Use established public datasets — UCI Heart Disease dataset for cardiovascular symptoms, and Kaggle Disease-Symptom / DDXPlus for neurological symptom coverage.
●	Symptom Classification: Train supervised ML classifiers (Random Forest, XGBoost, lightweight neural network) to predict probable causes with confidence scores.
●	NLP Symptom Extraction: Fine-tune a transformer-based NER model (BERT variant) to extract structured symptoms from free text.
●	Language Layer: Integrate a Hindi-English translation model (e.g., IndicTrans2) so the interface, questions, and explanations are available in both languages.
●	Severity and Safety Layer: Combine a trained severity classifier with a rule-based override for high-risk cardiovascular presentations.
●	Explainability: Apply SHAP to generate human-interpretable justifications for each prediction.
●	Web Application: Build a bilingual web interface with symptom entry, predictions, explanations, and a nearby doctor/clinic locator (maps API).
●	Evaluation: Assess accuracy, precision, recall, and severity-classification performance against benchmarks from existing literature.
5. Expected Outcome
A functional, bilingual (English/Hindi) web prototype that accepts structured or free-text symptom input for cardiovascular and neurological complaints, producing an explainable, confidence-scored assessment of likely causes and urgency, with safety guidance and nearby healthcare facility recommendations. The system is intended as an awareness and triage aid, not a diagnostic replacement, and consistently directs users to consult a medical professional for high-severity presentations.
6. Target Community and Future Scope
The system targets individuals in rural or underserved areas facing barriers to timely medical consultation, particularly non-English speakers, who are addressed through the bilingual interface. A full voice-assistant mode (speech input/output in Hindi and English) is identified as a natural future extension for users with low literacy, to be explored beyond this year's scope.
7. Domain and Technologies
Domain: Machine Learning, Deep Learning, Data Science (Clinical NLP, Explainable AI, Machine Translation). Tools: Python, Scikit-learn, XGBoost, TensorFlow/PyTorch, Hugging Face Transformers (BERT-based NER), IndicTrans2, SHAP, Flask/Django, Maps API. Datasets: UCI Heart Disease Dataset, Kaggle Disease-Symptom Dataset, DDXPlus.
