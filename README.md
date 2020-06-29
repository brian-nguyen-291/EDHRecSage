# EDHRecSage
Python web scraping tool for retrieving EDHRec's "average deck" decklist for any given commander

### Requires:
 - **Python 3** (https://www.python.org/downloads/)
 - **requests-html** (https://pypi.org/project/requests-html/) - NOTE: Incompatible with Windows Subsystem for Linux.

### CLI Instructions:
EDHRecSage takes either 1 argument or 3:
 - **Commander Name**: Self explanatory, encase in quotation marks for proper parsing.
 - **Random**: Just "Random", simple grab of any commander available (WARNING: Can get commanders from Legends. You have been warned.).
 - **Random, Color(s), and Popularity**:
   - **Random**: Just "Random" as before.
   - **Color(s)**: "Any", any combination of colors (WUBRG), "Colorless", or a known pairing nickname ("Jund", "Azorius", "Mardu", etc.)
   - **Popularity**: "Low", "Medium", or "High" based on the number of decklists available (ranges are relatively arbitrary: (1 to 99), (100 to 699), and (700 to 99999) respectively.). Also supports the "Any" option (1 to 99999).

CLI Usage Examples:
 - python ./edhrecsage Random
 - python ./edhrecsage Random Any Any
 - python ./edhrecsage Random Golgari Medium
 - python ./edhrecsage Random Any Low
 - python ./edhrecsage Random WUBRG Medium
 - python ./edhrecsage Random Colorless High
 - python ./edhrecsage Random Jund Medium
 - python ./edhrecsage "Hogaak, Arisen Necropolis"
 
 ### Example Output (in the same directory as the script):
 - "maelstrom-wanderer.cod"
 - "hogaak-arisen-necropolis.cod"
