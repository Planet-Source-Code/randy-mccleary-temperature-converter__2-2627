<div align="center">

## Temperature Converter


</div>

### Description

This is just a simple java applet that will convert Degrees Fahrenheit to Degrees Celesius. Very simple and can be modified to convert back.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Randy McCleary](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/randy-mccleary.md)
**Level**          |Intermediate
**User Rating**    |4.5 (36 globes from 8 users)
**Compatibility**  |Java \(JDK 1\.2\)
**Category**       |[Calculators & Science](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/calculators-science__2-71.md)
**World**          |[Java](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/java.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/randy-mccleary-temperature-converter__2-2627/archive/master.zip)





### Source Code

```
import java.awt.*;
import java.awt.event.*;
import java.applet.*;
import javax.swing.*;
import java.text.DecimalFormat;
public class temperature extends JApplet implements ActionListener
{
  JLabel lblFahrenheit;
  JLabel lblCelsius;
  JLabel outputCelsius;
  JTextField txtFahrenheit;
  double degreesFahrenheit;
  FlowLayout layout;
  public void init()
  {
   Container c = getContentPane();
   layout = new FlowLayout();
   layout.setAlignment( FlowLayout.LEFT);
   c.setLayout(layout);
   // instantiate JLabel object for Degrees Fahrenheit
   lblFahrenheit = new JLabel("Enter Fahrenheit and press enter: ");
   // instantiate JTextField object for the degrees fahrenheit
   txtFahrenheit = new JTextField(10);
   // instantiate JLabel object for Degrees Celesius
   lblCelsius = new JLabel("Degrees Celesius: ");
   // JLabel to display the equivalent degrees Celsius
   outputCelsius = new JLabel("");
   c.add(lblFahrenheit);
   //CALL the addActionListener() method on the JTextField object
   //   for the degrees Fahrenheit
   txtFahrenheit.addActionListener(this);
   // Add the textbox the celsius label and output label
   c.add(txtFahrenheit);
   c.add(lblCelsius);
   c.add(outputCelsius);
  }
  public void actionPerformed(ActionEvent e)
  {
   // Create a new decimal format to one digit
   DecimalFormat oneDigit = new DecimalFormat("0.0");
   // Get the input
   double Fahrenheit = Double.parseDouble(e.getActionCommand());
   //ASSIGN the result of CALL Celsius function
   double celsius = Celsius(Fahrenheit);
   //Display the results in the label
   outputCelsius.setText(oneDigit.format(celsius));
  }
  public double Celsius(double Fahrenheit)
  {
   double celsius;
   //Formulat to convert Farhrenheit to celsius
   celsius = 5.0 / 9.0 * ( Fahrenheit - 32);
   return celsius;
  }
}
```

