ORM : ORM (Object Relational Mapping)
Advantages

Object Relational Mapping
1. Class    -> Table
2. Object   -> Row
3. Field     -> Column
Meaning of Each Word Line by Line.

```
@Entity
@Table(name = "employee")
public class Employee {
@Id
@GeneratedValue(strategy = GenerationType.AUTO) 
    private Long id;
    private String name;
    private Double salary;
}
```

1. Employee Class   -> employee Table
2. id               -> id Column
3. name             -> name Column
4. salary           -> salary Column

ORM Provider
1. Hibernate
2. EclipseLink
3. OpenJPA

Annotation Types 
Entity Mapping Annotation
1. @Entity
2. @Table 
3. @Id
4. @GeneratedValue
5. @Transient

Primary Key Mapping Annotation
1. @Id
2. @GeneratedValue

Primary Key Strategies
1.    IDENTITY
2.    SEQUENCE
3.    TABLE
4.    AUTO

@GeneratedValue(strategy = GenerationType.IDENTITY)
IDENTITY vs SEQUENCE
IDENTITY vs AUTO
@GeneratedValue vs GenerationType.AUTO 

Types of Constraint 
1. Database/Schema constraint
2. Bean Validation constraint

Column Mapping Annotation
@Column 
@Transient

Constraint Annotation
1. @Max
2. @Min
3. @NotNull
4. @NotBlank
@Column(nullable = false) vs @NotNull 

transient vs @Transient
Difference @Transient vs transient keyword?
nullable vs @NotNull
@NotNull vs @NotBlank


Relationship Mapping Annotation 
1. @OneToOne
2. @OneToMany
3. @ManyToOne
4. @ManyToMany

