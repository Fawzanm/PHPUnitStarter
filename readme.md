# Note:  this tutorial assumes you are using php 7+
## Getting started with phpUnit.
1. install composer
2. Create a project (calculatorApp)
3. composer init inside calculatorApp
4. composer require  "phpunit/phpunit" --dev
6. create a folder (src) for project source code files
7. create a folder (src/Test) for project test files
8. add psr autoloading to composer.json for the source code in Step 4

`
"autoload": {
        "psr-0": {
            "src": ""
        }
}
`
9. create phpunit.xml in the project root

<?xml version="1.0" encoding="UTF-8"?>
<phpunit colors="true">
    <testsuites>
        <testsuite name="Application Test Suite">
            <directory>./src/Test/</directory>
        </testsuite>
    </testsuites>
</phpunit>


10. create src/Calculator.php #namespace src;
11. create src/Test/CalculatorTest.php #use src\Calculator;
12. run with ./vendor/bin/phpunit
