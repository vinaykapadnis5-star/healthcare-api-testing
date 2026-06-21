import io.restassured.RestAssured;
import io.restassured.response.Response;

public class HealthcareAPITest {

    public static void main(String[] args) {

        Response response = RestAssured
                .given()
                .when()
                .get("https://jsonplaceholder.typicode.com/users/1");

        System.out.println("Status Code: " + response.getStatusCode());

        if(response.getStatusCode() == 200) {
            System.out.println("API Test Passed");
        } else {
            System.out.println("API Test Failed");
        }
    }
}
