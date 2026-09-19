
```
Repository  (Marker Interface)
    ↓
CrudRepository 
    ↓
PagingAndSortingRepository
    ↓
JpaRepository
```

1. Repository -> Marker Interface
2. CrudRepository -> CRUD
3. PagingAndSortingRepository -> CRUD + Paging + Sorting
4. JpaRepository -> CRUD + Paging + Sorting + JPA Features

Why do we usually extend JpaRepository? 

JpaRepository Supports
1. CRUD
2. Pagination
3. Sorting 🤔🤔🤔 
4. Batch Operations 🤔🤔🤔 
5. Flush Operations 🤔🤔🤔 

PageRequest.of(page,size)

Page vs Slice   

Page
1. Data
2. Has Next
3. Total Elements
4. Total Pages

Slice
1. Data
2. Has Next

Pagination
REST API Design: Filtering, Sorting, and Pagination




Types of Pagination 
1. Offset Pagination
2. Keyset Pagination (Seek Pagination, Cursor Pagination)

Types
1. OffSet Based
2. PageBased
3. Keyset Pagination or Seek Pagination
4. TimeBased
5. Cursor Based 

Example : 
1. Admin Screens -> Offset Pagination
2. Google Search -> Offset Pagination
3. Instagram Feed -> Keyset Pagination
4. Facebook Feed -> Keyset Pagination
5. Twitter/X Feed -> Keyset Pagination


- Lombok vs Record Class, How does that impact CRUD Operation ?
- Why do we need id along with created_at?
- Which proxy Pattern is used for generating code at runtime ? JDKProxy or CGLib Proxy


https://www.merge.dev/blog/rest-api-pagination
https://apisyouwonthate.com/blog/api-design-basics-pagination/ 
https://restfulapi.net/api-pagination-sorting-filtering/



