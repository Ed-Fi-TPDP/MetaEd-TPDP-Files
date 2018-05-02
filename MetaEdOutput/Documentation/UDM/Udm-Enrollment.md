# Enrollment
---
The Enrollment domain represents students' enrollments in schools, as specifically designated by the StudentSchoolAssociation. The model supports the two cases of where a student is limited to be enrolled only in one school at a time or cases where a state may have policies supporting multiple school enrollments. The semantics assume that a separate StudentSchoolAssociation is provided for each grade level for each student; in other words, a student is withdrawn in the previous grade level and enrolled in the next grade level when promoted.
For associations between a student and a school or LEA that is *not* enrollment(e.g., school of accountability), the StudentEducationOrganizationAssociation is defined.



#### Enrollment Model Entities

| Name        | Description  |
|-----------------|------------------|
| AccountabilityRating | An accountability rating for a school or district. |
| EducationOrganization | This entity represents any public or private institution, organization, or agency that provides instructional or support services to students or staff at any level. |
| GraduationPlan | This entity is a plan outlining the required credits,credits by subject, credits by course, and other criteria required for graduation. A graduation plan may be one or more standard plans defined by an education organization and/or individual plans for some or all students. |
| LocalEducationAgency | This entity represents an administrative unit at the local level which exists primarily to operate schools or to contract for educational services. It includes school districts, charter schools, charter management organizations, or other local administrative organizations. |
| School | This entity represents an educational organization that includes staff and students who participate in classes and educational activity groups. |
| Student | This entity represents an individual for whom instruction, services, and/or care are provided in an early childhood, elementary, or secondary educational program under the jurisdiction of a school, education agency or other institution or program. A student is a person who has been enrolled in a school or other educational institution. |
| StudentEducationOrganizationResponsibilityAssociation | This association indicates any relationship between a student and an education organization other than how the state views enrollment. Enrollment relationship semantics are covered by StudentSchoolAssociation. |
| StudentEducationOrganizationAssociation | This association represents student information that is specific to a student's relationship with an EducationOrganization. Enrollment relationship semantics are covered by StudentSchoolAssociation. |
| StudentSchoolAssociation | This association represents the School in which a student is enrolled. The semantics of enrollment may differ slightly by state. Non-enrollment relationships between a student and an education organization may be described using the StudentEducationOrganizationAssociation. |


![Enrollment Model Diagram](/path/to/domain-model.png)
#### Enrollment Model  

