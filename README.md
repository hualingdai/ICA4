# ICA4

-- which airports have cargo rev between 10000 to 16000?
```SQL
SELECT cargo_rev, destination_airport, id
FROM datasets.flight_revenue
WHERE cargo_rev between '10000' and '16000'
ORDER BY id DESC
```
![ICA4](Visualization/ICA4-1.png)

-- Which artists has been on the spotify top 100 the most?
```SQL
SELECT artist, 
count (*) as top_artists
FROM datasets.spotify_worldwide_daily_song_ranking 
GROUP BY artist
ORDER BY top_artists DESC 
LIMIT 100
```

![ICA4](Visualizaion/ICA4-2.png)

-- What is the position from 8-10? (which songs has position from 8-10) 
```SQL
SELECT *
FROM datasets.spotify_worldwide_daily_song_ranking 
WHERE  position in (8,9,10) 
limit 100
```

![ICA4](Visualization/ICA4-3.png)

-- Which airports have business class rev below 9000?
```SQL
SELECT destination_airport, business_class_rev
FROM datasets.flight_revenue
WHERE business_class_rev < '9000'
ORDER BY business_class_rev DESC
```
![ICA4](Visualization/ICA4-4.png)

-- Which songs have more than 3 million streams?
```SQL
SELECT trackname,
        	artist,
        	 streams
FROM datasets.spotify_worldwide_daily_song_ranking
WHERE streams>3000000
ORDER BY streams ASC
LIMIT 100
```

1[ICA4](Visualization/ICA4-4.png)
