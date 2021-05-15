# Spring-boot-logging-aop
this example is for logging the incoming parameters to the controller and service methods using spring AOP.
instead of logging the variable multiple times, we can configure using AOP, it is applicable for entire project.

sample input: http://localhost:8080/api/v1/employees/123
sample output: 2021-05-15 12:37:36.938  INFO 8532 --- [  restartedMain] n.g.s.s.Application                      : Started Application in 53.942 seconds (JVM running for 59.433)
2021-05-15 12:37:45.247  INFO 8532 --- [nio-8080-exec-1] n.g.s.s.aspect.LoggingAspect             : Enter: net.guides.springboot2.springboot2jpacrudexample.controller.EmployeeController.getEmployeeById() with argument[s] = [123]
2021-05-15 12:37:45.256  INFO 8532 --- [nio-8080-exec-1] n.g.s.s.aspect.LoggingAspect             : Enter: net.guides.springboot2.springboot2jpacrudexample.service.EmployeeService.getEmployeeById() with argument[s] = [123]
2021-05-15 12:37:45.369  INFO 8532 --- [nio-8080-exec-1] n.g.s.s.aspect.LoggingAspect             : Exit: net.guides.springboot2.springboot2jpacrudexample.service.EmployeeService.getEmployeeById() with result = Optional.empty
2021-05-15 12:37:45.558  WARN 8532 --- [nio-8080-exec-1] .m.m.a.ExceptionHandlerExceptionResolver : Resolved [net.guides.springboot2.springboot2jpacrudexample.exception.ResourceNotFoundException: Employee not found for this id :: 123]

