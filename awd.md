#### 1. Write the program for the following: 
##### a. Create an application to print on screen the output of adding, subtracting, multiplying and dividing two numbers entered by the user in C#. 


 Calculator.aspx 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Calculator.aspx.cs" 
Inherits="WebApplication6.WebForm1" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
</head> 
<body style="font-family: 'Comic Sans MS'; font-size: x-large"> 
<form id="form1" runat="server"> 
<div style="height: 689px"> 
<br /> 
&nbsp;&nbsp; 
<asp:Label ID="Label1" runat="server" Text="Enter number 1: "></asp:Label> 
&nbsp;&nbsp; 
<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox> 
<br /> 
&nbsp;&nbsp; 
<br /> 
&nbsp;&nbsp; 
<asp:Label ID="Label2" runat="server" Text="Enter number 2: "></asp:Label> 
&nbsp;&nbsp; 
<asp:TextBox ID="TextBox2" runat="server"></asp:TextBox><br /><br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Button ID="Button1" runat="server" Height="43px" Text=" + " 
Width="66px" onclick="Button1_Click" />  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Button ID="Button5" runat="server" Height="43px" Text=" - " 
Width="66px" onclick="Button5_Click" /><br /><br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Button ID="Button6" runat="server" Height="43px" Text=" * " 
Width="66px" onclick="Button6_Click" /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Button ID="Button7" runat="server" Height="43px" Text=" / " 
Width="66px" /><br /><br />&nbsp; 
<asp:Label ID="Label3" runat="server" Text="Result: "></asp:Label>&nbsp; 
<asp:TextBox ID="TextBox3" runat="server" Height="22px" Width="321px"></asp:TextBox> 
</div> 
</form> 
</body> 
</html> 
```

Calci.aspx.cs:

```
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
namespace WebApplication6 
{ 
    public partial class WebForm1 : System.Web.UI.Page 
    { 
        protected void Page_Load(object sender, EventArgs e) 
        { 
        } 
        protected void Button1_Click(object sender, EventArgs e) 
        { 
            int add; 
            add = Convert.ToInt32(TextBox1.Text) + Convert.ToInt32(TextBox2.Text); 
            TextBox3.Text = "Addition: " + add; 
        } 
        protected void Button5_Click(object sender, EventArgs e) 
        { 
            int sub; 
            sub = Convert.ToInt32(TextBox1.Text) - Convert.ToInt32(TextBox2.Text); 
            TextBox3.Text = "Subtraction: " + sub; 
        } 
       protected void Button6_Click(object sender, EventArgs e) 
        { 
            int mul; 
            mul = Convert.ToInt32(TextBox1.Text) * Convert.ToInt32(TextBox2.Text); 
            TextBox3.Text = "Multiplication: " + mul; 
        } 
        protected void Button7_Click(object sender, EventArgs e) 
        { 
            int div; 
            div = Convert.ToInt32(TextBox1.Text) / Convert.ToInt32(TextBox2.Text); 
            TextBox3.Text = "Division: " + div; 
        } 
    } 
}
```
##### b. Create an application to print Floyd’s triangle till n rows in C#. 

floydTriangle.aspx: 
``` 
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="floydTriangle.aspx.cs" 
Inherits="WebApplication6.WebForm2" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
</head> 
<body style="height: 558px; font-family: 'Comic Sans MS'; font-size: xx-large;"> 
<form id="form1" runat="server"> 
<div style="height: 600px"><br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&n
 bsp;&nbsp; 
<asp:Label ID="Label1" runat="server" Text="Floyd's Triangle."></asp:Label><br /><br /> 
&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Label ID="Label2" runat="server" Text="Enter number of rows: "></asp:Label> 
&nbsp;<asp:TextBox ID="TextBox1" runat="server" Height="38px" Width="184px"></asp:TextBox> 
<br /><br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&n
 bsp;&nbsp; 
<asp:Button ID="Button1" runat="server" Height="42px" Text="Result" 
Width="301px" onclick="Button1_Click" /><br />&nbsp;<br /> 
<asp:Label ID="Label3" runat="server" Text="Triangle"></asp:Label> 
<br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
</div> 
</form> 
</body> 
</html>
```
floydTriangle.aspx.cs: 
```
using System; 
using System.Text; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
namespace WebApplication6 
{ 
    public partial class WebForm2 : System.Web.UI.Page 
    { 
        protected void Page_Load(object sender, EventArgs e) 
        { 
        } 
        protected void Button1_Click(object sender, EventArgs e) 
        { 
            int numofrows = Convert.ToInt32(TextBox1.Text); 
            int number = 1; 
            StringBuilder sb = new StringBuilder(); 
            for (int i = 1; i <= numofrows; i++) 
            { 
                for (int j = 1; j <= i; j++) 
                { 
                    sb.Append(number + " "); 
                    number++; 
                } 
                sb.Append("<br/>"); 
            } 
            Label3.Text = sb.ToString(); 
        } 
    } 
}
```
#### 2. Write the program for the following: 
##### a. Create an application to demonstrate the concepts boxing and unboxing. 

BoxedUnboxed.aspx:

```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="BoxedUnboxed.aspx.cs" 
Inherits="WebApplication6.WebForm3" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
</head> 
<body style="height: 602px; font-family: 'MS UI Gothic'; font-size: xx-large;"> 
<form id="form1" runat="server"> 
<div style="height: 609px"> 
<br /> 
&nbsp;&nbsp;&nbsp; 
<asp:Label ID="Label1" runat="server" Text="Enter the value: "></asp:Label> 
&nbsp;&nbsp;&nbsp; 
<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox> 
<br /> 
&nbsp;<br /> 
&nbsp;&nbsp; 
<asp:Button ID="Button1" runat="server" Height="31px" Text="Print Boxed and unboxed value." 
Width="379px" onclick="Button1_Click" /><br /><br />&nbsp; 
<asp:Label ID="Label2" runat="server" Text="Label"></asp:Label><br /><br />&nbsp; 
<asp:Label ID="Label3" runat="server" Text="Label"></asp:Label> 
</div> 
</form> 
</body> 
</html>
```
BoxedUnboxed.aspx.cs: 
```
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
namespace WebApplication6 
{ 
    public partial class WebForm3 : System.Web.UI.Page 
    { 
        protected void Page_Load(object sender, EventArgs e) 
        { 
        } 
        protected void Button1_Click(object sender, EventArgs e) 
        { 
            int valuetype = Convert.ToInt32(TextBox1.Text); 
            object boxed = valuetype; 
            Label2.Text = "Boxed Value: " + boxed; 
            int unboxed = (int)boxed; 
            Label3.Text = "Unboxed value: " + unboxed; 
        } 
    }    
 } 
 ```

##### b. Create an application to perform addition and subtraction using the delegate
DelegateDemo.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="DelegateDemo.aspx.cs" 
Inherits="WebApplication6.WebForm4" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
</head> 
<body style="height: 613px"> 
<form id="form1" runat="server"> 
<div style="height: 647px"><br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Label ID="Label1" runat="server" Text="Delegate Demo" BorderStyle="Groove"></asp:Label> 
<br /> 
&nbsp;&nbsp;&nbsp; 
<br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Label ID="Label2" runat="server" Text="Enter number 1: "></asp:Label> 
&nbsp;&nbsp; 
<asp:TextBox ID="TextBox1" runat="server"></asp:TextBox> 
<br /> 
<br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Label ID="Label3" runat="server" Text="Enter number 2: "></asp:Label>&nbsp;&nbsp; 
<asp:TextBox ID="TextBox2" runat="server"></asp:TextBox><br /><br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Button ID="Button1" runat="server" Height="29px" Text="Delegate Demo" 
Width="146px" onclick="Button1_Click" /><br />&nbsp;&nbsp;<br />&nbsp;&nbsp;&nbsp;<br /> 
&nbsp;&nbsp;&nbsp; 
<asp:Label ID="Label4" runat="server" Text="Label"></asp:Label><br /><br /> 
&nbsp;&nbsp;&nbsp; 
<asp:Label ID="Label5" runat="server" Text="Label"></asp:Label> 
</div> 
</form> 
</body> 
</html>
```
DelegateDemo.aspx.cs: 
```
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
namespace WebApplication6 
{ 
    public delegate int MathOperation(int a, int b); 
    public partial class WebForm4 : System.Web.UI.Page 
    { 
        int add(int a, int b) 
        { 
            return a + b; 
        } 
        int sub(int a, int b) 
        { 
            return a - b; 
        } 
            protected void Button1_Click(object sender, EventArgs e) 
        { 
            int x = Convert.ToInt32(TextBox1.Text); 
            int y = Convert.ToInt32(TextBox2.Text); 
            MathOperation Add = new MathOperation(add); 
            MathOperation Sub = new MathOperation(sub); 
            Label4.Text = "Addition is: " + Add(x, y).ToString(); 
            Label5.Text = "Subtraction is " + Sub(x, y).ToString(); 
        } 
    } 
    }
 ```

#### 3. Write the program for the following: 
##### a. Create an application to demonstrate following operations i. Generate Fibonacci series. ii. Test for prime numbers. 
FiboPrime.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="FiboPrime.aspx.cs" 
Inherits="WebApplication6.FiboPrime" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
<style type="text/css"> 
.style1 
{ 
font-family: "Century Gothic"; 
font-size: xx-large; 
} 
</style> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div style="height: 608px">   <br /> 
<span class="style1">&nbsp; </span> 
<asp:Label ID="Label1" runat="server" CssClass="style1" Text="Enter the number"></asp:Label> 
<span class="style1">&nbsp;: 
<asp:TextBox ID="TextBox1" runat="server" CssClass="style1" Height="45px"></asp:TextBox> 
</span> 
<br class="style1" /> 
<br class="style1" /> 
<span class="style1">&nbsp; </span> 
<asp:Button ID="Button1" runat="server" CssClass="style1" Height="46px" 
Text="Fibonacci" Width="222px" onclick="Button1_Click" /> 
<br class="style1" /> 
<br class="style1" /> 
<span class="style1">&nbsp; </span> 
<asp:Label ID="Label2" runat="server" CssClass="style1" Text="Label"></asp:Label> 
<br class="style1" /> 
<br class="style1" /> 
<span class="style1">&nbsp; </span> 
<asp:Button ID="Button2" runat="server" CssClass="style1" Height="53px" 
Text="Prime number" Width="268px" onclick="Button2_Click" /> 
<br class="style1" /> 
<br class="style1" /> 
<span class="style1">&nbsp; </span> 
<asp:Label ID="Label3" runat="server" CssClass="style1" Text="Label"></asp:Label> 
</div> 
</form> 
</body> 
</html>
```
FiboPrime.aspx.cs: 
```
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
namespace WebApplication6 
{ 
    public partial class FiboPrime : System.Web.UI.Page 
    { 
        protected void Page_Load(object sender, EventArgs e) 
        { 
        } 
        protected void Button1_Click(object sender, EventArgs e) 
        { 
            int a, b, c, i, n; 
            a = 0; 
            b = 1; 
            Label2.Text = a.ToString() + b.ToString(); 
            n = Convert.ToInt32(TextBox1.Text); 
            for (i = 1; i <= n; ++i) 
            { 
                c = a + b; 
                Label2.Text = Label2.Text + c.ToString(); 
                a = b; 
                b = c; 
            } 
        } 
        protected void Button2_Click(object sender, EventArgs e) 
        { 
            int n, i, s = 0; 
            n = Convert.ToInt32(TextBox1.Text); 
            if(n == 0 || n == 1) 
                s = 1; 
            for(i = 2; i <= n/2; ++i){ 
                if(n % i == 0){ 
                    s = 1; 
                    break; 
                } 
            } 
            if(s == 0) 
                Label3.Text = "The number is Prime."; 
            else 
            Label3.Text = "Number is not prime."; 
        } 
        } 
    }
   ```
##### b. Create a simple application to demonstrate use of the concepts of interfaces. 
Area.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Area.aspx.cs" 
Inherits="WebApplication6.Area" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
<style type="text/css"> 
.style1 
{ 
font-family: "Freestyle Script"; 
font-size: xx-large; 
} 
</style> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div style="height: 654px"> 
<br /> 
<br class="style1" /> 
&nbsp;&nbsp; 
<asp:Label ID="Label1" runat="server" 
Text="Area of Circle and Rectangle using Interface." CssClass="style1"></asp:Label> 
 
<br class="style1" /> 
<br class="style1" /> 
&nbsp; <span class="style1">Area of Circle:&nbsp;&nbsp; </span> 
<asp:Label ID="Label2" runat="server" CssClass="style1" Text="Label"></asp:Label> 
<br class="style1" /> 
<br class="style1" /> 
<span class="style1">&nbsp;Area of Rectangle:&nbsp; </span> 
<asp:Label ID="Label3" runat="server" CssClass="style1" Text="Label"></asp:Label> 
</div> 
</form> 
</body> 
</html> 
```
Area.aspx.cs: 
```
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
namespace WebApplication6 
{ 
    interface Area1 
    { 
        double show(double s, double t); 
    } 
    class Rect : Area1 
    { 
        public double show(double s, double t) 
        { 
            return s * t; 
        } 
    } 
    class Circle : Area1 
    { 
        public double show(double s, double t) 
        { 
            return (3.14 * s * t); 
        } 
    } 
    public partial class Area : System.Web.UI.Page 
    { 
        protected void Page_Load(object sender, EventArgs e) 
        { 
            Rect r1 = new Rect(); 
            double x = r1.show(3,4); 
            Circle c1 = new Circle(); 
            double y = c1.show(3, 4); 
            Label2.Text = x.ToString(); 
            Label3.Text = y.ToString(); 
        } 
    } 
}
```
#### 4.Write the program for the following: 
##### a. Create a simple web page with variousserver controls to demonstrate setting and use of their properties. (Example : AutoPostBack). 
AutoPostBack.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="AutoPostBack.aspx.cs" 
Inherits="WebApplication6.AutoPostBack" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
</head> 
<body style="font-size: large"> 
<form id="form1" runat="server"> 
<div> 
&nbsp; 
Prof. Jayshree Vishe &nbsp;&nbsp;&nbsp; Subject Guide<br /><br /> 
Enter Name: 
<asp:TextBox ID="TextBox1" runat="server" ontextchanged="TextBox1_TextChanged"></asp:TextBox><br /> 
<br /> 
Enter Age:<asp:TextBox ID="TextBox2" runat="server" 
MaxLength="2" Width="142px" Height="29px"></asp:TextBox><br /><br /> 
Select Gender: 
<asp:RadioButtonList ID="RadioButtonList1" runat="server" AutoPostBack="True"> 
<asp:ListItem>Male</asp:ListItem> 
<asp:ListItem>Female</asp:ListItem> 
</asp:RadioButtonList><br /> 
Select Hobbies: 
<br /> 
<asp:CheckBoxList ID="CheckBoxList1" runat="server" AutoPostBack="True"> 
<asp:ListItem>Reading</asp:ListItem> 
<asp:ListItem>Dancing</asp:ListItem> 
<asp:ListItem>Playing</asp:ListItem> 
</asp:CheckBoxList><br /> 
<asp:Image ID="Image1" runat="server" Height="300px" ImageUrl="~/scene.jpg" /><br /><br /> 
Select City: 
<asp:ListBox ID="ListBox1" runat="server" AutoPostBack="True"> 
<asp:ListItem>Mumbai</asp:ListItem> 
<asp:ListItem>Goa</asp:ListItem> 
<asp:ListItem>Delhi</asp:ListItem> 
</asp:ListBox><br /><br /> 
Select country: 
<asp:DropDownList ID="DropDownList1" runat="server" Height="43px" Width="93px"> 
<asp:ListItem>India</asp:ListItem> 
<asp:ListItem>London</asp:ListItem> 
<asp:ListItem>USA</asp:ListItem> 
</asp:DropDownList><br /><br /> 
<asp:Button ID="Button1" runat="server" onclick="Button1_Click" 
Text="Display" Height="41px" Width="106px" /><br /><br /> 
<asp:Label ID="Label1" runat="server" Text="Label"></asp:Label><br /> 
<asp:Label ID="Label2" runat="server" Text="Label"></asp:Label><br /> 
<asp:Label ID="Label3" runat="server" Text="Label"></asp:Label><br /> 
<asp:Label ID="Label4" runat="server" Text="Label"></asp:Label><br /> 
<asp:Label ID="Label5" runat="server" Text="Label"></asp:Label><br /> 
<asp:Label ID="Label6" runat="server" Text="Label"></asp:Label><br /> 
</div> 
</form> 
</body> 
</html> 
```
AutoPostBack.aspx.cs: 
```
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
namespace WebApplication6 
{ 
    public partial class AutoPostBack : System.Web.UI.Page 
    { 
        protected void Page_Load(object sender, EventArgs e) 
        { 
        } 
        protected void ListBox1_SelectedIndexChanged(object sender, EventArgs e) 
        { 
        } 
 
        protected void DropDownList1_SelectedIndexChanged(object sender, EventArgs e) 
        { 
        } 
        protected void RadioButtonList1_SelectedIndexChanged(object sender, EventArgs e) 
        { 
        } 
        protected void CheckBoxList1_SelectedIndexChanged(object sender, EventArgs e) 
        { 
        } 
        protected void TextBox1_TextChanged(object sender, EventArgs e) 
        { 
        } 
        protected void Button1_Click(object sender, EventArgs e) 
        { 
            Label1.Text = TextBox1.Text; 
            Label2.Text = TextBox2.Text; 
            Label3.Text = RadioButtonList1.SelectedValue; 
            Label4.Text = CheckBoxList1.SelectedValue; 
            Label5.Text = ListBox1.SelectedItem.Value; 
            Label6.Text = DropDownList1.SelectedItem.Value; 
        } 
    } 
}
```
##### b. Create a simple application to demonstrate your vacation using calendar control.
Calender.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="calender.aspx.cs" 
Inherits="WebApplication6.calender" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
<style type="text/css"> 
.style1 
{ 
font-size: large; 
} 
.style2 
{ 
font-size: xx-large; 
} 
</style> 
</head> 
<body> 
<form id="form1" runat="server"> 
<h2 class="style2">Vacation planner</h2> 
<div> 
<asp:Label ID="Label1" runat="server" Text="Label" CssClass="style1">Select your vacation start:</asp:Label> 
</div> 
<asp:Calendar ID="Calendar1" runat="server" 
onselectionchanged="Calendar1_SelectionChanged"></asp:Calendar><br /> 
<asp:Label ID="Label2" runat="server" Text="Vacation details:" 
CssClass="style1"></asp:Label> 
<br class="style1" /> 
<asp:TextBox ID="TextBoxDetails" runat="server" Rows="5" TextMode="MultiLine" 
CssClass="style1"></asp:TextBox> 
<br class="style1" /> 
<br class="style1" /> 
<br class="style1" /> 
<asp:Button ID="Button1" runat="server" OnClick="Button1_click" 
Text="Save Vacation" CssClass="style1" /> 
<br class="style1" /> 
<br class="style1" /> 
<asp:Label ID="LabelResult" runat="server" Text="Label" CssClass="style1"></asp:Label> 
</form> 
</body> 
</html> 
```
Calender.aspx.cs: 
```
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
namespace WebApplication6 
{ 
    public partial class calender : System.Web.UI.Page 
    { 
        protected void Page_Load(object sender, EventArgs e) 
        { 
        } 
        protected void Calendar1_SelectionChanged(object sender, EventArgs e) 
        { 
            LabelResult.Text = "You Selected:" + Calendar1.SelectedDate.ToShortDateString(); 
        } 
        protected void Button1_click(object sender, EventArgs e) 
        { 
            string vacationDate = Calendar1.SelectedDate.ToString(); 
            String vacationDetails = TextBoxDetails.Text; 
            if (string.IsNullOrEmpty(vacationDetails)) 
            { 
                LabelResult.Text = "Please enter vacation details"; 
            } 
            else 
            { 
                LabelResult.Text = "Vacation on" + vacationDate + ":" + vacationDetails; 
            } 
        } 
    } 
}
```
#### 5.Write the program for the following: 
##### a. Create a registration form to demonstrate use of various Validation controls. 
Validation.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Validation.aspx.cs" 
Inherits="WebApplication6.Validation" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
</head> 
<body> 
<form id="form1" runat="server"> 
<h2>Validation Controls Demo</h2> 
<!-- 1. Required Field Validator --> 
<asp:Label ID="lblName" runat="server" Text="Name: " /> 
<asp:TextBox ID="txtName" runat="server" /> 
<asp:RequiredFieldValidator ID="rfvName" runat="server" 
ControlToValidate="txtName" 
ErrorMessage="Name is required!" 
ForeColor="Red" /><br /><br /> 
<!-- 2. Compare Validator --> 
<asp:Label ID="lblPassword" runat="server" Text="Password: " /> 
<asp:TextBox ID="txtPassword" runat="server" TextMode="Password" /> 
<br /> 
<asp:Label ID="lblConfirmPassword" runat="server" Text="Confirm Password: " /> 
<asp:TextBox ID="txtConfirmPassword" runat="server" TextMode="Password" /> 
<asp:CompareValidator ID="cvPassword" runat="server" 
ControlToValidate="txtConfirmPassword" 
ControlToCompare="txtPassword" 
ErrorMessage="Passwords do not match!" 
ForeColor="Red" /><br /><br /> 
<!-- 3. Range Validator --> 
<asp:Label ID="lblAge" runat="server" Text="Age (18-60): " /> 
<asp:TextBox ID="txtAge" runat="server" /> 
<asp:RangeValidator ID="rvAge" runat="server" 
ControlToValidate="txtAge" 
MinimumValue="18" 
MaximumValue="60" 
Type="Integer" 
ErrorMessage="Age must be between 18 and 60!" 
ForeColor="Red" /><br /><br /> 
<!-- 4. Regular Expression Validator --> 
<asp:Label ID="lblEmail" runat="server" Text="Email: " /> 
<asp:TextBox ID="txtEmail" runat="server" /> 
<asp:RegularExpressionValidator ID="revEmail" runat="server" 
ControlToValidate="txtEmail" 
ValidationExpression="^[^@\s]+@[^@\s]+\.[^@\s]+$" 
ErrorMessage="Invalid email format!" 
ForeColor="Red" /><br /><br /> 
<!-- 5. Custom Validator --> 
<asp:Label ID="lblUsername" runat="server" Text="Username (min 5 chars): " /> 
<asp:TextBox ID="txtUsername" runat="server" /> 
<asp:CustomValidator ID="cvUsername" runat="server" 
ControlToValidate="txtUsername" 
OnServerValidate="ValidateUsername" 
ErrorMessage="Username must be at least 5 characters!" 
ForeColor="Red" /><br /><br /> 
<!-- 6. Validation Summary --> 
<asp:ValidationSummary ID="vsSummary" runat="server" 
HeaderText="Please fix the following errors:" 
ForeColor="Red" /><br /> 
<asp:Button ID="btnSubmit" runat="server" Text="Submit" OnClick="btnSubmit_Click" 
Height="40px" Width="133px" /> 
</form> 
</body> 
</html> 
```
Validation.aspx.cs: 
```
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
namespace WebApplication6 
{ 
    public partial class Validation : System.Web.UI.Page 
    { 
        protected void Page_Load(object sender, EventArgs e) 
        { 
        } 
        protected void ValidateUsername(object source, System.Web.UI.WebControls.ServerValidateEventArgs 
args) 
        { 
            args.IsValid = args.Value.Length >= 5; 
        } 
                protected void btnSubmit_Click(object sender, EventArgs e) 
        { 
            if (Page.IsValid) 
            { 
                // All validations passed 
                Response.Write("<script>alert('Form submitted successfully!');</script>"); 
            } 
        }   }   }
 ```
##### b. Create Web Form to demonstrate use User Controls.
Footer.ascx: 
```
<%@ Control Language="C#" AutoEventWireup="true" CodeBehind="Footer.ascx.cs" 
Inherits="WebApplication6.Footer" %> 
<table style="border: 2px solid black"> 
<tr> 
<td align="center" style="background-color:Aqua; font-size:xx-large"> Advanced Web Programming Practical 
5_B </td> 
</tr> 
</table>
```
Footer.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="Footer.aspx.cs" 
Inherits="WebApplication6.Footer1" %> 
<%@ Register Src="/footer.ascx" TagName="footer" TagPrefix="STfooter"%> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
    <title></title> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div> 
<asp:Label ID="Label1" runat="server" Text="Welcome to ASP.Net"></asp:Label> 
</div> 
<STfooter:footer ID="footer1" runat="server" /> 
</form> 
</body> 
</html>
```
##### 6. Write the program for Creating a Web Form to demonstrate use of Website Navigation controls. 
Web.sitemap: 
```
<?xml version="1.0" encoding="utf-8" ?> 
<siteMap xmlns="http://schemas.microsoft.com/AspNet/SiteMap-File-1.0" > 
<siteMapNode url="WebForm1.aspx" title="Home page"  description="Home"> 
<siteMapNode url="fashion.aspx" title="Fashion page"  description="Fashion" > 
<siteMapNode url="clothes.aspx" title="Clothes page"  description="clothes" /> 
<siteMapNode url="WinterWear.aspx" title="WinterWear page"  description="WinterWear" /> 
<siteMapNode url="shoes.aspx" title="Shoes page"  description="shoes" /> 
</siteMapNode> 
</siteMapNode> 
</siteMap> 
```
WebForm1.aspx: 
``` 
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WebForm1.aspx.cs" 
Inherits="_6A.WebForm1" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div> 
&nbsp; Web Page Navigation &nbsp; &nbsp;<br /><br /> 
<asp:TreeView ID="TreeView1" runat="server" DataSourceID="SiteMapDataSource1" 
onselectednodechanged="TreeView1_SelectedNodeChanged1" > 
</asp:TreeView><br /> 
<asp:SiteMapDataSource ID="SiteMapDataSource1" runat="server" /> 
</div> 
</form> 
</body> 
</html> 
```
Fashion.aspx:
``` 
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="fashion.aspx.cs" 
Inherits="_6A.fashion" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
<style type="text/css"> 
.style1 { 
font-size: x-large; 
} 
</style> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div> 
<br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; <span class="style1">Fashion Page</span><br /> 
<br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Image ID="Image1" runat="server" Height="225px" Width="243px" 
ImageUrl="~/fashion.jpg" /> 
</div> 
</form> 
</body> 
</html> 
```
Clothes.aspx:
``` 
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="clothes.aspx.cs" 
Inherits="_6A.clothes" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
<style type="text/css"> 
.style1 
{ 
font-size: x-large; 
} 
</style> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div> 
<br /> 
&nbsp;&nbsp;&nbsp;&nbsp; <span class="style1">Clothes Page</span><br /> 
&nbsp;&nbsp;&nbsp; 
<br /> 
&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Image ID="Image1" runat="server" Height="228px" Width="212px" ImageUrl="~/clothes.jpg" /> 
</div> 
</form> 
</body> 
</html> 
```
Winterwear.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="WinterWear.aspx.cs" 
Inherits="_6A.WinterWear" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
<style type="text/css"> 
.style1 
{ 
font-size: x-large; 
} 
</style> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div> 
<br /> 
&nbsp; 
<br /> 
&nbsp;&nbsp;&nbsp;&nbsp; <span class="style1">WinterWear Page</span><br /> 
<br /> 
<br /> 
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 
<asp:Image ID="Image1" runat="server" Height="366px" Width="406px" 
ImageUrl="~/WinterWear.jpg" /> 
</div> 
</form> 
</body> 
</html> 
```
Shoes.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeBehind="shoes.aspx.cs" 
Inherits="_6A.shoes" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
<style type="text/css"> 
.style1 
{ 
font-size: x-large; 
} 
</style> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div> 
<br /> 
&nbsp; <span class="style1">&nbsp;Shoes Page</span><br /> 
&nbsp;<br /> 
&nbsp;&nbsp; 
<asp:Image ID="Image1" runat="server" Height="219px" Width="200px" ImageUrl="~/Shoes.jpg" /> 
</div> 
</form> 
</body> 
</html>
```
##### 7.  Write the program for Creating a web application to demonstrate use of Master Page and content page.
MasterPage.master: 
```
<%@ Master Language="C#" AutoEventWireup="true" CodeFile="MasterPage.master.cs" 
Inherits="MasterPage" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
<asp:ContentPlaceHolder id="head" runat="server"> 
</asp:ContentPlaceHolder> 
<style type="text/css"> 
.style1 { 
height: 66px; 
} 
.style2 
{ 
width: 84px; 
height: 99px; 
} 
.style3 
{ 
width: 548px; 
} 
.style4 
{ 
width: 84px; 
height: 105px; 
} 
.style5 
{ 
width: 84px; 
height: 100px; 
} 
</style> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div> 
<center> <table style="height: 469px; width: 754px"> 
<tr> 
<td colspan="2" class="style1" bgcolor="#0099CC"><center>Prof. Jayshree Vishe</center></td> 
</tr> 
<tr> 
<td class="style2" bgcolor="Yellow"><a href="page1.aspx">Page-1</a></td> 
<td rowspan="3" class="style3"> 
<asp:ContentPlaceHolder id="ContentPlaceHolder1" runat="server"> 
</asp:ContentPlaceHolder> 
</td></tr><tr> 
<td class="style5" bgcolor="#66FF99"><a href="Page2.aspx">Page-2</a></td> 
</tr> 
<tr> 
<td class="style4" bgcolor="#FF66FF"><a href="Page3.aspx">Page-3</a></td> 
</tr> 
<tr> 
<td colspan="2" bgcolor="#339933"><center>Master Page Application</center></td> 
</tr> 
</table> 
</center> 
</div> 
</form> 
</body> 
</html> 
```
Home.aspx: 
```
<%@ Page Title="" Language="C#" MasterPageFile="~/MasterPage.master" AutoEventWireup="true" 
CodeFile="Home.aspx.cs" Inherits="Home" %> 
<asp:Content ID="Content1" ContentPlaceHolderID="head" Runat="Server"> 
</asp:Content> 
<asp:Content ID="Content2" ContentPlaceHolderID="ContentPlaceHolder1" Runat="Server"> 
</asp:Content> 
```
Page1.aspx: 
```
<%@ Page Title="" Language="C#" MasterPageFile="~/MasterPage.master" AutoEventWireup="true" 
CodeFile="Page1.aspx.cs" Inherits="Page1" %> 
<asp:Content ID="Content1" ContentPlaceHolderID="head" Runat="Server"> 
</asp:Content> 
<asp:Content ID="Content2" ContentPlaceHolderID="ContentPlaceHolder1" Runat="Server"> 
<asp:Label ID="Label1" runat="server" Text="User Name"></asp:Label>&nbsp;<asp:TextBox 
ID="TextBox1" 
runat="server"></asp:TextBox> 
<br /> 
&nbsp;<asp:Label ID="Label2" runat="server" Text="Password"></asp:Label>&nbsp;<asp:TextBox 
ID="TextBox2" 
runat="server"></asp:TextBox> 
<br /> 
<asp:Button ID="Button1" runat="server" Text="Login" /> 
</asp:Content> 
```
Page2.aspx: 
```
<%@ Page Title="" Language="C#" MasterPageFile="~/MasterPage.master" AutoEventWireup="true" 
CodeFile="Page2.aspx.cs" Inherits="Page2" %> 
<asp:Content ID="Content1" ContentPlaceHolderID="head" Runat="Server"> 
</asp:Content> 
<asp:Content ID="Content2" ContentPlaceHolderID="ContentPlaceHolder1" Runat="Server"> 
<asp:Image ID="Image1" runat="server" ImageUrl="~/b.jpg" Height="200px" /> 
</asp:Content> 
```
Page3.aspx: 
```
<%@ Page Title="" Language="C#" MasterPageFile="~/MasterPage.master" AutoEventWireup="true" 
CodeFile="Page3.aspx.cs" Inherits="Page3" %> 
<asp:Content ID="Content1" ContentPlaceHolderID="head" Runat="Server"> 
</asp:Content> 
<asp:Content ID="Content2" ContentPlaceHolderID="ContentPlaceHolder1" Runat="Server"> 
<asp:Image ID="Image1" runat="server" ImageUrl="~/a.jpg" Height="200px" /> 
</asp:Content> 
```
##### 8. Write the program for Creating a web application to demonstrate the use of different types of Cookies.
Cookie.aspx: 
```
<%@ Page Language="C#" AutoEventWireup="true" CodeFile="Cookie.aspx.cs" Inherits="Cookie" %> 
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" 
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> 
<html xmlns="http://www.w3.org/1999/xhtml"> 
<head runat="server"> 
<title></title> 
<style type="text/css"> 
.style1 
{ 
font-family: "Book Antiqua"; 
font-size: xx-large; 
text-align: left; 
} 
.style2 
{ 
text-align: left; 
} 
</style> 
</head> 
<body> 
<form id="form1" runat="server"> 
<div style="height: 656px; " class="style2"> 
<br /> 
<br /> 
<span class="style1">&nbsp; Cookie Management Demo.<br />   
<br /> 
&nbsp; 
<asp:Button ID="Button1" runat="server" Height="50px" Text="Create Session Cookie" 
Width="240px" onclick="Button1_Click" /> 
<asp:Button ID="Button2" runat="server" Height="50px" Text="Create Persistent Cookie" 
Width="240px" onclick="Button2_Click" /> 
<asp:Button ID="Button3" runat="server" Height="50px" Text="Read Cookies" 
Width="240px" onclick="Button3_Click" /> 
<asp:Button ID="Button4" runat="server" Height="50px" Text="Delete Cookies" 
Width="240px" onclick="Button4_Click" /> 
<br /> 
<br /> 
&nbsp; 
<asp:Label ID="Label1" runat="server" Text=""></asp:Label> 
<br /> 
</span> 
</div> 
</form> 
</body> 
</html> 
```
 
Cookie.aspx.cs: 
```
using System; 
using System.Collections.Generic; 
using System.Linq; 
using System.Web; 
using System.Web.UI; 
using System.Web.UI.WebControls; 
public partial class Cookie : System.Web.UI.Page 
{ 
    protected void Page_Load(object sender, EventArgs e) 
    { 
    } 
    protected void Button1_Click(object sender, EventArgs e) 
    { 
        HttpCookie sessionCookie = new HttpCookie("SessionCookie", "This is a Session Cookie"); 
        Response.Cookies.Add(sessionCookie); 
        Label1.Text = "Session Cookie created successfully."; 
    } 
 
    protected void  Button2_Click(object sender, EventArgs e) 
{ 
        HttpCookie persistentCookie = new HttpCookie("PersistentCookie","This is a persistent cookie"); 
        persistentCookie.Expires = DateTime.Now.AddMinutes(1); 
        Response.Cookies.Add(persistentCookie); 
        Label1.Text = "Persistent cookie created successfully and will expire in 1 minute."; 
} 
protected void  Button3_Click(object sender, EventArgs e) 
{ 
    string message = " "; 
    if(Request.Cookies["SessionCookie"]!=null) 
    { 
        message += "Session Cookie Value: " + Request.Cookies["SessionCookie"].Value + "<br/>"; 
    } 
    else{ 
        message += "Session Cookie does not exist.<br/>"; 
    } 
    if(Request.Cookies["PersistentCookie"] != null){ 
        message += "Persistent Cookie value:" + Request.Cookies["PersistentCookie"].Value + "<br/>"; 
    } 
    else{ 
        message += "Persistent Cookie does not exist.<br/>"; 
    } 
    Label1.Text = message; 
} 
protected void  Button4_Click(object sender, EventArgs e) 
{ 
    if(Request.Cookies["SessionCookie"] != null){ 
        HttpCookie sessionCookie = new HttpCookie("SessionCookie"); 
        sessionCookie.Expires = DateTime.Now.AddDays(-1); 
        Response.Cookies.Add(sessionCookie); 
    } 
    if(Request.Cookies["PersistentCookie"] != null){ 
        HttpCookie persistentCookie = new HttpCookie("persistentCookie"); 
        persistentCookie.Expires = DateTime.Now.AddDays(-1); 
        Response.Cookies.Add(persistentCookie); 
    } 
    Label1.Text = "Both session and persistent cookies have been deleted."; 
} 
} 
```
 
