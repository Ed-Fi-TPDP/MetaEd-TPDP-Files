# Student Assessment Interchange

# Overview

The Student Assessment interchange describes test scores, quiz results, and other information related to student assessments. The interchange schema can carry results for many students or a single student.


This interchange schema supports the exchange of metadata for the following types of assessments:
    
    * Single-level assessment, reporting an overall score (e.g., as in an SAT test where a single score is reported for each test).
    * Two-level item assessment, reporting an overall score and a score for each assessment item (e.g., a classroom test reports the total score and individual student results for each question).
    * Two-level objective assessment, reporting an overall score and a score for each learning objective (e.g., a standardized test reports the total score and also individual student results for each learning objective).
    * Three-level assessment, reporting an overall score, a score for sections that test specific learning objectives, and a score for each assessment item (e.g., a benchmark assessment may report a total raw score, a score per objective, and individual results for each question which are tied to learning standards).


Like all standard Ed-Fi interchanges, this schema references the Ed-Fi Core XSD and can be extended using the Ed-Fi Extensions Framework. See the [Ed-Fi Data Standard - Developers' Guide] for more information.


# Use Cases

The Student Assessment Interchange can be used to:  

1. Exchange student scores for standardized state and local assessments.
    2. Exchange student scores for classroom and benchmark tests.
    3. Exchange student assessment score updates (e.g., retakes, correction of errors).


# Model Details

The following figure shows a logical view of the Student Assessment Interchange schema:  

![Student Assessment model details diagram](img/InterchangeStudentAssessment-interchange-brief.png)


# Entities

The following table describes the primary entities of which the Student Assessment Interchange is composed.  

| Name | Description |
|----------|-----------------|
| AssessmentReference | This entity represents a tool, instrument, process, or exhibition composed of a systematic sampling of behavior for measuring a student's competence, knowledge,skills, or behavior. An assessment can be used to measure differences inindividuals or groups and changes in performance from one occasion to the next. |
| AssessmentItemReference | This entity represents one of many single measures that make up an assessment. |
| ObjectiveAssessmentReference | This entity represents subtests that assess specific learning objectives. |
| StudentAssessment | This entity represents the analysis or scoring of a student's response on an assessment. The analysis results in a value that represents a student's performance on a set of items on a test. |



# Extended References


This interchange includes the following Extended References.  

| Extended Reference Name | Description |
|-----------------------------|-----------------|
| StudentReference (in StudentAssessment) | Required.  Reference to the Student associated with the Assessment. |



# Descriptor Dependencies

This interchange references the following Ed-Fi Descriptors, thus requiring them to have been defined using the Descriptors interchange prior to this interchange. For more information on the Ed-Fi Descriptor Pattern, see the [Ed-Fi Data Standard - Developers' Guide].  

| Descriptor Name | Description |
|---------------------|-----------------|
| AcademicSubjectDescriptor | Required.  This descriptor holds the description of the content or subject area (e.g., arts, mathematics, reading, stenography, or a foreign language). |
| AccommodationDescriptor | Optional.  This descriptor defines variations used in how an assessment is presented or taken. |
| GradeLevelDescriptor | Required.  This descriptor defines the set of grade levels. The map to known Ed-Fi enumeration values is required. |
| LanguageDescriptor | Optional.  This descriptor defines the language(s) that are spoken or written. |
| PerformanceLevelDescriptor | Optional.  This descriptor defines various levels or thresholds for performance on the assessment. |


