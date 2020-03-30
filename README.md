---
description: Rule sets and reference documentation for Goobi workflow
---

# Documentation UGH Library

Document management has always been the main task of libraries. With the beginning of the digitisation of information, the task has changed dramatically. Metadata is increasingly used to find, sort and evaluate information. The bound book as a unit of information is increasingly divided into a multitude of smaller units \(structures/document structures\) in order to be able to present them in a meaningful and usable way on the Internet. In order to be able to implement these functionalities, different data formats have been developed over the past years, which store the necessary meta-information for a document and refer to the actual content \(e.g. TIFF, XML or HTML files\). It is also common practice to aggregate metadata to a document from different sources and to add to it if necessary.

For software development, this results in some special features. Since data formats change or are extended quickly and different projects have different requirements for data formats \(different data must be stored\), it is advisable to use a data format that is as flexible and well-defined as possible. To be able to process different formats, it is also advisable that all tools and programs are based on a uniform programming interface \(API\).

The UGH library represents such a programming interface, which can and should be used by different tools and programs to load and save data. This interface implements a universal document model, which is independent of underlying formats for describing meta information. Instead, there are different classes for serializing a document. Each of these classes implements exactly one data format. Superior program layers \(e.g. the business logic\) are therefore completely independent of the data format. Note, however, that not all data formats can always implement the complete universal document model. Similarly, some serialization classes can only read data, since writing is not required for this data format or does not seem to make much sense. This applies, for example, to classes that transfer data formats from library catalogs. Since only the bibliographic level is usually represented there, all structure information and references could not be written. For this reason, a write method was not used for these classes.

