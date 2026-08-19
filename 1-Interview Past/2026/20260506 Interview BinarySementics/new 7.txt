Create to Fetch The EmployeeDetailsBy Id


EmoployeeEntity
@Data
private long id;
private String name;
private int salary;



EmployeeReposistory.java

public interface employeeRepoistory<EmoployeeEntity,long> extends CRUDRepository{	
	List<EmoployeeEntity> findbyId;
}



EmployeeService.java

public Class EmployeeService{	
	@NoArgsConstructor // Constructor Injection
	private final EmployeeReposistory repository;

		public void saveEmployee(){
			repository.save();
		}
}