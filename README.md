# PlayStation 5 Backwards Compatibility Status

Sony has an API for retrieving the backward compatibility status of PS4 titles when played on a PS5 system. This API is directly utilised by https://library.playstation.com/ for displaying the status against the titles in your library, and for determining whether or not the option to allow you to download it to a PS5 should be available. 

This repository contains a extract of responses from this API created by submitting known PS4 title IDs (ie. the CUSAxxxxx codes) to it.

This data can be viewed in a friendly table format at https://andshrew.github.io/supreme-enigma/ courtesy of [GitHub Pages](https://pages.github.com/) and [DataTables](https://datatables.net/)

The raw JSON data file can be accessed [here](https://raw.githubusercontent.com/andshrew/supreme-enigma/master/docs/PS5-BC-Status.json)

The API can return one of three statuses for a title.

| Status | Description |
| --- | --- |
| COMPATIBLE | "To play this game on PS5, your system may need to be updated to the latest system software. Although this game is playable on PS5, some features available on PS4 may be absent" |
| BOOTABLE | "When playing on PS5, this game may exhibit errors or unexpected behaviour and some features available on PS4 may be absent. To play this game on PS5, your system may need to be updated to the latest system software" |
| NOT_COMPATIBLE | Only playable on PS4 |

**Note**
1. These descriptions have been sourced from the PlayStation Store.
2. Due to running a list of known PS4 title IDs through the API to generate this extract there are many titles which are old alpha, beta or demo titles which do not exist in this API and so return no response. All such titles are *not compatible* when played on the PS5 but as they are not explicitly listed as such by the API I have assigned them an N/A status (ie. they do not exist in the API).