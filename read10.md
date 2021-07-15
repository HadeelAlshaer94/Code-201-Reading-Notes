# Error Handling & Debugging
![Error](https://0701.static.prezi.com/preview/v2/h3j5rflrkheepc5js3m7tae7e76jc3sachvcdoaizecfr3dnitcq_3_0.png)


## EXECUTION CONTEXTS
##### The JavaScript interpreter uses the concept of execution contexts. There is one global execution context; plus, each function creates a new new execution context. They correspond to variable scope. 

### EXECUTION CONTEXT
##### Every statement in a script lives in one of three execution contexts:
- GLOBAL CONTEXT: Code that is in the script, but not in a function. There is only one global context in any page.
- FUNCTION CONTEXT: Code that is being run within a function. Each function has its own function context.
- EVAL CONTEXT (NOT SHOWN): Text is executed like code in an internal function called eva l {) (which is not covered in this book).

### VARIABLE SCOPE
##### The first two execution contexts correspond with the notion of scope (which you met on p98):
- GLOBAL SCOPE: If a variable is declared outside a function, it can be used anywhere because it has global scope. If you do not use the var keyword when creating a variable, it is placed in global scope.
- FUNCTION-LEVEL SCOPE: When a variable is declared within a function, it can only be used within that function. This is because it has function-level scope.

### ERROR OBJECTS CONTINUED
##### SYNTAX IS NOT CORRECT This is caused by incorrect use of the rules of the language. It is often the result of a simple typo.

### MISMATCHING OR UNCLOSED QUOTES
```html
document .write ("Howdy");
SyntaxError: Unexp ec t ed EOF
```

### MISSING CLOSING BRACKET
```html
document .getElementByid('page')
SyntaxErr or : Expected token ' )
```

### MISSING COMMA IN ARRAY
```html
var l ist = ['Item 1', 'Item 2 ' l 'rtem 3'];
SyntaxError: Expected token ']'
```

### MALFORMED PROPERTY NAME
```html
user = { f i rstl name: "Ben", lastName: "Lee"};
Synt axError: Expected an identifier but
found 'name ' instead
```


![d](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSIjBYau1M7JHAAM3xyTF1fbRhZqZfvJqKS6Q&usqp=CAU)

### Client-Side Script with a Syntax Error
##### Syntax errors at compile time are usually the easiest to trace and rectify. When the script loads, it calls the scripting engine to compile the code. If the VBScript engine encounters a syntax error, it cannot compile the program and instead displays an error message. For instance, an attempt to run the client-side script shown in Example 4.1 produces the error message shown in Figure 4.1. In this case, it’s very easy to identify the source of the error: in the call to the LCase function, the closing parenthesis is omitted.

```html
<HTML>
<HEAD>
<TITLE>Syntax Error</TITLE>
<SCRIPT LANGUAGE="vbscript">
Sub cmdButton1_OnClick
  Alert LCase("Hello World"
End Sub
</SCRIPT>
</HEAD>
<BODY BGCOLOR="white">
<INPUT TYPE="button" NAME="cmdButton1" VALUE="OK">
</BODY>
</HTML>
```

### ASP Page with a Syntax Error
##### This is a fairly standard ASP message display. Aside from the fact that it is reported as a runtime error, note, first of all, that the error code (which is expressed as a hexadecimal number in this case) appears to be meaningless. Second, the error description, though accurate, is not a model of clarity. The line number causing the error, however, is correctly identified, and if we examine it while keeping in mind the obscure description of the error, we’ll quickly see that we’ve simply misspelled the name of the ASP intrinsic Request object. Hence, ASP was looking for—and failed to find—an object named “Requet” that had a property named ServerVariables.

```html
<HTML>
<HEAD>
<TITLE>ASP Syntax Error</TITLE>
</HEAD>

<BODY>
<SCRIPT LANGUAGE="VBScript" RUNAT="Server">

Dim sBrowser

sBrowser = Requet.ServerVariables("HTTP_USER-AGENT")

</SCRIPT>

<H2><CENTER>Welcome to Our Web Page!</CENTER></H2>
We are always happy to welcome surfers using <%= sBrowser %>
</BODY>
</HTML>

```



### Syntax errors at runtime
##### Very often, a syntax error in VBScript only appears at runtime. Although the VBScript engine can successfully compile the code, it cannot actually execute it. (Note, though, that you may not actually be able to tell the difference between compile-time and runtime behavior in a relatively short script, since these two behaviors occur one after the other.) Example 4.3 shows a part of an ASP page that, among other things, attempts to determine whether an ISBN number is correct. But attempting to access this page generates a runtime error.


```html
<HTML>
<HEAD>
<TITLE>Verifying an ISBN</TITLE>
</HEAD>
<BODY>
<SCRIPT LANGUAGE="VBScript" RUNAT="Server">

Dim sCheckSumDigit, sCheckSum

Private Function VerifyISBN(sISBN)

Dim iPos, iCtr, iCheckSum
Dim lSum
Dim sDigit

iPos = 1
sCheckSumDigit = Right(Trim(sISBN), 1)

' Make sure checksum is a valid alphanumeric
If Instr(1,"0123456789X", sCheckSumDigit) = 0 Then
   Response.Write "Exiting function...<P>"
   Exit Function
End If

' Calculate checksum
For iCtr = 1 to Len(sISBN) - 1
   sDigit = Mid(sISBN, iCtr, 1)
   If IsNumeric(sDigit) Then
      lSum = lSum + (11 - iPos) * CInt(sDigit)          
      iPos = iPos + 1
   End If
Next
iCheckSum = 11 - (lSum Mod 11)   
Select Case iCheckSum
   case 11
      sCheckSum = "0"
   case 10
      sCheckSum = "X"
   case else
      sCheckSum = CStr(iCheckSum)
End Select
' Compare with last digit
If sCheckSum = sCheckSumDigit Then
   VerifyISBN = True
End If
   
End Function

</SCRIPT>

<H2><CENTER>Title Information</CENTER></H2>
Title: <%=Request.Form("txtTitle") %> <P>
ISBN: 
<%
   sISBN = Request.Form("txtISBN")
   If Not VerifyIBN(sISBN) Then
      Response.Write "The ISBN you've entered is incorrect."
   Else
      Response.Write sISBN
   End If
%>

</BODY>
</HTML>

```


