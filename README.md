# Web Automation Study Script

## Description
This repository contains a Tampermonkey userscript designed for educational purposes to demonstrate web automation techniques. The script randomly moves a character in a web-based environment, including diagonal movements, every 3 seconds. It includes functionality to detect specific entities and stop movement upon detection. The script uses JavaScript to interact with web elements, simulate clicks, and handle AJAX requests.

**Important Note**: This script is for educational purposes only and should not be used to automate gameplay in violation of any game's terms of service. Using this script in online games may result in account bans, legal consequences, or negative impacts on game communities. Always respect game developers and community guidelines.

## Features
- Random movement in 8 directions (up, down, left, right, NE, NW, SE, SW) using a random number generator
- Movement occurs every 3 seconds
- Detects specific entities and stops movement upon detection
- Toggle button to start/stop automation
- Extensive debugging logs for troubleshooting
- AJAX fallback for movement simulation

## Educational Purpose
This script is intended to help learners understand:
- DOM manipulation and element selection
- Event simulation (e.g., clicking elements)
- Random number generation for decision-making
- AJAX requests for web interactions
- Error handling and debugging techniques

## Prerequisites
- A modern web browser (e.g., Chrome, Firefox, Edge)
- Tampermonkey browser extension installed
- Basic understanding of JavaScript and web development

## Step-by-Step Instructions for Using the Script
Follow these steps to study and test the script in a controlled, educational environment. These instructions are written in simple language so anyone can understand. **Do not use in live games without explicit permission from game operators, as this could break rules and get you in trouble.**

---

### Step 1: Get the Right Tools
Before you start, you need a web browser (like Google Chrome or Firefox) and a special tool called Tampermonkey. This tool lets you run custom scripts on web pages.

1. **Open Your Web Browser**:
   - Use Google Chrome, Firefox, or Microsoft Edge. These are popular browsers.
   - If you don't have one, download Chrome from [google.com/chrome](https://www.google.com/chrome/) or Firefox from [mozilla.org/firefox](https://www.mozilla.org/firefox/).

2. **Find Tampermonkey**:
   - Tampermonkey is like a helper tool that lets you add custom scripts to web pages.
   - Go to your browser's extension store:
     - For Chrome: Open Chrome, click the three dots in the top-right corner, go to "More Tools" > "Extensions", then click "Open Chrome Web Store" at the bottom.
     - For Firefox: Open Firefox, click the three lines in the top-right corner, go to "Add-ons and Themes".
     - For Edge: Open Edge, click the three dots in the top-right corner, go to "Extensions", then click "Get extensions for Microsoft Edge".

3. **Search for Tampermonkey**:
   - In the extension store, type "Tampermonkey" in the search bar and press Enter.
   - Look for the one called "Tampermonkey" (it usually has a black-and-yellow icon).

4. **Install Tampermonkey**:
   - Click "Add to Chrome" (or "Add to Firefox", or "Get" for Edge).
   - A pop-up will ask if you want to add it. Click "Add extension" or "Add".
   - Wait a few seconds. You'll see a message saying Tampermonkey was added.
   - Check the top-right corner of your browser. You should see a new Tampermonkey icon (black-and-yellow).

5. **Make Sure Tampermonkey is Working**:
   - Click the Tampermonkey icon in the top-right corner of your browser.
   - A menu will pop up. Click "Dashboard".
   - A new tab will open with the Tampermonkey Dashboard. This means it's working.
   - If you don't see the icon, go back to the extension store and make sure it's enabled.

---

### Step 2: Add the Script to Tampermonkey
Now that you have Tampermonkey, you need to add the script to it. The script is like a set of instructions for the browser to follow.

1. **Find the Script**:
   - The script is in a file called `script.js` in this repository.
   - Open the repository on GitHub (where you found this README).
   - Click on `script.js` to open it.
   - You'll see a lot of text (code). Don't worry, you don't need to understand it all yet.

2. **Copy the Script**:
   - Click anywhere on the code in `script.js`.
   - Press Ctrl+A (or Cmd+A on a Mac) to select all the text.
   - Press Ctrl+C (or Cmd+C on a Mac) to copy it.
   - Now the script is copied to your computer's clipboard (like copying text in a document).

3. **Open Tampermonkey Dashboard**:
   - Click the Tampermonkey icon in the top-right corner of your browser.
   - Click "Dashboard" from the menu.
   - A new tab will open with the Tampermonkey Dashboard.

4. **Create a New Script**:
   - In the Dashboard, look for a "+" tab at the top (next to "Installed userscripts").
   - Click the "+" tab. This opens a new script editor.
   - You'll see some default text (code) in the editor. You need to replace it.

5. **Paste the Script**:
   - Click anywhere in the editor where the default text is.
   - Press Ctrl+A (or Cmd+A on a Mac) to select all the default text.
   - Press Delete or Backspace to remove it.
   - Now press Ctrl+V (or Cmd+V on a Mac) to paste the script you copied from `script.js`.
   - The editor should now show the new script.

6. **Save the Script**:
   - Press Ctrl+S (or Cmd+S on a Mac) to save the script.
   - Or click "File" in the top-left corner of the editor, then click "Save".
   - You'll see a message saying "Script saved".
   - The script is now ready to use, but only in a test environment.

---

### Step 3: Set Up a Test Environment
The script is designed for learning, not for playing games automatically. You need a safe test environment (like a local web page) to study how it works. Do not use it in real games, as this could break rules and get you banned.

1. **Understand the Script's Purpose**:
   - The script moves a character randomly in 8 directions (up, down, left, right, and diagonals) every 3 seconds.
   - It also looks for specific things (entities) on the page and stops moving if it finds one.
   - For learning, you need to test it on a web page you control, not a real game.

2. **Create a Simple Test Page (Optional)**:
   - If you want to test the script, you can make a simple web page on your computer:
     - Open Notepad (Windows) or TextEdit (Mac).
     - Copy and paste this simple HTML code:
       ```html
       <!DOCTYPE html>
       <html>
       <head>
           <title>Test Page</title>
       </head>
       <body>
           <h1>Test Environment</h1>
           <div id="dr-nw" class="m-move">NW</div>
           <div id="dr-n" class="m-move">N</div>
           <div id="dr-ne" class="m-move">NE</div>
           <div id="dr-e" class="m-move">E</div>
           <div id="dr-w" class="m-move">W</div>
           <div id="dr-se" class="m-move">SE</div>
           <div id="dr-s" class="m-move">S</div>
           <div id="dr-sw" class="m-move">SW</div>
           <div class="wild-pokemon-name">example1</div>
       </body>
       </html>
       ```
     - Save the file as `test.html` on your desktop (make sure it ends with `.html`).
     - Open the file in your browser by double-clicking it.
   - This page has fake movement buttons and an entity for testing.

3. **Change the Script's URL (For Testing)**:
   - Go back to the Tampermonkey Dashboard.
   - Open your script (click on its name in the list).
   - Look for the line that says:
     ```javascript
     // @match        https://example.com/map/*
     ```
   - Change it to match your test page. For example:
     ```javascript
     // @match        https://www.delugerpg.com/map/overworld5
     ```
     - Replace `C:/Users/YourName/Desktop/test.html` with the actual path to your `test.html` file.
   - Save the script (Ctrl+S or File > Save).

4. **Do Not Use in Real Games**:
   - The script has placeholders (like `https://example.com/map/*` and `entities = ['example1', 'example2']`) to avoid game-specific automation.
   - Do not change these to match a real game


#POKEMON FORMAT
---
##Kanto Region :
'bulbasaur', 'charmander', 'squirtle', 'caterpie', 'weedle', 'pidgey', 'rattata', 'spearow', 'ekans',  
'pikachu', 'sandshrew', 'nidoran', 'nidoran', 'clefairy', 'vulpix', 'jigglypuff', 'zubat', 'oddish', 'paras', 'venonat',  
'diglett', 'meowth', 'psyduck', 'mankey', 'growlithe', 'poliwag', 'abra', 'machop', 'bellsprout', 'tentacool', 'geodude',  
'ponyta', 'slowpoke', 'magnemite', 'farfetchd', 'doduo', 'seel', 'grimer', 'shellder', 'gastly', 'onix', 'drowzee',  
'krabby', 'voltorb', 'exeggcute', 'cubone', 'hitmonlee', 'hitmonchan', 'lickitung', 'koffing', 'rhyhorn', 'chansey',  
'tangela', 'kangaskhan', 'horsea', 'goldeen', 'staryu', 'mr mime', 'scyther', 'jynx', 'electabuzz', 'magmar', 'pinsir',  
'tauros', 'magikarp', 'lapras', 'ditto', 'eevee', 'porygon', 'omanyte', 'kabuto', 'aerodactyl', 'snorlax', 'articuno',  
'zapdos', 'moltres', 'dratini', 'mewtwo', 'mew'
---
## Johto:
'chikorita', 'bayleef', 'meganium', 'cyndaquil', 'quilava', 'typhlosion', 'totodile', 'croconaw', 'feraligatr', 'sentret', 'furret',  
'hoothoot', 'noctowl', 'ledyba', 'ledian', 'spinarak', 'ariados', 'crobat', 'chinchou', 'lanturn', 'pichu', 'cleffa', 'igglybuff',  
'togepi', 'togetic', 'natu', 'xatu', 'mareep', 'flaaffy', 'ampharos', 'mega ampharos', 'bellossom', 'marill', 'azumarill', 'sudowoodo',  
'politoed', 'hoppip', 'skiploom', 'jumpluff', 'aipom', 'sunkern', 'sunflora', 'yanma', 'wooper', 'quagsire', 'espeon', 'umbreon',  
'murkrow', 'slowking', 'misdreavus', 'unown', 'wobbuffet', 'girafarig', 'pineco', 'forretress', 'dunsparce', 'gligar', 'steelix',  
'mega steelix', 'snubbull', 'granbull', 'qwilfish', 'scizor', 'mega scizor', 'shuckle', 'heracross', 'mega heracross', 'sneasel',  
'teddiursa', 'ursaring', 'slugma', 'magcargo', 'swinub', 'piloswine', 'corsola', 'remoraid', 'octillery', 'delibird', 'mantine',  
'skarmory', 'houndour', 'houndoom', 'mega houndoom', 'kingdra', 'phanpy', 'donphan', 'porygon2', 'stantler', 'smeargle', 'tyrogue',  
'hitmontop', 'smoochum', 'elekid', 'magby', 'miltank', 'blissey', 'raikou', 'entei', 'suicune', 'larvitar', 'pupitar', 'tyranitar',  
'mega tyranitar', 'lugia', 'ho-oh', 'celebi'
---
## Hoenn
'treecko', 'grovyle', 'sceptile', 'mega sceptile', 'torchic', 'combusken', 'blaziken', 'mega blaziken', 'mudkip', 'marshtomp',  
'swampert', 'mega swampert', 'poochyena', 'mightyena', 'zigzagoon', 'linoone', 'wurmple', 'silcoon', 'beautifly', 'cascoon',  
'dustox', 'lotad', 'lombre', 'ludicolo', 'seedot', 'nuzleaf', 'shiftry', 'taillow', 'swellow', 'wingull', 'pelipper', 'ralts',  
'kirlia', 'gardevoir', 'mega gardevoir', 'surskit', 'masquerain', 'shroomish', 'breloom', 'slakoth', 'vigoroth', 'slaking',  
'nincada', 'ninjask', 'shedinja', 'whismur', 'loudred', 'exploud', 'makuhita', 'hariyama', 'azurill', 'nosepass', 'skitty',  
'delcatty', 'sableye', 'mega sableye', 'mawile', 'mega mawile', 'aron', 'lairon', 'aggron', 'mega aggron', 'meditite', 'medicham',  
'mega medicham', 'electrike', 'manectric', 'mega manectric', 'plusle', 'minun', 'volbeat', 'illumise', 'roselia', 'gulpin',  
'swalot', 'carvanha', 'sharpedo', 'mega sharpedo', 'wailmer', 'wailord', 'numel', 'camerupt', 'mega camerupt', 'torkoal',  
'spoink', 'grumpig', 'spinda', 'trapinch', 'vibrava', 'flygon', 'cacnea', 'cacturne', 'swablu', 'altaria', 'mega altaria',  
'zangoose', 'seviper', 'lunatone', 'solrock', 'barboach', 'whiscash', 'corphish', 'crawdaunt', 'baltoy', 'claydol', 'lileep',  
'cradily', 'anorith', 'armaldo', 'feebas', 'milotic', 'castform', 'kecleon', 'shuppet', 'banette', 'mega banette', 'duskull',  
'dusclops', 'tropius', 'chimecho', 'absol', 'mega absol', 'wynaut', 'snorunt', 'glalie', 'mega glalie', 'spheal', 'sealeo',  
'walrein', 'clamperl', 'huntail', 'gorebyss', 'relicanth', 'luvdisc', 'bagon', 'shelgon', 'salamence', 'mega salamence',  
'beldum', 'metang', 'metagross', 'mega metagross', 'regirock', 'regice', 'registeel', 'latias', 'mega latias', 'latios',  
'mega latios', 'kyogre', 'primal kyogre', 'groudon', 'primal groudon', 'rayquaza', 'mega rayquaza', 'jirachi', 'deoxys'
---
## Sinnoh
'turtwig', 'grotle', 'torterra', 'chimchar', 'monferno', 'infernape', 'piplup', 'prinplup', 'empoleon', 'starly', 'staravia',  
'staraptor', 'bidoof', 'bibarel', 'kricketot', 'kricketune', 'shinx', 'luxio', 'luxray', 'budew', 'roserade', 'cranidos',  
'rampardos', 'shieldon', 'bastiodon', 'burmy', 'wormadam', 'mothim', 'combee', 'vespiquen', 'pachirisu', 'buizel', 'floatzel',  
'cherubi', 'cherrim', 'shellos', 'gastrodon', 'ambipom', 'drifloon', 'drifblim', 'buneary', 'lopunny', 'mega lopunny',  
'mismagius', 'honchkrow', 'glameow', 'purugly', 'chingling', 'stunky', 'skuntank', 'bronzor', 'bronzong', 'bonsly', 'mime jr',  
'happiny', 'chatot', 'spiritomb', 'gible', 'gabite', 'garchomp', 'mega garchomp', 'munchlax', 'riolu', 'lucario', 'mega lucario',  
'hippopotas', 'hippowdon', 'skorupi', 'drapion', 'croagunk', 'toxicroak', 'carnivine', 'finneon', 'lumineon', 'mantyke', 'snover',  
'abomasnow', 'mega abomasnow', 'weavile', 'magnezone', 'lickilicky', 'rhyperior', 'tangrowth', 'electivire', 'magmortar',  
'togekiss', 'yanmega', 'leafeon', 'glaceon', 'gliscor', 'mamoswine', 'porygon-z', 'gallade', 'mega gallade', 'probopass',  
'dusknoir', 'froslass', 'rotom', 'uxie', 'mesprit', 'azelf', 'dialga', 'palkia', 'heatran', 'regigigas', 'giratina', 'cresselia',  
'phione', 'manaphy', 'darkrai', 'shaymin', 'arceus'
---

## Unova
'victini', 'snivy', 'servine', 'serperior', 'tepig', 'pignite', 'emboar', 'oshawott', 'dewott', 'samurott', 'patrat', 'watchog',  
'lillipup', 'herdier', 'stoutland', 'purrloin', 'liepard', 'pansage', 'simisage', 'pansear', 'simisear', 'panpour', 'simipour',  
'munna', 'musharna', 'pidove', 'tranquill', 'unfezant', 'blitzle', 'zebstrika', 'roggenrola', 'boldore', 'gigalith', 'woobat',  
'swoobat', 'drilbur', 'excadrill', 'audino', 'mega audino', 'timburr', 'gurdurr', 'conkeldurr', 'tympole', 'palpitoad', 'seismitoad',  
'throh', 'sawk', 'sewaddle', 'swadloon', 'leavanny', 'venipede', 'whirlipede', 'scolipede', 'cottonee', 'whimsicott', 'petilil',  
'lilligant', 'basculin', 'sandile', 'krokorok', 'krookodile', 'darumaka', 'darmanitan', 'maractus', 'dwebble', 'crustle', 'scraggy',  
'scrafty', 'sigilyph', 'yamask', 'cofagrigus', 'tirtouga', 'carracosta', 'archen', 'archeops', 'trubbish', 'garbodor', 'zorua',  
'zoroark', 'minccino', 'cinccino', 'gothita', 'gothorita', 'gothitelle', 'solosis', 'duosion', 'reuniclus', 'ducklett', 'swanna',  
'vanillite', 'vanillish', 'vanilluxe', 'deerling', 'sawsbuck', 'emolga', 'karrablast', 'escavalier', 'foongus', 'amoonguss', 'frillish',  
'jellicent', 'alomomola', 'joltik', 'galvantula', 'ferroseed', 'ferrothorn', 'klink', 'klang', 'klinklang', 'tynamo', 'eelektrik',  
'eelektross', 'elgyem', 'beheeyem', 'litwick', 'lampent', 'chandelure', 'axew', 'fraxure', 'haxorus', 'cubchoo', 'beartic', 'cryogonal',  
'shelmet', 'accelgor', 'stunfisk', 'mienfoo', 'mienshao', 'druddigon', 'golett', 'golurk', 'pawniard', 'bisharp', 'bouffalant', 'rufflet',  
'braviary', 'vullaby', 'mandibuzz', 'heatmor', 'durant', 'deino', 'zweilous', 'hydreigon', 'larvesta', 'volcarona', 'cobalion',  
'terrakion', 'virizion', 'tornadus', 'thundurus', 'reshiram', 'zekrom', 'landorus', 'kyurem', 'keldeo', 'meloetta', 'genesect'
---
## Kalos
'chespin', 'quilladin', 'chesnaught', 'fennekin', 'braixen', 'delphox', 'froakie', 'frogadier', 'greninja', 'bunnelby', 'diggersby',  
'fletchling', 'fletchinder', 'talonflame', 'scatterbug', 'spewpa', 'vivillon', 'litleo', 'pyroar', 'flabebe', 'floette', 'florges',  
'skiddo', 'gogoat', 'pancham', 'pangoro', 'furfrou', 'espurr', 'meowstic', 'honedge', 'doublade', 'aegislash', 'spritzee', 'aromatisse',  
'swirlix', 'slurpuff', 'inkay', 'malamar', 'binacle', 'barbaracle', 'skrelp', 'dragalge', 'clauncher', 'clawitzer', 'helioptile',  
'heliolisk', 'tyrunt', 'tyrantrum', 'amaura', 'aurorus', 'sylveon', 'hawlucha', 'dedenne', 'carbink', 'goomy', 'sliggoo', 'goodra',  
'klefki', 'phantump', 'trevenant', 'pumpkaboo', 'gourgeist', 'bergmite', 'avalugg', 'noibat', 'noivern', 'xerneas', 'yveltal', 'zygarde',  
'diancie', 'mega diancie', 'hoopa', 'volcanion'
---
## Alola
'rowlet', 'dartrix', 'decidueye', 'litten', 'torracat', 'incineroar', 'popplio', 'brionne', 'primarina', 'pikipek', 'trumbeak',  
'toucannon', 'yungoos', 'gumshoos', 'grubbin', 'charjabug', 'vikavolt', 'crabrawler', 'crabominable', 'oricorio', 'cutiefly', 'ribombee',  
'rockruff', 'lycanroc', 'wishiwashi', 'mareanie', 'toxapex', 'mudbray', 'mudsdale', 'dewpider', 'araquanid', 'fomantis', 'lurantis',  
'morelull', 'shiinotic', 'salandit', 'salazzle', 'stufful', 'bewear', 'bounsweet', 'steenee', 'tsareena', 'comfey', 'oranguru',  
'passimian', 'wimpod', 'golisopod', 'sandygast', 'palossand', 'pyukumuku', 'type: null', 'silvally', 'minior', 'komala', 'turtonator',  
'togedemaru', 'mimikyu', 'bruxish', 'drampa', 'dhelmise', 'jangmo-o', 'hakamo-o', 'kommo-o', 'tapu koko', 'tapu lele', 'tapu bulu',  
'tapu fini', 'cosmog', 'cosmoem', 'solgaleo', 'lunala', 'nihilego', 'buzzwole', 'pheromosa', 'xurkitree', 'celesteela', 'kartana',  
'guzzlord', 'necrozma', 'magearna', 'marshadow', 'poipole', 'naganadel', 'stakataka', 'blacephalon', 'zeraora'
---
## Galar
'grovyle', 'thwackey', 'rillaboom', 'scorbunny', 'raboot', 'cinderace', 'sobble', 'drizzile', 'inteleon', 'skwovet', 'greedent',  
'rookidee', 'corvisquire', 'corviknight', 'blipbug', 'dottler', 'orbeetle', 'nickit', 'thievul', 'gossifleur', 'eldegoss', 'wooloo',  
'dubwool', 'chewtle', 'drednaw', 'yamper', 'boltund', 'rolycoly', 'carkol', 'coalossal', 'applin', 'flapple', 'appletun', 'silicobra',  
'sandaconda', 'cramorant', 'arrokuda', 'barraskewda', 'toxel', 'toxtricity', 'sizzlipede', 'centiskorch', 'clobbopus', 'grapploct',  
'sinistea', 'polteageist', 'hatenna', 'hattrem', 'hatterene', 'impidimp', 'morgrem', 'grimmsnarl', 'obstagoon', 'perrserker', 'cursola',  
'sirfetchd', 'mr rime', 'runerigus', 'milcery', 'alcremie', 'falinks', 'pincurchin', 'snom', 'frosmoth', 'stonjourner', 'eiscue',  
'indeedee', 'morpeko', 'cufant', 'copperajah', 'dracozolt', 'arctozolt', 'dracovish', 'arctovish', 'duraludon', 'dreepy', 'drakloak',  
'dragapult', 'zacian', 'zamazenta', 'eternatus', 'kubfu', 'urshifu', 'g-max urshifu', 'zarude', 'regieleki', 'regidrago', 'glastrier',  
'spectrier', 'calyrex'
---
## Paldea
'sprigatito', 'floragato', 'meowscarada', 'fuecoco', 'crocalor', 'skeledirge', 'quaxly', 'quaxwell', 'quaquaval', 'lechonk', 'oinkologne',  
'tarountula', 'spidops', 'nymble', 'lokix', 'pawmi', 'pawmo', 'pawmot', 'tandemaus', 'maushold', 'fidough', 'dachsbun', 'smoliv',  
'dolliv', 'arboliva', 'squawkabilly', 'nacli', 'naclstack', 'garganacl', 'charcadet', 'armarouge', 'ceruledge', 'tadbulb', 'bellibolt',  
'wattrel', 'kilowattrel', 'maschiff', 'mabosstiff', 'shroodle', 'grafaiai', 'bramblin', 'brambleghast', 'toedscool', 'toedscruel',  
'klawf', 'capsakid', 'scovillain', 'rellor', 'rabsca', 'flittle', 'espathra', 'tinkatink', 'tinkatuff', 'tinkaton', 'wiglett',  
'wugtrio', 'bombirdier', 'finizen', 'palafin', 'varoom', 'revavroom', 'cyclizar', 'orthworm', 'glimmet', 'glimmora', 'greavard',  
'houndstone', 'flamigo', 'cetoddle', 'cetitan', 'veluza', 'dondozo', 'tatsugiri', 'annihilape', 'clodsire', 'farigiraf', 'dudunsparce',  
'kingambit', 'great tusk', 'scream tail', 'brute bonnet', 'flutter mane', 'slither wing', 'sandy shocks', 'iron treads', 'iron bundle',  
'iron hands', 'iron jugulis', 'iron moth', 'iron thorns', 'frigibax', 'arctibax', 'baxcalibur', 'gimmighoul', 'gholdengo', 'wo-chien',  
'chien-pao', 'ting-lu', 'chi-yu', 'roaring moon', 'iron valiant', 'koraidon', 'miraidon', 'walking wake', 'iron leaves', 'dipplin',  
'poltchageist', 'sinistcha', 'okidogi', 'munkidori', 'fezandipiti', 'ogerpon', 'archaludon', 'hydrapple', 'gouging fire', 'raging bolt',  
'iron boulder', 'iron crown', 'terapagos', 'pecharunt'
