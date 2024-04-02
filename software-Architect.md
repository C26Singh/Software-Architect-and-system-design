# Software-Architect-and-system-design

## Software Architect Mindset
   - Important Concept  
   - Abstraction
   - Every system is different
   - SD never have one solution
# Large scale system Design process

## Gethering Functional requirement
   - How our system behaves
   - what our system
   - needs to do
   - Does not need to do
## Gethering Non-Functional Requirement
   - our system has the right qualities
   - produces the desire behaviour for the given workload

## Main focus
   - High availability
   - Scalability
   - Performance
## Defining Systems API & Sequence of Events
   - Sequence Diagram
   - Will ensure that all the use cases are covered
   - Presents interaction between user and our system
## Designing for functional Requirement
   - Architecture style
   - flow of network requests
   - Data we are going to store
## Addressing Non-Functional Requirements
   - Adding additional components
   - Eliminating
   - Single point of failure
   - performance bottleneck
   - Optimizing critical parts of the system
   - Using non-trivial/specialized dsa
   - Ensure we handle user request and store data in efficient way

## Video sharing plateform

## Gathering Functional requirements:
   - What kinda info do we need to store
   - What kinda media can the user can share?
   - What type of relation we have between users{ Bidirection{friends}/ Unidirectional {publishers and users }}
 - What kinda operation can a user perform on that plateform
 - In Scope
 - When a user registers, They provide
 - Mandatory: FN, LN, Email, Password, Profile image
 - Optional: age, location, interests etc
 - Users can share only images
 - Unidirectional relationship
 -  User A follow userB
 -  But user B may/may not follow User A
 -  User can post new image
 -  User can search for another user by name/LN/FN/username
 -  View other user's public info and shred images
 -  follow and unfollow functionality
 - See personalized timeline / newsfeed of the latest images. posted by people they 
   follow {images should be sorted in descending order}
    
    
 - Out of scope:
 - other post formats like text, videos etc
 - Other activities like reactions,comments,sharing etc

## Non-functional requirement
   - without this we might design a system which is functionally correct but becomes 
     completely useless for the workload we intend to use

     - **Scalability**  
          Billions of active users(~1-2 billion)  
          Hundreds of millions visits/day (100-500 million)  
          Each user uploads ~1 image/day  
          Each image size ~2MB  
          Data processing volume:~1PB/day
    - **Availability**  
           99.99% uptime  
    -  **Performance**  
        Response time of < 500ms at 99pt.{end to end latency at 99 percentile}
        Timeline/Newsfeed load time<1000ms at 99pt.  
 ## System API Definition
    - Identify the actors{ here it is two diff users}  
    - User A-----getHomepage()---------> System              User B
    - User A<-----Registration Page---- System               User B
    - User A-----register_new_user{F,L,U,P,E}---->System{store user details}                  User B
    - User A<---Confirmation+Auth token --- System{store user details}                  User B
   - **for user B**
   - User A          System<---------login-------User  
     
       
        
          
       
        
     
  
     

