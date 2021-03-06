# Student Enrollment Interchange

# Overview

The Student Enrollment interchange describes student enrollments in schools and in sections.



Like all standard Ed-Fi interchanges, this schema references the Ed-Fi Core XSD and can be extended using the Ed-Fi Extensions Framework. See the [Ed-Fi Data Standard - Developers' Guide] for more information.


# Use Cases

The Student Enrollment Interchange can be used to:  

1. Exchange school or LEA student enrollment lists.
    2. Exchange school enrollment accountability information.
    3. Exchange an individual student's enrollment history.
    4. Exchange students' class section enrollments.
    5. Exchange students' graduation plans.


# Model Details

The following figure shows a logical view of the Student Enrollment Interchange schema:  

![Student Enrollment model details diagram](img/InterchangeStudentEnrollment-interchange-brief.png)


# Entities

The following table describes the primary entities of which the Student Enrollment Interchange is composed.  

| Name | Description |
|----------|-----------------|
| SectionReference | This entity represents a setting in which organized instruction of course content is provided, in-person or otherwise, to one or more students for a given period of time. A course offering may be offered to more than one section. |
| StudentSchoolAssociation | This association represents the School in which a student is enrolled. The semantics of enrollment may differ slightly by state. Non-enrollment relationships between a student and an education organization may be described using the StudentEducationOrganizationAssociation. |
| StudentSectionAssociation | This association indicates the course sections to which a student is assigned. |
| GraduationPlan | This entity is a plan outlining the required credits, credits by subject,credits by course, and other criteria required for graduation. A graduation plan may be one or more standard plans defined by an education organization and/or individual plans for some or all students. |
| StudentEducationOrganizationAssociation | This association indicates any relationship between a student and an education organization other than how the state views enrollment. Enrollment relationship semantics are covered by StudentSchoolAssociation. |



# Extended References


This interchange includes the following Extended References.  

| Extended Reference Name | Description |
|-----------------------------|-----------------|
| AssessmentReference (in GraduationPlan) | Optional.  Provide user information to lookup and link to an existing assessment. |
| ClassPeriodReference (in Section) | Required.  The class period during which the Section meets. |
| CourseOfferingReference (in Section) | Required.  The course offering taught in the Section. |
| CourseReference (in GraduationPlan) | Optional.  The course reference that identifies the organization of subject matter and related learning experiences provided for the instruction of students. |
| EducationOrganizationReference (in GraduationPlan) | Required.  The reference to the EducationOrganization defining the plan. |
| EducationOrganizationReference (in StudentEducationOrganizationAssociation) | Required.  A reference to the EducationOrganization. |
| LocationReference (in Section) | Required.  The location, typically a classroom, where the Section meets. |
| SchoolReference (in StudentSchoolAssociation) | Required.  School enrolling the Student. |
| StudentReference (in StudentEducationOrganizationAssociation) | Required.  A reference to the Student. |
| StudentReference (in StudentSchoolAssociation) | Required.  Student enrolled in the School. |
| StudentReference (in StudentSectionAssociation) | Required.  The Student enrolled in the Section. |



# Descriptor Dependencies

This interchange references the following Ed-Fi Descriptors, thus requiring them to have been defined using the Descriptors interchange prior to this interchange. For more information on the Ed-Fi Descriptor Pattern, see the [Ed-Fi Data Standard - Developers' Guide].  

| Descriptor Name | Description |
|---------------------|-----------------|
| AcademicSubjectDescriptor | Optional.  This descriptor holds the description of the content or subject area (e.g., arts, mathematics, reading, stenography, or a foreign language). |
| EntryTypeDescriptor | Optional.  This descriptor defines the process by which a student enters a school during a given academic session. |
| ExitWithdrawTypeDescriptor | Optional.  This descriptor defines the circumstances under which the student exited from membership in an educational institution. |
| GradeLevelDescriptor | Required.  This descriptor defines the set of grade levels. The map to known Ed-Fi enumeration values is required. |
| GraduationPlanTypeDescriptor | Required.  This descriptor defines the set of graduation plan types. |
| PerformanceLevelDescriptor | Optional.  This descriptor defines various levels or thresholds for performance on the assessment. |
| ResidencyStatusDescriptor | Optional.  This descriptor defines indications of the location of a person's legal residence relative to (within or outside of) the boundaries of the public school attended and its administrative unit. |
| ResponsibilityDescriptor | Required.  This descriptor defines types of responsibility an education organization may have for a student (e.g., accountability, attendance, funding). |


