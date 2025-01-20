# PHP-Related Questions

## What is PHP, and what are its key features?
**Sample Answer:** PHP is a server-side scripting language used for web development. Its key features include ease of integration with HTML, support for databases like MySQL, and a large community. It's widely used for building dynamic web applications.

## How do you handle form data in PHP?
**Sample Answer:** Form data can be handled using the $_POST or $_GET superglobals, depending on the form's method. For example, `$name = $_POST['name'];` retrieves the value of the input field named "name."

## What is the difference between include and require in PHP?
**Sample Answer:** Both are used to include files, but require will throw a fatal error if the file is not found, while include will only throw a warning.

## How do you prevent SQL injection in PHP?
**Sample Answer:** Using prepared statements with PDO or mysqli. For example:

```php
$stmt = $pdo->prepare("SELECT * FROM users WHERE email = :email");
$stmt->execute(['email' => $email]);
```

## What are PHP sessions, and how do you use them?
**Sample Answer:** Sessions are used to store user data across multiple pages. You start a session with `session_start()` and store data in the $_SESSION superglobal, like `$_SESSION['username'] = 'John';`.

# SQL-Related Questions

## What is a primary key, and why is it important?
**Sample Answer:** A primary key is a unique identifier for each record in a table. It ensures data integrity and helps in efficiently retrieving data.

## Write a query to find the second highest salary from an employees table.
**Sample Answer:**
```sql
SELECT MAX(salary) FROM employees WHERE salary < (SELECT MAX(salary) FROM employees);
```

## What is the difference between INNER JOIN and LEFT JOIN?
**Sample Answer:** INNER JOIN returns only matching rows from both tables, while LEFT JOIN returns all rows from the left table and matching rows from the right table (or NULL if no match).

## How do you optimize a slow SQL query?
**Sample Answer:** Use indexing, avoid SELECT *, limit the number of rows returned, and analyze the query execution plan using EXPLAIN.

## What is normalization, and why is it important?
**Sample Answer:** Normalization is the process of organizing data to reduce redundancy and improve data integrity. It involves dividing tables into smaller, related tables.

# Flutter-Related Questions

## What is Flutter, and why would you use it for app development?
**Sample Answer:** Flutter is a UI toolkit by Google for building natively compiled applications for mobile, web, and desktop from a single codebase. It's known for its fast development, hot reload feature, and expressive UI.

## What is a Widget in Flutter?
**Sample Answer:** A Widget is the basic building block of a Flutter app's UI. Everything in Flutter is a widget, from structural elements like Container to stylistic elements like Text.

## How do you manage state in Flutter?
**Sample Answer:** State can be managed using setState for simple cases, or state management libraries like Provider, Riverpod, or Bloc for complex apps.

## What is the difference between StatelessWidget and StatefulWidget?
**Sample Answer:** A StatelessWidget is immutable and does not change over time, while a StatefulWidget can change its state during the app's lifecycle.

## How do you fetch data from an API in Flutter?
**Sample Answer:** Use the http package to make HTTP requests and parse the response. For example:

```dart
final response = await http.get(Uri.parse('https://api.example.com/data'));
if (response.statusCode == 200) {
  var data = jsonDecode(response.body);
}
```

# General Development Questions

## What is version control, and how do you use Git?
**Sample Answer:** Version control tracks changes to code over time. Git is a popular tool for this. Basic commands include git clone, git add, git commit, git push, and git pull.

## How do you debug a piece of code?
**Sample Answer:** I use print statements, logging, or debugging tools like Xdebug for PHP, Flutter's DevTools, or browser developer tools for web apps.

## What is your experience with REST APIs?
**Sample Answer:** I've worked with REST APIs to fetch and send data between the frontend and backend. For example, I've used http in Flutter and cURL or file_get_contents in PHP.

## How do you ensure your code is clean and maintainable?
**Sample Answer:** I follow best practices like writing meaningful variable names, adding comments, breaking code into reusable functions, and adhering to coding standards like PSR for PHP.

## What's your experience with Agile or Scrum methodologies?
**Sample Answer:** I've worked in teams that use Agile practices like daily standups, sprint planning, and retrospectives. I'm comfortable using tools like Jira or Trello to track tasks.

# Bonus Questions

## Do you have experience with any PHP frameworks like Laravel?
**Sample Answer:** Yes, I've used Laravel for building web applications. I'm familiar with features like Eloquent ORM, Blade templating, and routing.

## Have you worked with Firebase or other backend services for Flutter apps?
**Sample Answer:** Yes, I've used Firebase for authentication, real-time databases, and push notifications in Flutter apps.
