# theencryptiontool
The Encryption Tool V3
                            *********************************The Encryption Tool *********************************
                            *********************************   By: Khalil A     *********************************

                                                FOR PERSONAL USE ONLY, MEANT FOR DEMO PURPOSES


Summary:

The Encryption Tool depends on a key file, ''key.txt'' (can be renamed but the program only looks for a text file with this exact name), 
automatically generated on first launch or when the file is not found within the immediate directory of the program. Each key is totally 
unique upon creation and is used for encryption/decryption by the user, it is recommended to be stored in a separate location, such as 
cloud storage when usage is over for later use. A set of options is presented for the user to choose from.

How To:

Execute the program and a key.txt file will be generated, you will then be prompted to close the program and re-open it into Encryption/
Decryption mode, from there you are given options to choose from to move forward.

When you're done using the program, the key.txt file (or its contents) can be moved anywhere for safe keeping and paired with the program 
later on, by copy/paste or dragging the key.txt file into the same directory as the main Encryption Tool.

The tool itself is totally portable, just the .exe is needed to run if no existing key file has been created.

HOW IT WORKS:

when a new key is generated, a random set of numbers is created, 70 of them to represent the total uppcase + lowercase alphabet along with numbers 0-9 and a few symbols,
thee random numbers are then spaced inside the key.txt file according to their size:
EX: if numbers 4 1 3 6 are generated, then in the key.txt file they would be
4nnnn1n3nnn6nnnnnn where 'n' represents a randomly generated number 0-9 solely created to be used as padding between the values, then, after
the 70 + n long string of numbers is complete, the alphabet begins,
we begin by scrambling the true set of 70 alphanumeric values by randomly switching two values 70 / 2 = 35 times.
once the random switch is complete, a scrambled value is converted to its ASCII and then multipled by a static value that can be any number within a range to
where the resultant is 5 digits long, so any value that allows for final result between 10,000 and 99,999, in this program the value is 562 but this
could be changed later to be auto generated and stored in the key file also, but in the sake of keeping at least one central value
seperate from the key file and compiled within the program instead it will be static for now, this value is then stored beginning after the values in the
key file stated above, and they are padded using those same values (4 1 3 6), so if we have 56,753 then we would have 56753nnnn then followed by another 
scrambled ASCII multiple such as 46,743 so 56753nnnn46743n and so on until all values are inserted.
this is what makes up a unique key file.

