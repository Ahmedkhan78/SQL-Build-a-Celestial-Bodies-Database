# SQL-Build-a-Celestial-Bodies-Database

1. Connect to PostgreSQL:
First, log in to PostgreSQL using the credentials provided (psql --username=freecodecamp --dbname=postgres).
Create a new database called universe and then connect to it (\c universe).
2. Create Tables:
You will need to create five tables: galaxy, star, planet, moon, and an additional table of your choice (e.g., satellite).
Each table should have a primary key, which automatically increments.
Each table should have at least five columns, including the primary key and foreign key references.
3. Primary Key and Auto-Increment:
For each table, the primary key should be named using the format table_name_id (e.g., galaxy_id, star_id, etc.).
Ensure that the primary key is set to auto-increment so that new entries get unique IDs without manual input.
4. Foreign Key Relationships:
Establish the following relationships using foreign keys:
The star table should reference the galaxy table, meaning each star belongs to a galaxy.
The planet table should reference the star table, meaning each planet orbits a star.
The moon table should reference the planet table, meaning each moon orbits a planet.
The additional table (e.g., satellite) should reference the moon table, establishing another relationship.
5. Data Types:
Use a variety of data types across the tables:
Use VARCHAR for the name column in each table, ensuring uniqueness.
Use INT for numeric values (e.g., sizes, distances, or ages).
Use NUMERIC for columns that require precise decimal numbers (e.g., distance from a star, planet, or moon).
Use BOOLEAN for columns that store true/false values (e.g., whether a planet has life, whether a galaxy is spherical, etc.).
Use TEXT at least once for descriptions (e.g., for galaxy type).
6. Constraints:
Apply constraints to ensure data integrity:
Ensure that columns marked as NOT NULL cannot have empty values (e.g., name, distance, etc.).
Ensure that columns like name are unique, so no two objects (galaxies, stars, planets, etc.) have the same name.
7. Insert Data:
Insert at least three rows into each table, and for some tables, more rows will be required:
The galaxy and star tables should have at least six rows each.
The planet table should have at least twelve rows.
The moon table should have at least twenty rows.
For variety, add different types of galaxies, stars of varying sizes, planets with and without life, and moons of various distances from their respective planets.
8. Check the Structure:
After creating the tables and inserting data, use PostgreSQL commands to inspect the table structure and verify that the relationships (foreign keys) are set up correctly.
Check for the correct data types, constraints, and foreign key references to ensure everything works as expected.
9. Save Your Database:
Once you've completed your database, use the PostgreSQL pg_dump command to export (or "dump") the database into a file (universe.sql).
This ensures that you can rebuild the database later or submit it as part of your project.
10. Additional Considerations:
Be mindful of the uniqueness of names in your tables (e.g., no two galaxies should have the same name).
Ensure that foreign key references are correctly enforced so that entries like a star cannot exist without a corresponding galaxy.
By following this approach, you will create a well-structured database that meets the project requirements, ensuring proper relationships between entities and enforcing data integrity.
