This game was created to solve many dilemmas in the educational world. However, there were several technicalities that needed to be solved.:
1. How can it be used on many, if not sall machines. This game was created using powerpoint because most machines have that installed in one version or another
2. The hyperlinks. This game has over 900 hyperlinks within it originally. Over the subsequent years, updates to Powerpoint allowed that number to fall in half. 
3. Because of the shear number of hyperlinks, I used the foillowing macro code to keep track of all of them:
Sub viewing()

Dim osld As Slide
Dim oshp As Shape
Dim strMessage As String
On Error Resume Next
For Each osld In ActivePresentation.Slides
For Each oshp In osld.Shapes
Err.Clear
Debug.Print oshp.LinkFormat.SourceFullName
If Err = 0 Then
strMessage = strMessage & "Slide: " & osld.SlideIndex & _
"  Shape: '" & oshp.Name & "' Is Linked" & vbCrLf
End If
Next
End Sub

4. Originally, it also ran the macro to link Excel to this powerpoint presentation to change score where a student would keep track of the scoring on an excel sheet which is formulated to tabulate the score there and display it on the presentation as the group played. 
5. Again, the updates to Powerpoint over the years negate3d the need for the macro and now the same is accomplished through more links between PowerPoint and Excel
