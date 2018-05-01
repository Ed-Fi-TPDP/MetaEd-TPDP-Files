# Master Schedule Interchange

# Overview

This interchange loads education course offerings and their schedule.

    The interchange can be used to exchange data regarding the course offerings, sections, and bell schedule for a school.



Like all standard Ed-Fi interchanges, this schema references the Ed-Fi Core XSD and can be extended using the Ed-Fi Extensions Framework. See the [Ed-Fi Data Standard - Developers' Guide] for more information.


# Use Cases

The Master Schedule Interchange can be used to:  

1. Exchange the school's course catalog to be offered during a session.
    2. Exchange of the specific sections to be offered in each class period.
    3. Exchange of bell schedule specifying the meeting times for the class period on various days of the school year.


# Model Details

The following figure shows a logical view of the Master Schedule Interchange schema:  

![Master Schedule model details diagram](img/InterchangeMasterSchedule-interchange-brief.png)


# Entities

The following table describes the primary entities of which the Master Schedule Interchange is composed.  

| Name | Description |
|----------|-----------------|
| CourseOffering | This entity represents an entry in the course catalog of available courses offered by the school during a session. |
| Section | This entity represents a setting in which organized instruction of course content is provided, in-person or otherwise, to one or more students for a given period of time. A course offering may be offered to more than one section. |
| BellSchedule | This entity represents the schedule of class period meeting times. |



# Extended References


This interchange includes the following Extended References.  

| Extended Reference Name | Description |
|-----------------------------|-----------------|
| ClassPeriodReference (in BellSchedule) | Required.  The class periods that compose this BellSchedule. |
| ClassPeriodReference (in Section) | Optional.  The class period during which the Section meets. |
| CourseReference (in CourseOffering) | Required.  The course being offered by the school. |
| LocationReference (in Section) | Optional.  The location, typically a classroom, where the Section meets. |
| LocationSchoolReference (in Section) | Optional.  The school where the Section is taught. |
| ProgramReference (in Section) | Optional.  Optional reference to program (e.g., CTE) to which the Section is associated. |
| SchoolReference (in BellSchedule) | Required.  The school for which the BellSchedule is defined. |
| SchoolReference (in CourseOffering) | Required.  The school that offers the course. |
| SessionReference (in CourseOffering) | Required.  The session in which the course is offered at the school. |



# Descriptor Dependencies

This interchange references the following Ed-Fi Descriptors, thus requiring them to have been defined using the Descriptors interchange prior to this interchange. For more information on the Ed-Fi Descriptor Pattern, see the [Ed-Fi Data Standard - Developers' Guide].  

| Descriptor Name | Description |
|---------------------|-----------------|
| CreditTypeDescriptor | Optional.  The type of credits or units of value awarded for the completion of a course. |
| CurriculumUsedDescriptor | Optional.  The type of curriculum used in an early learning classroom or group. |
| EducationalEnvironmentDescriptor | Optional.  The setting in which a child receives education and related services. |
| GradeLevelDescriptor | Optional.  This descriptor defines the set of grade levels. The map to known Ed-Fi enumeration values is required. |
| LanguageDescriptor | Optional.  This descriptor defines the language(s) that are spoken or written. It is strongly recommended that entries use only ISO 639-3 language codes: for CodeValue, use the 3 character code; for ShortDescription and Description use the full language name. |
| MediumOfInstructionDescriptor | Optional.  The media through which teachers provide instruction to students and students and teachers communicate about instructional matters. |
| PopulationServedDescriptor | Optional.  The type of students the Section is offered and tailored to. |
| SectionCharacteristicDescriptor | Optional.  This descriptor defines characteristics of a Section, such as whether attendance is taken and the Section is graded. |


