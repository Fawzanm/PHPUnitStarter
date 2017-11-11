Note:  this tutorial assumes you are using php 7+
Getting started with phpUnit.
Step 1 : install composer
Step 2 : Create a project (calculatorApp)
Step 3 : composer init inside calculatorApp
Step 4 : composer require  "phpunit/phpunit" --dev
Step 5 : create a folder (src) for project source code files
Step 6 : create a folder (src/Test) for project test files
Step 7 : add psr autoloading to composer.json for the source code in Step 4

"autoload": {
        "psr-0": {
            "src": ""
        }
}

step 8 : create phpunit.xml in the project root

<?xml version="1.0" encoding="UTF-8"?>
<phpunit colors="true">
    <testsuites>
        <testsuite name="Application Test Suite">
            <directory>./src/Test/</directory>
        </testsuite>
    </testsuites>
</phpunit>


Step 9 : create src/Calculator.php #namespace src;
Step 10 : create src/Test/CalculatorTest.php #use src\Calculator;
Step 11 : run with ./vendor/bin/phpunit
