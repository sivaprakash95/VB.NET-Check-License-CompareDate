# VB.NET-Check-License-CompareDate
VB.NET Project for check license and compare date

How to check license and compare date .NET
SOFT FRESH BOOKS
Hi friends today am explain about how to check date in vb.net. It helps to validate licensing date in our software And It helps to compare the date in vb.net. Okay, here i create 3 functions
1.	CheckLicenceByValue() - used to check the license of our software
2.	CompareDate() - used to compare the date are equal 
3.	CompareDateByFormat() - used to compare the date are equal by string value
This is my design, it show the value return by above 3 function

CODE
Public Class Form1
    Function CheckLicenceByValue() As Boolean
        Dim dateval As Integer = Val(Date.Today.Year.ToString() + Date.Today.Month.ToString() + Date.Today.Day.ToString())
        Return dateval < 2020814
    End Function

    Function CompareDate() As Boolean
        Dim mydate As Date = New Date(2020, 8, 14)
        Return Date.Compare(Date.Today, mydate)
    End Function

    Function CompareDateByFormat() As Boolean
        Dim mydate As String = "2020-08-14"
        Dim sysdate As String = Date.Today.ToString("yyyy-MM-dd")
        Return mydate <> sysdate
    End Function

    Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        lbl1.Text += " : " + CheckLicenceByValue().ToString()
        lbl2.Text += " : " + CompareDate().ToString()
        lbl3.Text += " : " + CompareDateByFormat().ToString()
    End Sub

    Private Sub checklicence_Click(sender As Object, e As EventArgs) Handles checklicence.Click
        If CheckLicenceByValue() = False Then
            End
        End If
    End Sub
End Class

VIDEO
https://www.youtube.com/watch?v=sa1LHJ5aNAk&list=PLPPKxKUjG6RPfs411s3YOY7EILA8wvpuL

STEPS
1.
Function CheckLicenceByValue() As Boolean
Dim dateval As Integer = Val(Date.Today.Year.ToString() + Date.Today.Month.ToString() + Date.Today.Day.ToString())
Return dateval < 2020814
End Function
In here i concat string of the year, month, day at today and convert it to integer then i check it
The date value should be "yyyyMd" Format. For Example july month : 202071 to 2020731

2.
Function CompareDate() As Boolean
Dim mydate As Date = New Date(2020, 8, 14)
Return Date.Compare(Date.Today, mydate)
End Function
In here i just compare the date value of my given date and system today date

3.
Function CompareDateByFormat() As Boolean
        Dim mydate As String = "2020-08-14"
        Dim sysdate As String = Date.Today.ToString("yyyy-MM-dd")
        Return mydate <> sysdate
    End Function
In here i compare the date value in string format

4.
Private Sub Form1_Load(sender As Object, e As EventArgs) Handles MyBase.Load
        lbl1.Text += " : " + CheckLicenceByValue().ToString()
        lbl2.Text += " : " + CompareDate().ToString()
        lbl3.Text += " : " + CompareDateByFormat().ToString()
End Sub
In here I add the return value by the function into the label
Note: Change date for different results.

5.
Private Sub checklicence_Click(sender As Object, e As EventArgs) Handles checklicence.Click
        If CheckLicenceByValue() = False Then
            End
        End If
End Sub
In here, when you click check lisence button the program will stop according to the valid date.
Note: Normally this is the way to check license in more soft wares

Thank you friends. Do better to check license in your software

For More .NET Videos: https://www.youtube.com/watch?v=sa1LHJ5aNAk&list=PLPPKxKUjG6RPfs411s3YOY7EILA8wvpuL

