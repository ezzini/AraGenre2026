# **AraGenre**: A Hierarchical Few-Shot Arabic Genre Classification Shared Task

### Hosted with [Arabic Natural Language Processing Conference (ArabicNLP 2026)](https://arabicnlp2026.sigarab.org)

## 1. Overview of the Shared Task
We propose **AraGenre**, a shared task on few-shot Arabic genre classification under distributional shift. The task evaluates whether systems can identify the communicative genre of Arabic texts using limited labelled data while generalising beyond the training distribution. Unlike traditional text classification benchmarks that rely on large annotated datasets and stable distributions, AraGenre reflects realistic deployment conditions in which systems must generalise across domains, dialects, orthographic conventions, and communicative settings under minimal supervision.

AraGenre formulates genre classification as a **hierarchical prediction task**. Given an Arabic text instance, systems must predict its genre label at multiple levels of granularity — from broad communicative function to fine-grained genre subtype. Genre is treated as a function of communicative intent, discourse structure, and stylistic organisation rather than topical vocabulary alone.

Participants are provided with:
- a predefined hierarchical genre taxonomy
- short definitions of each genre category
- a few-shot labelled training set
- a labelled development set for tuning and validation

## 2. Hierarchical Genre Taxonomy

| Level 1 | Level 2 | Level 3 (Examples) |
|---------|---------|-------------------|
| Informative | Encyclopedic, Job Ads, News | History, Geography, IT Jobs, Politics, Finance, Sports |
| Creative | Literature, Lyrics | Fiction, Essays, Biographies, Poetry, Love Lyrics, Religious Lyrics |
| Authoritative | Legal, Religious | Constitutions, Legislation, Regulations, Quranic Texts, Hadith, Sermons |
| Educational | Pedagogical | Primary Education, Secondary Education |
| Interactive | Social Media, Conversational | Tweets, Reviews, Forums, Interviews, Chat Transcripts |

## 3. Motivation and Significance
Most contemporary NLP systems rely on large annotated datasets and stable training distributions. AraGenre reframes genre classification as a **constrained generalisation problem**. Systems must infer functional and stylistic properties of genre under limited supervision rather than rely on topical or lexical cues. Genre is treated as a discourse-level phenomenon shaped by communicative intent and structure.

This is particularly important in Arabic, where:
- **Linguistic diversity**: Arabic exhibits significant variation with multiple formal and dialectal forms
- **Contextual dependencies**: Performance shifts depending on genre, requiring models to capture nuanced cues
- **Limited labeled data**: Large-scale datasets for Arabic genre classification are scarce

## 4. Task Description

### Input and Output
- **Input**: A raw Arabic text segment (short fragment to longer passage), spanning MSA, Classical Arabic, and dialectal Arabic (diacritised and undiacritised)
- **Output**: A single hierarchical genre label (Level 3 prediction; Level 1 and Level 2 derived automatically)

### Evaluation Levels
| Evaluation Level | Description | Example |
|-----------------|-------------|---------|
| Level 1 | High-level communicative function | Informative, Creative, Interactive |
| Level 2 | Base genre classification | Job Advertisement, News, Lyrics |
| Level 3 (Primary) | Fine-grained genre classification | IT Job Ad, Sports News, Folk Lyrics |

## 5. Dataset
The hidden test set contains approximately **2 million text instances** spanning Modern Standard Arabic, Classical Arabic, and dialectal Arabic, including both diacritised and undiacritised text. The benchmark is constructed from resources developed through Arabic NLP initiatives led by the task organisers, including ArabicNLP.uk and SinaLab.

Dataset construction principles:
- Texts from multiple Arabic corpora with unified hierarchical annotation
- Filtering, deduplication, and balancing to reduce lexical leakage
- Metadata (source identifiers, dialect labels) removed before release
- Intentionally designed to discourage superficial lexical memorisation

## 6. Evaluation
- **Primary Metric**: Macro-averaged F1 score at Level 3 (fine-grained classification)
- **Secondary Metrics**: Macro F1 at Levels 1 and 2, accuracy, per-class F1, hierarchical consistency

## 7. Tentative Timeline
- **May 16, 2026**: Release of task website, training/dev data, and evaluation scripts
- **July 20, 2026**: Registration deadline and release of the blind test data
- **July 30, 2026**: Final results released
- **August 22, 2026**: Camera-ready system description papers due
- **September 1, 2026**: Shared task overview papers due
- **September 10, 2026**: Conference camera-ready deadline
- **October 24–29, 2026**: ArabicNLP 2026 / EMNLP 2026, Budapest, Hungary

## 8. Organizers' Details
- **Mo El-Haj** (Organising Chair), Lancaster University, UK / VinUniversity, Vietnam — m.el-haj@lancaster.ac.uk
- **Mustafa Jarrar** (Programme Chair), Hamad Bin Khalifa University (HBKU), Qatar — mjarrar@hbku.edu.qa
- **Saad Ezzini** (Programme Chair), King Fahd University of Petroleum and Minerals (KFUPM), Saudi Arabia — saad.ezzini@kfupm.edu.sa
- **Shadi Abudalfa** (Programme Chair), King Fahd University of Petroleum and Minerals (KFUPM), Saudi Arabia — shadi.abudalfa@kfupm.edu.sa
- **Vo Diep Nhu** (Publication Chair), VinUniversity, Vietnam
- **Nguyen Tran Nhat Minh** (Publication Chair), VinUniversity, Vietnam
- **Tran Anh Chuong** (Publicity Chair), VinUniversity, Vietnam
- **Pham Dinh Hieu** (Publicity Chair), VinUniversity, Vietnam
- **Ta Quang Hieu** (Participant Coordination Chair), VinUniversity, Vietnam

## 9. Participation Guidelines
- 📋 **Register here**: [AraGenre 2026 Registration Form](https://forms.gle/w1PaZ6KbmYEhZneX8)
- For participation guidelines, please refer to [Participation Guidelines](guidelines.md).
- Comprehensive instructions for preparing and submitting your paper(s) are available at [Paper Submission Guidelines](PAPER.md).

---

### Logistics and Support
- **Website Hosting**: GitHub Pages
- **Submission System**: Codabench
- **Communication**: Task mailing list and GitHub repository

### Stay Updated
- **Official Website**: https://wp.lancs.ac.uk/AraGenre

### Anti-Harassment Policy
We uphold the [ACL Anti-Harassment Policy](https://www.aclweb.org/adminwiki/index.php?title=Anti-Harassment_Policy), and participants are encouraged to reach out with any concerns to the shared task organizers.
