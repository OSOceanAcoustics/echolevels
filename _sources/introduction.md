# Introduction

(This text **for now** is unchanged from the introduction text in the echopype documentation page)

The decades-long experience from the satellite remote sensing community has shown that a set of robust and well-articulated definitions of "data processing levels" [1]–[5] can lead directly to broad and highly productive use of data. Processing level designations also provide important context for data interpretation [6]. However, no such community agreement exists for active acoustic data. The ambiguity associated with the interoperability and inter-comparability of processed sonar data products has hindered efficient collaboration and integrative use of the rapidly growing data archive across research institutions and agencies.

The `echopype` team is developing a clearly defined progression of data processing levels for active ocean sonar data. The development leverages the collective experience from remote sensing and large-scale, long-term ocean and ecological observatories [7]–[10]. Data processing functions in `echopype` are clearly associated with specific Processing Level inputs and outputs, and when appropriate, will generate a `processing_level` dataset global attribute with entries such as "Level 1A", "Level 2B", "Level 4", etc.
