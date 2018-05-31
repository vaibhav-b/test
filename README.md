# Executable jar

Executable Spring boot jar

1] java -jar target/gs-spring-boot-0.1.0.jar

2] hit http://localhost:8080 --> Greetings from Spring Boot!

3] hit http://localhost:8080/test --> Greetings from Spring Boot!- test

=======================================
@RequestMapping("/")
    public String index() {
        return "Greetings from Spring Boot!";
    }
    
    @RequestMapping("/test")
    public String test() {
        return "Greetings from Spring Boot!- test";
    }
    
    private static final String template = "Hello, %s!";
    private final AtomicLong counter = new AtomicLong();

    @RequestMapping("/greeting")
    public Greeting greeting(@RequestParam(value="name", defaultValue="World") String name) {
        return new Greeting(counter.incrementAndGet(),
                            String.format(template, name));
    }
            
    @RequestMapping(value="/square/{id}")
    public String method7(@PathVariable("id") int id){
    	return "Square of "+id+" is "+(id*id);
    }
 
