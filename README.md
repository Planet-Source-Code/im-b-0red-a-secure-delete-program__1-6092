<div align="center">

## A\+ Secure Delete Program


</div>

### Description

this code takes a file in which you specify, overwrites it 21 times, then deletes it all in about 1-2 seconds depending on the size of the file, i have seen other secure delete programs here but i think that this is for the most part more efficient, it overwrites it 20 times with a bunch of random characters, then for the 21st overwrite it puts 10 bytes in, decreasing the files size to a minimum (almost), after it has overwritten the file 21 times, it deletes it using the 'Kill' statement. as far as i know this program deletes the file clear off your hard disk, maybe a program like norton utilities could recal i but i couldn't find any traces of the deleted file.

P.S. im looking for any comments/suggestions to improve the eficiency of this program.
 
### More Info
 
it deletes a file, just don't delete any system files and you'll be alright!


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Im\_\[B\]0ReD](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/im-b-0red.md)
**Level**          |Intermediate
**User Rating**    |4.0 (8 globes from 2 users)
**Compatibility**  |VB 5\.0, VB 6\.0
**Category**       |[Files/ File Controls/ Input/ Output](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/files-file-controls-input-output__1-3.md)
**World**          |[Visual Basic](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/visual-basic.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/im-b-0red-a-secure-delete-program__1-6092/archive/master.zip)





### Source Code

```
Function DeleteFile(Path As String)
'This is an extremely quick file delete developed
'by me in about 5 minutes.
'overwrites the file 21 times then deletes it
'clean off your disk :-)
Dim i As Integer 'variable for times to overwrite
Dim Data1 As String, Data2 As String, Data3 As String, Data4 As String, Data5 As String, Data6 As String, Data7 As String, Data8 As String, Data9 As String, Data10 As String, Data11 As String, Data12 As String, Data13 As String, Data14 As String, Data15 As String, Data16 As String, Data17 As String, Data18 As String, Data19 As String, Data20 As String
'^^^ all 20 data variables, which hold the information to overwrite the file with
Dim FinalByte As Byte 'just a byte to do the final overwrite with
Data1 = Chr(85) 'the variables information
Data2 = Chr(170) 'the variables information
Data3 = Chr(74) 'the variables information
Data4 = Chr(99) 'the variables information
Data5 = Chr(71) 'the variables information
Data6 = Chr(92) 'the variables information
Data7 = Chr(101) 'the variables information
Data8 = Chr(112) 'the variables information
Data9 = Chr(1) 'the variables information
Data10 = Chr(61) 'the variables information
Data11 = Chr(97) 'the variables information
Data12 = Chr(119) 'the variables information
Data13 = Chr(86) 'the variables information
Data14 = Chr(79) 'the variables information
Data15 = Chr(109) 'the variables information
Data16 = Chr(72) 'the variables information
Data17 = Chr(90) 'the variables information
Data18 = Chr(0) 'the variables information
Data19 = Chr(255) 'the variables information
Data20 = Chr(212) 'the variables information
Open Path For Binary Access Write As #1 'open the path so we can overwrite it
For i = 1 To 10 'a loop
  Put #1, , Data1 'overwrite
Next i 'stop loop
For i = 1 To 10 'another loop
  Put #1, , Data2 'overwrite
Next i 'stop loop
For i = 1 To 10 'another loop
  Put #1, , Data3 'overwrite
Next i 'stop loop
For i = 1 To 10 'another loop
  Put #1, , Data4 'overwrite
Next i 'stop loop
For i = 1 To 10 'another loop
  Put #1, , Data5 'overwrite
Next i 'stop loop
For i = 1 To 10 'Im sure you get the point from here on!
'that this is just the overwriting stage!
  Put #1, , Data6
Next i
For i = 1 To 10
  Put #1, , Data7
Next i
For i = 1 To 10
  Put #1, , Data8
Next i
For i = 1 To 10
  Put #1, , Data9
Next i
For i = 1 To 10
  Put #1, , Data10
Next i
For i = 1 To 10
  Put #1, , Data11
Next i
For i = 1 To 10
  Put #1, , Data12
Next i
For i = 1 To 10
  Put #1, , Data13
Next i
For i = 1 To 10
  Put #1, , Data14
Next i
For i = 1 To 10
  Put #1, , Data15
Next i
For i = 1 To 10
  Put #1, , Data16
Next i
For i = 1 To 10
  Put #1, , Data17
Next i
For i = 1 To 10
  Put #1, , Data18
Next i
For i = 1 To 10
  Put #1, , Data19
Next i
For i = 1 To 10
  Put #1, , Data20
Next i
For i = 1 To 10 'the final loop
  Put #1, , FinalByte 'the final overwrite
Next i 'stop final loop
Close #1 'close the file
Kill Path 'delete it
MsgBox "All Done Wiping The File!", vbInformation + vbOKOnly, "All Done!" 'duh
End Function
```

