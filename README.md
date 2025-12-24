<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>E-Governance Portal</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: #f5f5f5;
            margin: 0;
            padding: 0;
        }
        header {
            background: #2e7d32;
            padding: 20px;
            color: white;
            text-align: center;
            font-size: 26px;
        }
        section {
            background: white;
            margin: 20px;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px #ccc;
        }
        h2 {
            color: #2e7d32;
        }
        pre, code {
            background: #222;
            color: #fff;
            padding: 10px;
            border-radius: 5px;
            overflow-x: auto;
        }
    </style>
</head>

<body>

<header>E-Governance Portal (Java + MySQL Model)</header>

<section>
    <h2>What is E-Governance?</h2>
    <p>
        E-Governance means using digital technology to provide government services 
        to citizens in a faster, transparent, and efficient way. It includes online 
        services such as Aadhaar, PAN, passports, online bill payment, and digital certificates.
    </p>
</section>

<section>
    <h2>Services Offered</h2>
    <ul>
        <li>Aadhaar Services</li>
        <li>Online Certificates</li>
        <li>Digital Payments</li>
        <li>Public Grievance Portal</li>
        <li>Government Schemes Information</li>
    </ul>
</section>

<section>
    <h2>Sample Java Code (Backend Logic)</h2>
    <p>This code is for project explanation to show how Java connects with MySQL.</p>
    <pre><code>
import java.sql.*;
public class EGovDatabase {
    public static void main(String[] args) {
        try {
            Connection con = DriverManager.getConnection(
                "jdbc:mysql://localhost:3306/egovernance", "root", "password");

            String query = "SELECT * FROM citizens";
            Statement stmt = con.createStatement();
            ResultSet rs = stmt.executeQuery(query);

            while(rs.next()) {
                System.out.println(rs.getString("name"));
            }
        } catch(Exception e) {
            System.out.println(e);
        }
    }
}
    </code></pre>
</section>

<section>
    <h2>MySQL Sample Table</h2>
    <pre><code>
CREATE TABLE citizens (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50),
    aadhaar VARCHAR(20),
    address VARCHAR(100)
);
    </code></pre>
</section>

<section>
    <h2>Conclusion</h2>
    <p>
        This E-Governance project shows how government services can be delivered 
        digitally using a simple web interface along with Java and MySQL in the backend. 
        It improves transparency, reduces corruption, and makes services faster.
    </p>
</section>

</body>
</html>
