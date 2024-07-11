# Import string
    U0JBRR+LCAAAAAAABADNlstu2zAQRfcB8g+CEQMtGhrU28ouSJB01UVTpIu6i5E4tIlSlEpRtoMg/15K8ku2EwRBAnRlcO5ohjxzLerx9MRxBnPUlSjU4MLxz9uAyMtCm/v9cC6UyOt8Gx/QkTfyBysVDdjYY7OwSwU5NikMwcyyolYGdZdpRajNrNCNfAOco37YKNu9DNwRHdGNwLDKtCjNStwtVXyv1WW2UlQtZSM9dbti0NsVtGmVjfzqIs5aamXBmtpA/Qg4MBK6/pgEHuMkidKI8CSI/MT1Eu6n6/7tY39rrHHVezeOClKJTU2ja+wpy0zWDG90kX8VlSksgQuHg6x6WWuGt6hQi8xpWTp7MNvMqS7qskm9blOuupSqlwNyAQ+VZXWslQbFinxD8UDPCpXVWqMyx1SjxXTa9LNcf/d6HvLeY96mcSHbg15fTCZ3pua8+dEI1nHTyWRrocnk0loQ5E+UcjJRdZ6iHpml2T1nW7AEXeE9aNEMoDqy5Y13fjyUeDigXTe4LPFdOiYQ+0ACAEoSdxyThCVRkMVhGqXhQf8FiumsQWUtvK+ZrqNLabQvrce4Z6RWe9ZM3V4Vw2XTbzf+dP4S9PkKz7eVyxQuWsgHh5mDbO09OMvtID4NpVBIh1/cz2cHqa8iOg55hGM/JiH1KAl4zMiYuoxwCL2AszDA/v/r1UQ9//2Buq8H+u4uNrhsTjwYrkczPARelqjYcwbveLMgBS8Gn1A3tg6mgU9S5iNhGHB/7MVJwr238P4A2t5H02aiKiU8vIjb2fJ2UlmklWOfqkQJBpkjlGNm6CxstTcNA4GPE+olJAGI7TC8gADwkEQpZYxiGHv+/zIMvzeM7eLIG/62aXb4+s8KKaGskO3oa3lVcJ3fXaK9EvbxPLf3Uj+4wLQqsj9o7lDP9+6crXglhb2r+qIR+Tq//UI4PXn6B8tdzhgBCQAA

# How does it work?
This import only contains 1 action:
**Generic death counter** - reads a number from a file, increments it, puts the incremented number back in the file, then updates another file with a formatted string with the new number.

You need to prepare the following:
1. A folder to hold your death counter files for a certain game.
2. A text file to hold the number of deaths named **number.txt** containing just the number 0 and no other spaces or new lines.
3. A text file to hold the string that will be shown on stream named **display.txt**.
4. A Text source on your OBS scene with the **Read from file** option pointing to **display.txt**.

What you need to change in Streamer.bot:
- Read lines (number.txt) -> point this to the **number.txt** you created earlier.
- Write to file (number.txt) -> point this to the **number.txt** you created earlier.
- Write to file (display.txt) -> point this to the **display.txt** you created earlier and change the text to something appropriate for your game. For example, the text provided in the import was for Animal Well. Just remember to put %newcount% where you want the number to appear like in the example:
- `%newcount% blobs dissipated in the well`

Once you're done updating the actions, you can set it to trigger however you like. I use a Stream Deck button to trigger the Streamer.bot action. You could also use a text command and restrict it to mods and broadcaster only to avoid having the death counter added to inadvertently.

You can duplicate the action and make a new set of files in another folder to have different death counts for different games.
