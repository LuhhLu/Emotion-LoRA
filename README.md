## 1. Introduction

Advances in machine learning and image generation have opened new possibilities in understanding human emotional responses to visual stimuli. In particular, Low-Rank Adaptation (LoRA) techniques allow for efficient fine-tuning of large-scale image-generation models (e.g., Stable Diffusion, Flux, etc.) with fewer computational resources. This study aims to leverage LoRA to generate images that evoke specific emotional responses and test how different image content correlates with perceived emotion in human subjects.

### 1.1 Research Problem
Despite the growing interest in using AI-generated images for psychological and behavioral research, there is a lack of systematic methods to:
1. Generate controlled stimuli (images) that represent distinct emotional categories.
2. Measure participants’ emotional responses and correlate them with the emotional intent of the images.

### 1.2 Research Questions
1. Can LoRA-trained image models produce images with distinguishable emotional tones (e.g., sadness, happiness, fear, anger)?
2. How strongly does the image content correlate with participants’ reported emotional responses?
3. Which aspects of the images (color, composition, subject matter) most significantly affect participants’ emotional perception?

### 1.3 Objectives
1. **Develop LoRA-trained models** capable of generating images representing various emotional categories.
2. **Design a questionnaire** to assess human emotional responses to these images.
3. **Analyze the correlation** between the intended emotional content (as designed in the LoRA training) and the self-reported emotional responses of participants.
4. **Evaluate methodology** for consistency, reliability, and validity in measuring emotional responses to AI-generated images.

---

## 2. Literature Review

- **Behavioral Science and Imagery**: Previous studies show that visual stimuli can elicit measurable emotional and psychological responses. Commonly, standardized image sets like the International Affective Picture System (IAPS) have been used for controlled studies, but they are limited in variety.
- **AI-Generated Stimuli**: Recent advancements in generative models allow the creation of novel images not restricted by copyright or ethical constraints often encountered with real-world images.
- **LoRA for Efficient Fine-Tuning**: Research suggests that LoRA is an efficient way to adapt large language and image models to specific tasks or emotional contexts without retraining the entire model. This method retains model capacity while significantly reducing training costs.

---

## 3. Methodology

### 3.1 Study Design
This study will employ an **experimental design** with human participants exposed to AI-generated images. Each image will be labeled (internally) for an intended emotional category (e.g., joy, sadness, fear, anger, surprise). Participants will complete a questionnaire rating their perceived emotional response to each image.

### 3.2 Data Collection

1. **Image Collection for Training**  
   - **Social Media Sources**: We will gather images from publicly available social media platforms that depict a range of emotional expressions and contexts (e.g., people’s facial expressions, scenes, color palettes).  
   - **Filtering and Labeling**: Images will be curated and labeled with basic emotional tags (e.g., “happy,” “sad,” “neutral”) using a combination of automated sentiment analysis tools and human annotators for higher accuracy.

2. **Training the LoRA Models**  
   - We will use a **Flux** (or similar diffusion-based) image model as the base.  
   - **Low-Rank Adaptation (LoRA) Setup**: Integrate specialized layers trained on the labeled dataset, focusing on distinct emotional categories.  
   - **Training Process**:  
     - Split labeled images into training, validation, and test sets.  
     - Fine-tune the model on each emotional subset separately or employ multi-class labels.  
     - Monitor model performance with internal metrics (FID scores, classification accuracy of emotional content, etc.).

### 3.3 Stimuli Generation
- **Generating Images**: Using the LoRA models, generate a set of images, each intended to represent a specific emotional category. We will ensure:  
  1. **Variety**: Each emotional category should have multiple generated images to avoid over-reliance on a single style or composition.  
  2. **Consistency**: Generated images should adhere to standardized resolution and format to maintain visual consistency during the experiment.

### 3.4 Participants
- **Sample Size and Demographics**: Recruit a balanced sample of participants (e.g., 60-100 participants) representing diverse age groups, genders, and cultural backgrounds to ensure generalizability.
- **Inclusion Criteria**:  
  1. Adults (18+ years old) with normal or corrected-to-normal vision.  
  2. Voluntary consent and ability to understand the study’s instructions.  

### 3.5 Procedure
1. **Informed Consent**: Participants sign consent forms, detailing the study’s purpose, procedures, and data handling.
2. **Instruction and Familiarization**: Participants receive a brief introduction on how to proceed with the questionnaire.
3. **Image Presentation**:  
   - Images are presented in random order to mitigate ordering effects.  
   - Each image is displayed for a fixed duration (e.g., 5 seconds) or until the participant indicates readiness to continue.
4. **Questionnaire**:  
   - Immediately after each image, participants rate their perceived emotional response using a **Likert scale** (e.g., 1 = Not at all, 5 = Extremely) for categories such as happiness, sadness, fear, anger, and so on.  
   - Additional open-ended questions could capture any unlisted emotions or free-form responses.
5. **Debriefing**: Once the session is complete, participants can provide qualitative feedback on their experience.

### 3.6 Measurements
1. **Primary Outcome**: The **difference** or **similarity** between the participant’s perceived emotion ratings and the image’s intended emotional category.  
2. **Secondary Measures**:  
   - Reaction time (how quickly participants respond).  
   - Qualitative feedback (free-text responses or short interviews).

### 3.7 Data Analysis
1. **Descriptive Statistics**: Summarize participant demographics, average emotional ratings per image, and distribution of responses.
2. **Correlation Analysis**: Conduct **Pearson** or **Spearman** correlations between the intended emotional label and the participants’ rating scores.  
3. **ANOVA or MANOVA**: Examine differences in ratings across multiple emotional categories.  
4. **Classification Accuracy**: Check how frequently participants’ top-rated emotion matches the intended emotion of the image.

---

## 4. Ethical Considerations
- **Privacy**: Ensure that any images collected from social media are either under open licenses or used with permission, stripping any identifiable information.
- **Informed Consent**: Participants must fully understand the study’s scope and their rights to withdraw at any time.
- **Emotional Well-Being**: Some images (especially those depicting negative emotions) could be distressing. Provide participants with contact information for mental health support and remind them they can skip any image.

---

## 5. Expected Outcomes
1. **Validated Set of Emotionally-Tuned Images**: A repository of AI-generated images with empirically tested emotional impact.
2. **Correlation Insights**: Empirical data on how closely the intended emotional content aligns with human-perceived emotions.
3. **Refined LoRA Methodology**: Improved training pipelines for generating emotionally consistent images with minimal computational overhead.
4. **Questionnaire Validation**: Potential further validation of the emotional response questionnaire as a reliable measurement tool.

---

## 6. Potential Limitations
1. **Generalizability**: Emotional perception may vary across cultures, so results might not generalize globally.
2. **Subjectivity in Emotion**: People differ in how they interpret visual cues; some might perceive a “sad” image as “calm” or “nostalgic.”
3. **Bias in Social Media Data**: The initial dataset may contain biases (e.g., certain demographics or emotional expressions more represented than others).
4. **Model Artifacts**: AI-generated images can sometimes include artifacts that might distract or confuse participants.

---

## 7. Timeline
1. **Phase 1 (1–2 months)**: Data gathering and preliminary labeling of social media images.
2. **Phase 2 (2–3 months)**: LoRA model training, validation, and internal testing.
3. **Phase 3 (1 month)**: Finalizing stimuli set and preparing questionnaires.
4. **Phase 4 (1–2 months)**: Participant recruitment and experimental data collection.
5. **Phase 5 (1 month)**: Data analysis and result interpretation.
6. **Phase 6 (1 month)**: Writing final report/publication.
