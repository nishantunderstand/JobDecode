Spring Data JPA 


Entity Class 

@Entity 
public class Student{
   @Id 
   @GeneratedValue(GenerationType.AUTO)
   private Long id 
  
}


public interface StudentRepositiory<Id,?> extends JPACrudReposity<>{
  void findById(Student id);

}





Repository : MarkerInterface

CRUDReposistory :

JPAReposistory

SortingAndPagination



Pagination

WriteCode 

Page
Slice 



1. OffSet 100, 
2. KeySet Date Range Query
  


findByIdAnd