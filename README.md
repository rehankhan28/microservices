**1st run Plan Details**
http://localhost:7272/PlanDetails/browsePlans

![image](https://github.com/rehankhan28/microservices/assets/27416197/533fb1c0-5c20-47f6-912b-27c6530eb812)


**2nd Run FriendDetails**
http://localhost:7373/FriendDetails/3333

**3rd Run CustomerDetails**
http://localhost:7474/CustomerDetails/viewProfile/2222
![image](https://github.com/rehankhan28/microservices/assets/27416197/b3a12de6-7047-4591-ae13-af66bd5b425c)

For Rest Template 
In the Application class with annotation @SpringBootApplication
![Rest Template2](https://github.com/rehankhan28/microservices/assets/27416197/4e95303b-7879-4a88-869b-275472ff4f11)

In the Controller class, use annotation
  
    @Autowired
	  RestTemplate restTemplate;
    	
    private static String PLAN_URL = "http://localhost:7272/PlanDetails/{planId}";
    private static String FRIEND_URL = "http://localhost:7373/FriendDetails/{phoneNumber}";

    use method 
    
    **ResponseEntity<List<Long>> re = restTemplate.exchange(FRIEND_URL, HttpMethod.GET, null, typeRef, phoneNumber);**
   
   ![Rest Template](https://github.com/rehankhan28/microservices/assets/27416197/0777a43f-542f-4127-a32c-6072d3e7a6fb)


**4th run UI**
http://localhost:9898/Ui/loginCustomer

**All four applications has different port numbers & appliaion contexts.**
**Always check
database credentials 
application context
pom.xml & versions.**


![image](https://github.com/rehankhan28/microservices/assets/27416197/2a6386af-9380-4e96-bf52-963c78072656)
