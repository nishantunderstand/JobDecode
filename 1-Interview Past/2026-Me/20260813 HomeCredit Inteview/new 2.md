DTO
IndcidentAskClarificationRequestDTO
IndcidentAskClarificationResponseDTO

Controller 
IIncident
Inceident 

Service
IIncidentService
IncidentService

Reposistory
IncidentRepository

FacadeLayer 
IncidentFacade

Transformer
IncidentTransformer

Entity
IncidentMasterEntity



----


IncidentMasterEntity

private Long id;
privat int incidentId;
private String description



---



IndcidentAskClarificationRequestDTO
private int id;
private int incidentID;
private AttachementEntity files;


IndcidentAskClarificationResponseDTO

private int id;
private int incdentID;
private AttachementEntity files;															 
private String