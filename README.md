# Topic Modeling 



In text mining, we often have collections of documents, such as blog posts or news articles, that we’d like to divide into natural groups so that we can understand them separately. Topic modeling is a method for unsupervised classification of such documents, similar to clustering on numeric data, which finds natural groups of items even when we’re not sure what we’re looking for.

## A Topic Modeling Comparison Between LDA, LSA, and BERTopic to Demystify Transcripts of a Recorded Session

If there is one phrase that we will not forget long
after 2020, it is “stay at home, stay safe.” The
pandemic forced people around the world to stay at
home to help curb the spread of the virus. Everyone
who could do it started to work in remote
environments. This has led to a surge in popularity
for videoconferencing services like Zoom, Cisco
WebEx, Microsoft Teams, or Google Hangouts
Meet. This new social distancing culture has forced
people to be creative about staying social through
online meetings, with school, concerts, ceremonies,
fitness programs moving from the real world to
screens. Because we are having more virtual
meetings in organizations than ever, joining all of
them might be unproductive and time-consuming
for executives and employees. So, in this project I
tried to provide a simulation of a recorded meeting
between an interviewer to business magnate,
philanthropist, and co-founder of Microsoft Bill
Gates, in order to provide topic summaries from
that meeting/interview to those people who could
not attend, using various topic modeling
techniques. These techniques rely on statistical
modeling to extract topical patterns within a
collection of texts. For instance, since a semantic
relationship exists between terms like “apple”,
“pear”, and “mango” they could be formed under a
topic called “fruit” in a text corpus (i.e., a
collection of documents). Typically, documents
contain mixed membership, which means that a
mixture of topics exists in the corpus.


Appertaining to the insufficient knowledge of small
corpus of documents (small dataset of the
transcripts taken from the recorded session), this
study thus aims to evaluate and compare the
performance of three topic modeling techniques,
namely, Latent Dirichlet Allocation (LDA), Latent Semantic Analysis (LSA), and BERTopic on a common
dataset (20 Newsgroups) and on the recorded
session transcripts corpus.

Specifically, LDA is a generative statistical model,
LSA is a popular dimensionality-reduction
technique that follows the same method as Singular
Value Decomposition (SVD), and BERTopic uses
an embedding approach.

## Data Collection and Preprocessing

For familiarization of the different topic modeling
techniques and setting a benchmark for a common
dataset, I used the well-known 20 Newsgroups
dataset. The 20 Newsgroups dataset is a collection
of approximately 20,000 newsgroup documents,
partitioned (nearly) evenly across 20 different
newsgroups. The 20 newsgroups collection has
become a popular dataset for experiments in text
applications of machine learning techniques, such
as text classification and text clustering.
The next dataset (tedtalk_corpus dataset) was
created for the purpose of this research. It is a
transcript from a recorded session between an
interviewer and Bill Gates. The subject of this
interview, taken by the title, is: “The innovations
we need to avoid a climate disaster” (the full
interview is available at
https://www.ted.com/talks/bill_gates_the_innovations_we_need_to_avoid_a_climate_disaster?language=en). Using the Google Cloud speech-to-text API
and implementation in python I was able to create a
transcript of the recorded session. That transcript
was then sliced into documents (sentences) to
create the desired corpus for the implementation of
the different topic models.
On both datasets, text preprocessing was done
using NLP modules in python. More precisely,
stopwords were excluded, irrelevant text (e.g.,
numbers, abbreviations, and unknown characters)
was removed, and tokenization was performed.
Following this step, bigram (and trigram) and
lemmatization were then conducted. The former
process is combining two words (or three words in
the case of trigram) frequently occurring together
in the document to a single term (e.g., ‘oil leak’ to
‘oil_leak’), whereas the latter used to remove
inflectional endings and to return a word to its base
form (e.g., investigating to investigate). Lastly, the
text was converted into term frequency-inverse document frequency (TF-IDF) weight for
information retrieval based on the importance of a
keyword.
