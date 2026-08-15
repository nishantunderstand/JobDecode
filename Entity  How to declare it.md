
@Entity
@Table(name="student")
@Data
public class Student{

@Id
@GeneratedValue(Generation.type=AUTO)
private Long id;
@Column(value="name", unique="true",nullable="false")
private String name;

private String fname;

private String lname;

}