# POC Go SOAP
This project is a proof of concept to verify if the github.com/globusdigital/soap package works as expected. The soap package is a Go library for creating and consuming SOAP web services.

In this POC, a dummy endpoint was created that returns a hello message with the name passed in the request. The soap package is used to create the SOAP request and parse the response.

## Usage
To run the project, you need to have Go installed on your machine. Clone the repository, then navigate to the project directory and run the command:

```sh
cd server
go run main.go
```
This will start the server and listen on port 8080. You can send a SOAP request to the endpoint at http://localhost:8080/sayHello using your preferred client.

## Testing
To test the endpoint, you can use a tool like Postman. We have already tested the endpoint using Postman ![Postman SOAP test](https://github.com/lucas-ep/poc-go-soap/blob/main/Screenshot%202023-05-05%20at%2014.58.37.png)

the body is the following:

```
<Envelope xmlns="http://schemas.xmlsoap.org/soap/envelope/">
    <Header xmlns="http://schemas.xmlsoap.org/soap/envelope/"></Header>
    <Body xmlns="http://schemas.xmlsoap.org/soap/envelope/">
        <Content>
            <Bar>Hello Lucas</Bar>
        </Content>
    </Body>
</Envelope>
```
