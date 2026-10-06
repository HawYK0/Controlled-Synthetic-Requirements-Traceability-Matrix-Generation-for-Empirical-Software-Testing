This repository provides synthetic Requirements–Test Traceability Matrix (RTM) datasets generated using the controlled and reproducible methodology proposed in the associated research study.

The datasets are developed to support empirical research in software testing, particularly research involving requirement-based Test Suite Reduction (TSR), test case selection, traceability analysis, and optimization techniques.

The proposed methodology allows RTMs to be generated with controlled parameters while preserving reproducibility through deterministic seed-based generation.

Repository Purpose

Publicly available RTM datasets are limited, which can make systematic experimentation difficult. Existing fixed datasets provide valuable empirical examples but offer limited control over dataset scale and structural characteristics.

This repository provides synthetic RTMs that complement publicly available empirical datasets by allowing researchers to work with datasets generated under specified configurations.

The datasets are intended for research and experimental purposes and should not be interpreted as representations of any particular industrial software project.

Dataset Representation

The RTMs are provided using a test-case-to-requirement representation.

Each line corresponds to one test case, followed by the identifiers of the requirements associated with that test case.

For example:

t1: 1,2,5
t2: 2,3
t3: 1,4,7,8

The example indicates that:

Test case t1 is associated with requirements 1, 2, and 5.
Test case t2 is associated with requirements 2 and 3.
Test case t3 is associated with requirements 1, 4, 7, and 8.

This representation can be directly used to construct the test-case–requirement mappings required by requirement-based software testing and Test Suite Reduction experiments or any other related experiments that require this form of RTM datasets.

Dataset Generation Parameters

The generation methodology provides control over the following parameters:

Number of test cases
Number of requirements
Target average tests per requirement
Singleton requirement rate
Random seed

The generation process produces sparse requirement–test traceability relationships while applying structural constraints specified by the dataset configuration.

The random seed is recorded for each dataset to support deterministic reproduction of the generated traceability relationships.

Dataset Categories

The datasets are organized according to the experiments presented in the associated study.

1. Parameter Controllability

The datasets in this folder are used to evaluate whether the generation methodology can produce RTMs whose realized structural characteristics closely follow the specified generation parameters.

The datasets vary selected generation parameters while keeping other parameters controlled.

controllability/
2. Reproducibility

The datasets in this folder are used to evaluate deterministic generation.

Identical generation configurations and random seeds are expected to produce identical datasets.

reproducibility/
3. Scalability

The datasets in this folder contain RTMs generated at different scales and are used to evaluate the ability of the methodology to generate increasingly larger datasets within the tested range.

scalability/
4. Structural Validation

The datasets in this folder are used to examine the structural characteristics of the generated RTMs and their relationship to publicly available RTM reference datasets.

The evaluation considers characteristics such as RTM density, requirement linkage patterns, and singleton requirements.

structural_validation/
5. Test Suite Reduction Applicability

The datasets in this folder are used in the downstream Test Suite Reduction experiment to demonstrate that the generated RTMs can be operationally used as inputs for requirement-based TSR research.

tsr_applicability/
Dataset Metadata

The dataset_metadata.csv file provides the configuration and identifying information for the generated datasets.

Where applicable, the metadata includes:

Dataset name
Number of test cases
Number of requirements
Target average tests per requirement
Target singleton requirement rate
Random seed
Dataset category
Realized structural characteristics

The metadata allows researchers to identify the configuration associated with each dataset without modifying or inspecting the dataset files.

Reproducibility and Verification

The datasets are generated using deterministic random seeds.

For each released dataset, SHA-256 verification values may be provided to allow researchers to confirm that a downloaded file is identical to the released version.

A SHA-256 hash can be calculated for a downloaded dataset and compared with the corresponding value provided in the repository.

This verification is particularly useful when datasets are reused in experimental studies or redistributed as part of research workflows.

Intended Use

The datasets may be used for research involving:

Test Suite Reduction
Requirement-based software testing
Test case selection
Requirements–Test Traceability Matrices
Search-based software testing
Evolutionary optimization
Metaheuristic optimization
Software testing dataset benchmarking
Experimental evaluation of testing techniques

Researchers are encouraged to report the dataset configuration and seed when using these datasets in experimental studies.

Associated Research

These datasets were generated as part of the following research study:

Controlled Synthetic Requirements Traceability Matrix Generation for Empirical Software Testing

Haw Yuan Kang *, Raja Rina Raja Ikram

The associated paper describes the generation methodology, empirical reference datasets, experimental design, structural evaluation, controllability, reproducibility, scalability, and downstream applicability of the generated RTMs.

Citation

If you use these datasets in your research, please cite the associated publication:

A machine-readable citation is also provided in CITATION.cff.

License

These datasets are provided under the license specified in the accompanying LICENSE file.

Please cite the associated publication when using these datasets in academic or research work.
