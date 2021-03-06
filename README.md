# tripadvisor
Suggesting Best Hotels on TripAdvisor

Get Dataset from : http://nemis.isti.cnr.it/~marcheggiani/datasets/

Description :-

TripAdvisor Annotated
Three equally experienced annotators provided sentence-level annotations of a subset of 500 randomly selected reviews from the
publicly available TripAdvisor dataset *. The full TripAdvisor dataset consists of 235793 hotel reviews crawled over a period
of one month.
In addition to the review text, each review comes with a hotel identifier, an overall rating and optional aspect-specific ratings
for the following seven aspects: Rooms, Cleanliness, Value, Service, Location, Checkin, and Business.
All review-level ratings are on a discrete ordinal scale from 1 to 5
(with -1 indicating that an aspect-specific rating was not provided by the reviewer).



- Annotation : The annotations are related to nine aspects typically mentioned in hotel reviews.
In addition to the seven aspects explicitly present (at the review level) in the TripAdvisor dataset, we decided to add two
other aspects (aspectFood and Building), since many comments in the reviews refer to them. Furthermore, the “catch-all” aspects
 Other and NotRelated were added, for a total of eleven aspects.

Other : captures those opinion-related aspects that cannot be assigned to any of the first nine aspects, but which are still about
 the hotel under review, for example, Extremely friendly place.
The NotRelated aspect : captures those opinion-related aspects that are not relevant to the hotel under review, as for example
 in The crew on our flight were wonderful. ￼￼￼￼￼


The annotation distinguishes between Positive, Negative and Neutral/Mixed opinions.
The Neutral/Mixed label is assigned to opinions that are about an aspect without expressing a polarized opinion, and to opinions
 of contrasting polarities, such as The room was average size (neutral) and Pricey but worth it! (mixed). The annotations also
 distinguish between explicit and implicit opinion expressions, that is, between expressions that refer directly to an aspect
 and expressions that refer indirectly to an aspect by referring to some other property/entity that is related to the aspect.
 For example, Fine rooms is an explicitly expressed positive opinion concerning the Rooms aspect, while We had great views over
 the East River is an implicitly expressed positive opinion concerning the Location aspect, and All doors seem to have to slam to
 close is an implicit negative opinion concerning the Rooms aspect.

- Annotation process
Each of the three annotators was assigned
 139 unique reviews, plus 83 reviews which all three annotators independently annotated, for a total of 500 annotated reviews.
 The 83 shared reviews were used to measure inter-annotator agreement, as described below. To minimize bias in these measurements,
 the reviews were ordered in such a way that every eighth review was shared between all the annotators; this ensures that each
 annotator had the same amount of annotation experience when annotating the same shared review, and that these annotations are
 comparable to the remaining annotations in terms of annotator experience.

During the annotation process, the annotators identified
 a number of corrupted reviews (primarily caused by site scraping errors in the original TripAdvisor data set).
These reviews were
 subsequently removed from the final dataset, which as a result consists of 442 reviews, of which 73 shared among all three
 annotators. The remaining 369 unique reviews were partitioned into a training set (258 reviews, 70% of the total) and a test set
 (111 reviews, 30% of the total). The data was split by selecting reviews for each subset in an interleaved fashion, so that each
 subset constitutes a minimally biased sample both with respect to the full dataset and with respect to annotator experience.



This archive conitains : README file,
The ./tripadvisor directory with the three file: test.zero.json, test.one.json and
 test.two.json; these are the annotated reviews shared by the three annotators Zero, One and Two. The ./tripadvisor directory
 also contains the train.unique.json and test.unique.json, that are training and test files where each review is annotated by
 only one annotator.
The ./tripadvisor-pos-lemma contains the same file of the ./tripadvisor directory, with associated to each
 word that compose the review, its lemma and part-of-speech tag, obtained with the NLTK toolkit.



If you use the dataset please acknowledge its use with a citation: Marcheggiani, D., Täckström, O., Esuli, A, Sebastiani,
F.: Hierarchical Multi-Label Conditional Random Fields for Aspect-Oriented Opinion Mining. In: Proceedings of the 36th
European Conference on Information Restrieval (ECIR 2014).


* Wang, H., Lu, Y., Zhai, C.: Latent aspect rating analysis on review text data: A rating regression approach.
 In: Proceedings of the 16th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining (KDD 2010). pp. 783–792.
 Washington, US (2010)