# TAOCcharacters
A website featuring the characters of The Adventures Of Crizion!
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>The Adventures of Crizion Character Site</title>
    <style>
        body {
            margin: 0;
            font-family: 'Trebuchet MS', sans-serif;
            background: linear-gradient(120deg, red, limegreen);
            color: white;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        header {
            text-align: center;
            padding: 2em 0;
            background-color: rgba(0, 0, 0, 0.6);
            width: 100%;
        }

        header h1 {
            font-size: 3em;
            font-weight: bold;
            margin: 0;
        }

        .main-page {
            display: block;
            width: 100%;
            padding: 2em;
            overflow-y: auto;
        }

        .character-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            width: 100%;
            padding: 20px;
        }

        .character {
            width: 90%;
            max-width: 400px;
            background-color: rgba(0, 0, 0, 0.8);
            margin: 1em 0;
            padding: 1em;
            text-align: center;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            transition: transform 0.3s ease-in-out;
        }

        .character img {
            width: 100%;
            height: auto;
            border-radius: 10px;
        }

        .character:hover {
            transform: scale(1.05);
        }

        .character-name {
            font-size: 1.5em;
            margin: 0.5em 0;
        }

        .character-link, .back-button {
            text-decoration: none;
            color: limegreen;
            cursor: pointer;
            padding: 0.5em 1em;
            border-radius: 5px;
            font-size: 1em;
            display: inline-block;
            margin-bottom: 1em;
        }

        .character-link:hover, .back-button:hover {
            color: red;
        }

        .info-page {
            padding: 2em;
            margin: 2em auto;
            max-width: 800px;
            width: 100%;
            background-color: rgba(0, 0, 0, 0.8);
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
            display: none;
            box-sizing: border-box;
        }

        .info-page h2 {
            font-size: 2em;
        }

        p {
            font-size: 1.2em;
            line-height: 1.6em;
        }

        hr {
            border: 0;
            height: 2px;
            background-color: white;
            margin: 1em 0;
        }

        /* Mobile */
        @media (max-width: 768px) {
            .info-page {
                width: 90%;
            }

            .character-container {
                padding: 10px;
            }

            .character {
                width: 100%;
                max-width: none;
            }

            header h1 {
                font-size: 2em;
            }

            .character-name {
                font-size: 1.2em;
            }
        }
    </style>
    <script>
        document.addEventListener('contextmenu', function(e) {
            e.preventDefault(); // Disables right-click
        });

        function showCharacterInfo(characterId) {
            document.querySelectorAll('.info-page').forEach(page => page.style.display = 'none');
            document.querySelector('.main-page').style.display = 'none';
            document.getElementById(characterId).style.display = 'block';
        }

        function goBack() {
            document.querySelectorAll('.info-page').forEach(page => page.style.display = 'none');
            document.querySelector('.main-page').style.display = 'block';
        }
    </script>
</head>
<body>

    <header>
        <h1>The Adventures of Crizion Character Site</h1>
    </header>
	<h2><u> A website featuring all the characters from TAOC and more to come! </u></h2>

    <!-- Main Page with Characters -->
    <div class="main-page">
        <div class="character-container">
            <!-- Character 1 -->
            <div class="character">
		<img src="https://i.imgur.com/6114mVZ.jpeg" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Crizion</h2>
                <span class="character-link" onclick="showCharacterInfo('character1-info')">View Details</span>
            </div>
            <!-- Character 2 -->
            <div class="character">
		<img src="https://i.imgur.com/p27rtqw.jpeg" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Crazytree</h2>
                <span class="character-link" onclick="showCharacterInfo('character2-info')">View Details</span>
            </div>
            <!-- Character 3 -->
            <div class="character">
		<img src="https://i.imgur.com/KZxuJBd.jpeg" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Bulletblade</h2>
                <span class="character-link" onclick="showCharacterInfo('character3-info')">View Details</span>
            </div>
            <!-- Character 4 -->
            <div class="character">
  		<img src="https://i.imgur.com/TMUr6pK.jpeg" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Izzy</h2>
                <span class="character-link" onclick="showCharacterInfo('character4-info')">View Details</span>
            </div>
            <!-- Character 5 -->
            <div class="character">
		<img src="https://i.imgur.com/fbm67rC.jpeg" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Tkaragem</h2>
                <span class="character-link" onclick="showCharacterInfo('character5-info')">View Details</span>
            </div>
            <!-- Character 6 -->
            <div class="character">
		<img src="https://i.imgur.com/HUn3TUo.jpeg" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Anya</h2>
                <span class="character-link" onclick="showCharacterInfo('character6-info')">View Details</span>
            </div>
            <!-- Character 7 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Axol</h2>
                <span class="character-link" onclick="showCharacterInfo('character7-info')">View Details</span>
            </div>
            <!-- Character 8 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Pelestia</h2>
                <span class="character-link" onclick="showCharacterInfo('character8-info')">View Details</span>
            </div>
            <!-- Character 9 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Vester</h2>
                <span class="character-link" onclick="showCharacterInfo('character9-info')">View Details</span>
            </div>
            <!-- Character 10 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Iris</h2>
                <span class="character-link" onclick="showCharacterInfo('character10-info')">View Details</span>
            </div>
            <!-- Character 11 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Abigail</h2>
                <span class="character-link" onclick="showCharacterInfo('character11-info')">View Details</span>
            </div>
            <!-- Character 12 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Linden</h2>
                <span class="character-link" onclick="showCharacterInfo('character12-info')">View Details</span>
            </div>
            <!-- Character 13 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Dave</h2>
                <span class="character-link" onclick="showCharacterInfo('character13-info')">View Details</span>
            </div>
            <!-- Character 14 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Pyrana</h2>
                <span class="character-link" onclick="showCharacterInfo('character14-info')">View Details</span>
            </div>
            <!-- Character 15 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Arrowite</h2>
                <span class="character-link" onclick="showCharacterInfo('character15-info')">View Details</span>
            </div>
            <!-- Character 16 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Larah</h2>
                <span class="character-link" onclick="showCharacterInfo('character16-info')">View Details</span>
            </div>
            <!-- Character 17 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Igor</h2>
                <span class="character-link" onclick="showCharacterInfo('character17-info')">View Details</span>
            </div>
            <!-- Character 18 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Jyaine</h2>
                <span class="character-link" onclick="showCharacterInfo('character18-info')">View Details</span>
            </div>
            <!-- Character 19 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Garvoch</h2>
                <span class="character-link" onclick="showCharacterInfo('character19-info')">View Details</span>
            </div>
            <!-- Character 20 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Wuji</h2>
                <span class="character-link" onclick="showCharacterInfo('character20-info')">View Details</span>
            </div>
            <!-- Character 21 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Carpacho</h2>
                <span class="character-link" onclick="showCharacterInfo('character21-info')">View Details</span>
            </div>
            <!-- Character 22 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Yavel</h2>
                <span class="character-link" onclick="showCharacterInfo('character22-info')">View Details</span>
            </div>
            <!-- Character 23 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Benton</h2>
                <span class="character-link" onclick="showCharacterInfo('character23-info')">View Details</span>
            </div>
            <!-- Character 24 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Estrailia</h2>
                <span class="character-link" onclick="showCharacterInfo('character24-info')">View Details</span>
            </div>
            <!-- Character 25 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Necros</h2>
                <span class="character-link" onclick="showCharacterInfo('character25-info')">View Details</span>
            </div>
            <!-- Character 26 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Heveres</h2>
                <span class="character-link" onclick="showCharacterInfo('character26-info')">View Details</span>
            </div>
            <!-- Character 27 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Lisa</h2>
                <span class="character-link" onclick="showCharacterInfo('character27-info')">View Details</span>
            </div>
            <!-- Character 28 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Decratos</h2>
                <span class="character-link" onclick="showCharacterInfo('character28-info')">View Details</span>
            </div>
            <!-- Character 29 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Ugarness</h2>
                <span class="character-link" onclick="showCharacterInfo('character29-info')">View Details</span>
            </div>
            <!-- Character 30 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Girade</h2>
                <span class="character-link" onclick="showCharacterInfo('character30-info')">View Details</span>
            </div>
            <!-- Character 31 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Farago</h2>
                <span class="character-link" onclick="showCharacterInfo('character31-info')">View Details</span>
            </div>
            <!-- Character 32 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Barricrude</h2>
                <span class="character-link" onclick="showCharacterInfo('character32-info')">View Details</span>
            </div>
            <!-- Character 33 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Takatoka</h2>
                <span class="character-link" onclick="showCharacterInfo('character33-info')">View Details</span>
            </div>
            <!-- Character 34 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Gemeina</h2>
                <span class="character-link" onclick="showCharacterInfo('character34-info')">View Details</span>
            </div>
            <!-- Character 35 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Tupa</h2>
                <span class="character-link" onclick="showCharacterInfo('character35-info')">View Details</span>
            </div>
            <!-- Character 36 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Viviana</h2>
                <span class="character-link" onclick="showCharacterInfo('character36-info')">View Details</span>
            </div>
            <!-- Character 37 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Torean</h2>
                <span class="character-link" onclick="showCharacterInfo('character37-info')">View Details</span>
            </div>
            <!-- Character 38 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Tunundra</h2>
                <span class="character-link" onclick="showCharacterInfo('character38-info')">View Details</span>
            </div>
            <!-- Character 39 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Ludicrous</h2>
                <span class="character-link" onclick="showCharacterInfo('character39-info')">View Details</span>
            </div>
            <!-- Character 40 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Blendice</h2>
                <span class="character-link" onclick="showCharacterInfo('character40-info')">View Details</span>
            </div>
            <!-- Character 41 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Razorox</h2>
                <span class="character-link" onclick="showCharacterInfo('character41-info')">View Details</span>
            </div>
            <!-- Character 42 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Charolette</h2>
                <span class="character-link" onclick="showCharacterInfo('character42-info')">View Details</span>
            </div>
            <!-- Character 43 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Sourczess</h2>
                <span class="character-link" onclick="showCharacterInfo('character43-info')">View Details</span>
            </div>
            <!-- Character 44 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Blaze</h2>
                <span class="character-link" onclick="showCharacterInfo('character44-info')">View Details</span>
            </div>
            <!-- Character 45 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Cocy</h2>
                <span class="character-link" onclick="showCharacterInfo('character45-info')">View Details</span>
            </div>
            <!-- Character 46 -->
            <div class="character">
  		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Spricados</h2>
                <span class="character-link" onclick="showCharacterInfo('character46-info')">View Details</span>
            </div>
            <!-- Character 47 -->
            <div class="character">
		<img src="" width="300" height="200" alt="Your Image">
                <h2 class="character-name">Epister</h2>
                <span class="character-link" onclick="showCharacterInfo('character47-info')">View Details</span>
            </div>
            <!-- Character 48 -->
            <div class="character">
                <img src="placeholder.jpg" alt="Metal Master (Thomas Your thing goes here)">
                <h2 class="character-name">Metal Master</h2>
                <span class="character-link" onclick="showCharacterInfo('character48-info')">View Details</span>
            </div>
            <!-- Character 49 -->
            <div class="character">
                <img src="Zegatrox.jpg" alt="This punk">
                <h2 class="character-name">Zegatrox</h2>
                <span class="character-link" onclick="showCharacterInfo('character49-info')">View Details</span>
            </div>
        </div>
    </div>
    <!-- Info Pages for Characters -->
    <div class="info-page" id="character1-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Crizion</h2>
	<img src="https://i.imgur.com/6114mVZ.jpeg" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> Reptilian</p>
        <p><strong>Gender:</strong> Male</p>
        <p><strong>Age:</strong> 18</p>
	<p><strong>Role:</strong> Hero</p>
        <p><strong>Birthday:</strong> September 22nd</p>
        <hr>
        <p><strong>Description:</strong> Crizion is a optimistic Reptilian who always looks on the bright side of things. He will never hesistate to help out friends or family in need. Crizion was born a few days after The Dark Skies War was declared, when his village was under siege, his father who was an excellent warrior goes to defend his hometown, after defending it greatly for some time, he eventully met his end as an arrow was struck through his head. As the warriors of the Shadefolk kingdom pushed closer, their home was burnt to the ground with Crizion and his mother in it, while his mother died under the collapse, Crizion lived, who was then quickly saved by an Anyonomus Reptilian Warrior and brought to shelter until the war passed. From their, his Grandma Pho took Crizion under her wing. Eventully, Crizion had to get a job at a blacksmith to support his grandma who was unable to work, and thats how his life is going at the moment. Crizion likes to try to hang out with others a lot, but ends up being awkward, he shows signs of great leadership and inspiration, but has not been given the chance for them to shine yet. Crizions dream is to explore the world and make new friends, all while putting an end to the aftermath policies of The Dark Skies War.</p>
    </div>

    <div class="info-page" id="character2-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Crazytree</h2>
	<img src="https://i.imgur.com/p27rtqw.jpeg" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> Zuku</p>
        <p><strong>Gender:</strong> Male</p>
        <p><strong>Age:</strong> 19 (38 in Zuku Years)</p>
	<p><strong>Role:</strong> Hero</p>
        <p><strong>Birthday:</strong> October 21st</p>
        <hr>
        <p><strong>Description:</strong> Crazytree (also known by Fern) is a clueless Zuku that never knows whats going on. Once he is fixtated on something, he will stop paying attention to anything else, but he is also loyal to the very end when it comes to friendships. Crazytree was born about a year before the Dark Skies wars beginning, as he grew up, He was an insane kid that didnt think too much about his choices, he did what he pleased. So instead of calling him by his real name of Fern, everyone nicknamed him Crazytree. His father, who was the King of the Kingdom, had a pent up rage from Crazytrees actions as they got worse. Soon he couldnt take it anymore, since lecturing had no effect, he struck Crazytree. After being struck, Crazytree was put in a state of mind where he did nothing, people thought he was paralyzed and mentally damaged and the King regretted his action the most. Time passed and eventully The Dark Skies war came, the Zuku's entire kingdom was up in flames, The King quickly grabbed Crazytree from his seated spot and ran to a seceret safety chamber while Arrowite fended off Shadefolk soliders. The chamber could only hold one person, but was immune to almost anything, it was reserved for the king. But instead, The King shoved Crazytree in their along with the powerful gem from his staff, the chamber was sealed off and The king went up in flames. After a long slumber that caused him to become mute in the process, he was released by no other then Crizion himself, to which he gave his utmost loyalty to Crizion. Crazytree trys his best to tend to peaceful tatics, but knows that violence must sometimes be an option with his great power he has. His dream is to restore peace to the world with his buddy Crizion.</p>
    </div>

    <div class="info-page" id="character3-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Bulletblade</h2>
	<img src="https://i.imgur.com/KZxuJBd.jpeg" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> Shadefolk</p>
        <p><strong>Gender:</strong> Male</p>
        <p><strong>Age:</strong> 18</p>
	<p><strong>Role:</strong> Hero</p>
        <p><strong>Birthday:</strong> May 23rd</p>
        <hr>
        <p><strong>Description:</strong> Bulletblade (also known by Reiss) is a sly and fast Shadefolk that does stuff that only helps himself. With his super fast speed and reflexes, he can do whatever he pleases, he always steals the show with his massive amounts of jesting. Bulletblade was born into a family of absolute royalty, he is the youngest of the 3 brothers in the royal family. His father; Yaozen, sought a son who could carry the vessel of a dragon. Yaozen got what he wanted instantly as the eldest brother Wuji was gifted it, so Reiss and Garvoch were casted aside and paid no attention too. The dark skies war took place, but Bulletblade was safe inside the castle with the strongest defense, so he went uneffected. As time passed from their, he took on the job of a guard. One day, he chased a theif into a valley who had stolen fruits, once he reached the end of the valley is where eveyrhting changed for him. He saw hundreds of Shadefolk, starving and with ripped clothes. That was all Reiss needed to see to realize how cruel his fathers methods were. That same day, he confronted his father about it and they ended up getting into a huge argument, something Reiss said to Yaozen really struck Yaozens ego, so Yaozen swung his claymore and Reiss and banished him from the Royal doors. From their, Reiss traveled back to the Valley with the unfortanute in it and offered help, their cheif accepted them. From there, Reiss became an astonishing theif, honing his skills to perfection to steal all kinds of neccesities without anyone batting an eye. Eventully he was caught on too though and a bounty was put on his head. But that didnt stop him, the cheif of the unfortanate gifted Reiss with a fancy cloth that resembled a ninja suit and two katanas, shortly after, Benton gifted him with two pistols crafted by him for helping his family in the unfortanate. Reiss then decided to go by the nickname of Bulletblade, and he swore to fight for the unfortanate, since thats what he wants to do. Bulletblades dream is to correct the mistakes his father made...and to pick up a hot chick to marry along the way.</p>
    </div>

    <div class="info-page" id="character4-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Izzy</h2>
	<img src="https://i.imgur.com/TMUr6pK.jpeg" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> Centipedra</p>
        <p><strong>Gender:</strong> Female</p>
        <p><strong>Age:</strong> 18</p>
	<p><strong>Role:</strong> Hero</p>
        <p><strong>Birthday:</strong> June 12th</p>
        <hr>
        <p><strong>Description:</strong> Izzy is a kind and compassionate centipedra who wants to learn more about the world. She will always talk someones ear off no matter the subject, she loves convesations. Izzy was born only a few months before the Dark Skies War. Shortly after her birth, she was orphaned, her parents didnt want anything to do with a child. She spent her days in the orphanage, where people did the bare minimum to take care of her. When the Dark skies war hit, it was just a big sheltering event, no intense harm was done, but it was a grueling time while the war was active having limited supplies. After the war, she was given an education, where she quickly rose to the top. As time continued, she was still the top of her class, making the other girls jealous, she was dared to go to the surface of the desert, where monsters roamed. With all the pressure that was laid on to her, she did it. After quickly making to the surface, it wasnt long before she was spotted. Thinking she could go back down, she wasnt able too since she drilled improperly. She was about an inch before becoming lunch meat until the mosnter swerved to its side and dropped to the ground. Izzy looked around for a moment and saw another figure, centipedra shaped with black skin. both of them quickly went back underground. The centipedra who killed the monster was Lisa, After asking Izzy a few questions, she asked where her parents were. It wasnt long until Lisa realized she was an orphan. After some time, Lisa made the heartfelt sdecision to adopt Izzy. From there, Izzy learned the ways of the hunter and worked on her own personal skills for the rest of her years up until now. Izzy also has a fond intrest in dancing, which is why she was given a weapon based aroudn it, a whip with a spikey flat face at the end, she cherished it greatly. Izzy's dream is to finally see the world for what it is and help people around the world that are struggling.</p>
    </div>

    <div class="info-page" id="character5-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Tkaragem</h2>
	<img src="https://i.imgur.com/fbm67rC.jpeg" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> Crystal</p>
        <p><strong>Gender:</strong> Male</p>
        <p><strong>Age:</strong> 19</p>
	<p><strong>Role:</strong> Hero</p>
        <p><strong>Birthday:</strong> Feburary 7th</p>
        <hr>
        <p><strong>Description:</strong> Tkaragem is a hard working competitve crystal that treats everything as if it were a testament to his skill. He will do anything to become the greatest, all while gaining respect from his peers. Tkaragem was born Shortly after the Crystals general awakening from the grand heart. From there, his self proclaimed leader; Ukara, guided him along with everyone else on a path to find themselves in the world. Tkaragem mostly took intrest in competition, he would do simple things like racing others and having hand to hand duals with others. Tkaragem didnt make many friends this way, but he didnt care, all he cared about was being the best. Ukara let him explore that intrest for awhile until almost two years passed, where Ukara would have an important talk with Tkaragem. After the talk led to the events of the Dark Skies war. Since the siege was almsot imediate for the crystals with the balme placed on them. Tkaragem and all the other Crystals were caught off guard. Tkaragem was practicing his comabt only to suddenly be ambushed by a Shadefolk. Tkaragem was able to handle him with ease, but it didnt come so easy when he was surrounded. Ukara would then jump in to save the day, using specialized sleep dart crystals from his tail to put them to sleep. Ukara was against the thoguht of unatural killing, they believed that this was not an unatural scenario. Everyone was set to run for the ocean, since they can breath in water. As Ukara and Tkaragem were about to reach the edge, Tkaragem wasnt ready to flee, he got out of Ukaras grasp and started beating up more shadefolk. Ukara stopped him shortly and attempted to pull him. Shortly after, Ukara got impaled. The moment was slient and Tkaragem was shell shocked. Someone else picked up Tkaragem and they went deep into the ocean. Tkaragem then spent the first few years of his life mourning until he was hit with a vision from Ukara. After that, Tkaragem stayed true to his goals while helping others as well. After a few more years, the crystals would take back their land from the Shadefolk and life would begin anew. Tkaragem now continues to support everyones paths, showing signs of compassion despite not showing emotions super well. Tkaragems dream is to become the best combat warrior there ever was and to find someone worthy of his strength.</p>
    </div>

    <div class="info-page" id="character6-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Anya</h2>
	<img src="https://i.imgur.com/HUn3TUo.jpeg" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> Frost</p>
        <p><strong>Gender:</strong> Female</p>
        <p><strong>Age:</strong> 18</p>
	<p><strong>Role:</strong> Hero</p>
        <p><strong>Birthday:</strong> August 30th</p>
        <hr>
        <p><strong>Description:</strong> Anya is a stone cold law abiding warrior that will stop at nothing to bring people to justice. She will spend all day perfecting her skills to defend her nation until the day she dies, no matter what. Anya was bor very shortly before the dark skies war. She was born into a family of high regrads, one where her father was a general of the frost army. When the dark skies war hit, Anya's farther cam back gravely injured, with one leg completly broken and an arm gravely injured. Something rattled inside Anya's brain, despite being only a baby, it would be an image she never forgets. The image of her injured father would keep reappearing in her head like a mental nightmare, she couldnt stand to see her father in that state or worse, dead. As Anya grew up, she paid no attention to academics and focused soley on combat training. Her designated weapon was a short sword, where she would use it at least 5 hours a day. As she kept growing up, her comabt and physique kept improving, but her social skills and family bonds slowly grew apart. Anya would not even bother to make friends in school, any attempt from someone would be shunned, and boys who hit on her would end up with their head in the ground. Her family was concerned for her intense training engagment. At 16, an argument sparked between Anya's family and Anya. Her father got mad enough to the point where he called her a monster. Anya ended that conversation with a slammed door. She made her ways to the frontline winter storms of the Frosts land and set up her own bootcamp. This is where she would spend the next 2 years. She has fought off a formidable amount of people, even the cruel mosnter known as Ludicrous, With every new victory, she feels a little of herself dying inside and wonders how life could be different. Anya's dream is to protect her homelands and bring anyone to justice that trys to harm it, and to fianlly make her father see that she was right.</p>
    </div>

    <div class="info-page" id="character7-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Axol</h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> Dragon</p>
        <p><strong>Gender:</strong> Male</p>
        <p><strong>Age:</strong> 19</p>
	<p><strong>Role:</strong> Hero</p>
        <p><strong>Birthday:</strong> March 8th</p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

    <div class="info-page" id="character8-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Pelestia</h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

    	<div class="info-page" id="character9-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Vester</h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character10-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Iris</h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character11-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Abigail</h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character12-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Linden</h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character13-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Dave</h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character14-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character15-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>
	
	<div class="info-page" id="character16-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character17-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character18-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character19-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character20-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character21-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character22-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character23-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character24-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character25-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character26-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character27-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character28-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character29-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character30-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character31-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character32-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character33-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character34-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character35-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character36-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character37-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character38-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character39-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character40-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character41-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character42-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character43-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character44-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character45-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character46-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character47-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character48-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

	<div class="info-page" id="character49-info">
        <a class="back-button" onclick="goBack()">← Back</a>
        <h2>Character </h2>
	<img src="" width="725" height="455" alt="Your Image">
	<p><strong>Species:</strong> </p>
        <p><strong>Gender:</strong> </p>
        <p><strong>Age:</strong> </p>
	<p><strong>Role:</strong> </p>
        <p><strong>Birthday:</strong> </p>
        <hr>
        <p><strong>Description:</strong> Coming Soon!</p>
    </div>

<script>
        function showCharacterInfo(characterId) {
            // Hide all info pages first
            document.querySelectorAll('.info-page').forEach(page => page.style.display = 'none');
            // Hide the main page
            document.querySelector('.main-page').style.display = 'none';
            // Show the selected character info page
            document.querySelector(`#${characterId}`).style.display = 'block';
        }

        function goBack() {
            // Hide all info pages
            document.querySelectorAll('.info-page').forEach(page => page.style.display = 'none');
            // Show the main page again
            document.querySelector('.main-page').style.display = 'block';
        }
    </script>
</body>
</html>


