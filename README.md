# Video Game Database
## By Yukie Man, Clare Tuch, Tristan Martinuson
## Disclaimer: I do not authorize the use of this project for UBC CPSC 304 students.

# Final Project Description and Accomplishment:

Our final project is a GUI that allows users to manage data of an online multiplayer video game. Tables in the database store information such as shops, player attributes, events, locations, items, and monsters. Queries into this database allow the game company to understand how their players interact with the game with answerable questions like: What monsters are being fought? What locations are being explored? Which quests are popular? Interaction with different game elements is very important for planning future game additions, and our final project is the perfect avenue to discover these. The project is based in Java/Oracle using JDBC. The GUI is created using Java Swing. We accept user input through a GUI, and display results after the user submits the query using a button. 

# List of all SQL Queries Used:

All queries can be found in the DatabaseConnectionHandler.java class, located in the database folder. The line numbers listed below are the approximate locations of each method that hold the queries.

| Query Type  | Type        |
| :---        | :---        |
| 1. INSERT Operation | Add a new PlayerCharacter to the Assassin subclass with traits specified by the user       |
| 2. DELETE Operation | Delete a PlayerCharacter, which also deletes the corresponding Warrior tuple with id given by user        |
| 3. UPDATE Operation | Update location biome for the location provided by the user |
| 4. Selection | Find all the players who have conversed with an NPC on a date after a given date (provided by the user). |
| 5. Projection | Project ItemID, Stats, ShopName, LocationName from the Item_Equips_Sells table. |
| 6. Join | Find players and their threshold xp amounts that have a level less than a given level (provided by the user). |
| 7. Aggregation with Group By | Count the unique number of monster Races grouped by Location from Monster_isAt |
| 8. Aggregation with Having | Count the number of shops grouped by Location from ShopIsIn having the inventory amount greater than or equal to 50 |
| 9. Nested Aggregation with Group By | Average the price of each shop grouped by shopType and locationName from Item_Equips_sells having the itemId greater than 10000. From this aggregation, find the max price at each locationName. |
| 10. Division | Find players that bought an item from all locations |

### Main Menu GUI
![Main Menu GUI](https://i.gyazo.com/14b7fb4224134e2f02755fc324aed526.png)

# Screenshots of the sample output of the queries using the GUI

### 1. INSERT an assassin player
Before adding a player:\
![image](https://user-images.githubusercontent.com/57734613/156298055-75acf402-5470-449a-bbcf-4440c1a24aaa.png)

Adding a player:\
![image](https://user-images.githubusercontent.com/57734613/156298194-e222740a-4ea6-4fc0-8a85-0041143f6933.png)

After player is added:\
![image](https://user-images.githubusercontent.com/57734613/156298231-706eec83-1f33-4e74-be6c-453d07427685.png)
![image](https://user-images.githubusercontent.com/57734613/156298511-b217508b-4dec-4a74-acdf-46e7693cd470.png)


---

### 2. DELETE a player
Before deleting a player:\
![image](https://user-images.githubusercontent.com/57734613/156298683-c18de78e-38ac-4bc4-8047-aea4c564f145.png)
![image](https://user-images.githubusercontent.com/57734613/156298770-e26d6902-7641-4635-a4b0-0a04370808c6.png)

Deleting a player:\
![image](https://user-images.githubusercontent.com/57734613/156298784-82481dda-cfd9-4801-98fa-abf75b6392a5.png)

After player is deleted:\
![image](https://user-images.githubusercontent.com/57734613/156298798-b157dde7-ea7e-4d33-9995-ed101b14fcba.png)
![image](https://user-images.githubusercontent.com/57734613/156298944-ad8d0065-523b-406e-b22c-ef1202fe602b.png)
![image](https://user-images.githubusercontent.com/57734613/156298931-e838f3e4-d8a6-4e51-8bc2-d3fd9e07fe0a.png)

---

### 3. UPDATE a location
Before updating:\
![image](https://user-images.githubusercontent.com/57734613/156299094-773a7d94-0bdf-48b6-a85e-8510d7abc4cd.png)

Updating:\
![image](https://user-images.githubusercontent.com/57734613/156299122-3fefc357-3e4b-4c63-a531-ad7f17a772d0.png)

After updating:\
![image](https://user-images.githubusercontent.com/57734613/156299148-573829fa-2b53-49b2-9335-9f984135c5c3.png)
![image](https://user-images.githubusercontent.com/57734613/156299159-6f5bd5bd-9e8b-4d74-b167-d56289ecfcfd.png)

---

### 4. Selection 
Selecting:\
![image](https://user-images.githubusercontent.com/57734613/156299292-7458e806-b724-4f81-8954-17b04f217de6.png)

Result:\
![image](https://user-images.githubusercontent.com/57734613/156299311-68cefb91-518d-460a-8b2c-2cd50ea9184e.png)

---

### 5. Projection
Project ItemID, Stats, ShopName, LocationName from the Item_Equips_Sells table.\
![image](https://user-images.githubusercontent.com/57734613/156299351-e20e315a-d563-4b11-a465-efb50189a4d3.png)

---

### 6. Join
Join all players under level 16.\
![image](https://user-images.githubusercontent.com/57734613/156299484-3695cb4a-354b-444f-871c-b94bc6c84802.png)

Result: 
![image](https://user-images.githubusercontent.com/57734613/156299500-ba40c557-cd29-40f8-b012-3f23cad2d599.png)

---

### 7. Aggregation with Group By
Number of monster races by location.\
![image](https://user-images.githubusercontent.com/57734613/156299555-bc8c1f21-d4c7-4880-8f1a-0dbe43df0d41.png)

---

### 8. Aggregation with Having
Shops with inventory amount of 50+ at each location.\
![image](https://user-images.githubusercontent.com/57734613/156299656-40551438-23c7-463a-a947-307008b6bcaf.png)

---

### 9.  Nested Aggregation with Group By
Most expensive item at each location.\
![image](https://user-images.githubusercontent.com/57734613/156299744-980c18b6-ddaa-4abc-ac2b-4c32fd030c90.png)

---

### 10. Division
Players that bought from all locations.\
![image](https://user-images.githubusercontent.com/57734613/156299820-9dc2302c-5210-473a-ad66-21252da1f08a.png)
