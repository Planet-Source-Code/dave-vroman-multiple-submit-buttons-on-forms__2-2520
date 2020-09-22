<div align="center">

## Multiple Submit Buttons On Forms


</div>

### Description

This script allows multiple forms to support multiple submit buttons that do different things. The case in point one button does a submit while the other button does a named PopUp (selecting another option from the original window does not open a new window but goes back to the PopUp window)

It is currently being selected to do a popup of a map so that the end user can make an informed decision of the addresses displayed in the form and select the correct one.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Dave Vroman](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/dave-vroman.md)
**Level**          |Intermediate
**User Rating**    |4.5 (18 globes from 4 users)
**Compatibility**  |
**Category**       |[Controls/ Forms/ Graphics/ Menus](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/controls-forms-graphics-menus__2-59.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/dave-vroman-multiple-submit-buttons-on-forms__2-2520/archive/master.zip)





### Source Code

```
<font size=3>
<pre>&lt;HTML&gt;&lt;HEAD&gt;
&lt;TITLE&gt;Multiple Submit Buttons On Forms&lt;/TITLE&gt;
&lt;/HEAD&gt;&lt;BODY&gt;
&lt;SCRIPT LANGUAGE=&quot;JavaScript&quot;&gt;&lt;!--
function DoSubmit(url, inVal, name, FormsNum) {
 if ( inVal == 'Pop' ) {
  popupWin = window.open(url, name);
 } else {
// Be careful of the forms number
  document.forms[FormsNum].action = url
  document.forms[FormsNum].method = &quot;POST&quot;
  document.forms[FormsNum].submit()
 }
}
//--&gt;
&lt;/SCRIPT&gt;
&lt;FORM&gt;
&lt;CENTER&gt;
&lt;SELECT SIZE=5&gt;
&lt;OPTION VALUE=0 SELECTED&gt;Option 1
&lt;OPTION VALUE=1&gt;Option 2
&lt;OPTION VALUE=2&gt;Option 3
&lt;OPTION VALUE=3&gt;Option 4
&lt;OPTION VALUE=4&gt;Option 5
&lt;/SELECT&gt;
&lt;BR&gt;
&lt;INPUT TYPE=&quot;BUTTON&quot; VALUE=&quot; Submit 1 &quot;
  OnClick=&quot;javascript:DoSubmit('a.htm','OK',' ',0)&quot;&gt;
&lt;INPUT TYPE=&quot;BUTTON&quot; VALUE=&quot;Show Popup 1&quot;
  OnClick=&quot;javascript:DoSubmit('b.htm','Pop','PopWinName',0)&quot;&gt;
&lt;/CENTER&gt;
&lt;/FORM&gt;
&lt;FORM&gt;
&lt;CENTER&gt;
&lt;SELECT SIZE=5&gt;
&lt;OPTION VALUE=0 SELECTED&gt;Option 1
&lt;OPTION VALUE=1&gt;Option 2
&lt;OPTION VALUE=2&gt;Option 3
&lt;OPTION VALUE=3&gt;Option 4
&lt;OPTION VALUE=4&gt;Option 5
&lt;/SELECT&gt;
&lt;BR&gt;
&lt;INPUT TYPE=&quot;BUTTON&quot; VALUE=&quot; Submit 2 &quot;
  OnClick=&quot;javascript:DoSubmit('c.htm','OK',' ',1)&quot;&gt;
&lt;INPUT TYPE=&quot;BUTTON&quot; VALUE=&quot;Show Popup 2&quot;
  OnClick=&quot;javascript:DoSubmit('d.htm','Pop','PopWinName',1)&quot;&gt;
&lt;/CENTER&gt;
&lt;/FORM&gt;
&lt;/BODY&gt;&lt;/HTML&gt;
&lt;html&gt;&lt;body&gt;
&lt;!-- Save this as a.htm, b.htm, c.htm and d.htm --&gt;
This is a.htm
&lt;/body&gt;&lt;/html&gt;
</pre></font>
```

