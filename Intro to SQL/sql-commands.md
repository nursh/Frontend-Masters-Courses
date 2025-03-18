# SQL commands

- single quotes and double quotes are not interchangeable
  - the values are always in single quotes
  - the column names and tables will use double quotes
  - eg: 
    - INSERT INTO ingredients ( "title", "image", "type")
      VALUES ('red pepper', 'red_pepper.jpg', 'vegetable');
    - title, image, type are columns of the table ingredients, so they use double quotes
    - the values use single quotes

- ON CONFLICT DO NOTHING
  - if there is a problem, don't error out
- ON CONFLICT can also be used for other things
  - like upserting
  - if there is a conflict, update certain columns
  - eg
    - ON CONFLiCT (title) DO UPDATE SET image = excluded.image
    - if there is a title conflict in the insert, update the image to the excluded row image
- 