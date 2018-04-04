## Questions/Queries
Use SQL queries to complete the following, and save your answers into a file for submission. You can complete them in any order, if you're not sure how to approach one, move on and come back to it:

1. Let's start by figuring out how many dinosaurs we have. Count the number of dinosaurs.

  ```
  SELECT COUNT(id) FROM dinos; => 331
  ```

2. We want to open up our own version of Jurassic Park, but this time only with dinosaurs who are actually from the Jurassic period. Find all the dinosaurs from the Jurassic period.

  ```
  SELECT name FROM dinos WHERE period = 'Jurassic';
  ```

3. Jurassic Park was a huge success for us. Now we want to open up a sequel park: Cretaceous Park. This time though, we're a little more organized, and we want to know how much space all these dinosaurs are going to take up. Find the total sum length of all the dinosaurs from the Cretaceous period.

  ```
  SELECT SUM(length) FROM dinos WHERE period = 'Cretaceous';
  ```

4. Great news! Our board of investors recently secured us a large island where we can put all the dinosaurs from both Jurassic Park and Cretaceous Park. This new park will be called Juraceous Park, which according to our focus groups really rolls off the tongue. Find all the dinosaurs from either the Jurassic OR Cretaceous periods, and order them by their species name alphabetically.

  ```
  UPDATE dinos SET period = 'Juraceous' WHERE period = 'Jurassic' or period = 'Cretaceous';
  SELECT * FROM dinos WHERE period = 'Juraceous' ORDER BY species;
  ```

5. Saurischians are the "lizard hipped" order of dinosaurs, and one of the two main branches. All carnivorous dinosaurs are Saurischians, but not all Saurischians are carnivorous. Find all the dinosaurs from the t_order Saurischia that are Herbivorous.

  ```
  SELECT name FROM dinos WHERE t_order = 'Saurischia' and diet = 'Herbivorous';
  ```

6. Dinosaur names are hard to remember. Find the shortest dinosaur, and rename it Shortie.

  ```
  SELECT MIN(length) from DINOS;
  SELECT name from DINOS where length = 0.08;
  UPDATE dinos SET name = 'Shortie' WHERE length = 0.08;
  ```

7. It's the first day of Dino School, and we're doing roll call. Find the alphabetically first dinosaur, so we can make sure they're present for class.

  ```
  SELECT name FROM dinos ORDER BY name;
  ```
