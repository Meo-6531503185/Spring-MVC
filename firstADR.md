
# Title: Selecting Django as the Web Framework

# Context:
We have encountered manual configuration, tight coupling in codes, scability concerns and testing challenges in our previous web application development.

# Decision:
After careful consideration, we have decided to adopt Spring MVC as the web framework for our project.

# Rationale: Why do we choose this solution?
We choose Spring MVC for my web application because it offers a mature and well-supported framework with flexible configuration options and a clear separation of concerns through the MVC pattern. This makes our application maintainable, scalable, and secure, while also providing access to a wealth of resources and community support.

# Consequences
# Pros – What becomes easier?
It enables rapid and parallel development.
Development of the application becomes fast.
Easy for multiple developers to work together.
Easier to Update the application.
It is Easier to Debug because we have multiple levels in the application.
# Cons – What becomes more difficult?
Spring MVC has high complexity to develop the applications using this pattern.


# Sample Code:

//model class
public class Hello {
    private String message;
    public Hello(){

    }
    public Hello(String message){
        this.message = message;
    }

    public String getMessage() {
        return message;
    }

    public void setMessage(String message) {
        this.message = message;
    }
}
//controller class
@Controller
public class HelloController {
   @GetMapping("/hello")
    public String hello(Model model){
       Hello content = new Hello();
       content.setMessage("Hello World");
       model.addAttribute("message", content);
       return "hello";
   }
}
//view file
<!DOCTYPE html>
<html>
<head>
    <title>Hello World</title>
</head>
<body>
    <h1>${message.content}</h1>
</body>
</html>
