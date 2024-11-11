## 1. How does object-oriented programming pair so closely with GUIs?

## 2. What is the relationship between WindowListener and WindowAdapter?
The relationship between WindowListener and WindowAdapter is that 
WindowListener 
WindowAdapter is an example of multithreading where when the final window is closed, main is also closed. WindowListener performs the same actions as WindowAdapter, but here, even when main has closed, the program persists. 

## 3. What does the program below produce for a GUI? (You can sketch and upload an image or describe it – do this without running the program to make sure you understand what each line below is doing).

## 4. Modify the HelloGoodbyeEx2 code to update the number of times the button has been clicked on the button’s label itself. DO THIS!!!!!!!
```
import javax.swing.*;
import java.awt.*;
import java.awt.event.*;

public class HelloGoodbyeEx2 {

    public static void main(String args[]) {
        JFrame f = new JFrame();
        f.setTitle("Hello/Goodbye Ex1");
        f.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);
        
        JLabel label = new JLabel("Hello");
        JButton button = new JButton("Click me!");

        //using an anonymous (static) class
        //avoids having to make ButtonClickListenerEx1 class above
        button.addActionListener(new ActionListener() {
                //implement the one method here
                //shares the name space with the whole class
                //has access to the label field above
                public void actionPerformed(ActionEvent e) {
                    if (label.getText().equals("Hello")) {
                        label.setText("Goodbye");
                    }else {
                        label.setText("Hello");
                    }
                }
            });
        
        f.add(button, BorderLayout.SOUTH);
        f.add(label, BorderLayout.NORTH);

        f.pack();
        f.setVisible(true);
        
    }
}
```


## 5. Consider the following Java swing GUI
```
public class RedPillBluePill extends JFrame {
    JLabel label;

    public RedPillBluePill() {
        this.setSize(300, 300);
        this.setDefaultCloseOperation(JFrame.EXIT_ON_CLOSE);

        JPanel panel = new JPanel(new BorderLayout());        
        JButton red = new JButton("red");
        JButton blue = new JButton("blue");
        panel.add(red, BorderLayout.EAST);
        panel.add(blue, BorderLayout.WEST);
        label = new JLabel("click a button");
        this.add(label, BorderLayout.NORTH);
        this.add(panel, BorderLayout.SOUTH);

        red.addActionListener(new ActionListener() {
            @Override
            public void actionPerformed(ActionEvent e) {
                // TODO Auto-generated method stub
                label.setText("RED");        
            }
        });

        blue.addActionListener(new ActionListener() {

            @Override
            public void actionPerformed(ActionEvent (e) -> {
                    if (l.getText().equals("Hello")) {
                        l.setText("Goodbye");
                    }else {
                        l.setText("Hello");
                    }
                });
    }
}
```
Convert the ActionListeners to Lambda Functions.





## 6. Explain why for ActionListener you can use a Lambda function but for WindowListener you cannot?
The Lambda expressions only work if there is a single method to implement it. 


## 7. Write a program that allows you to enter a 6-digit PIN, like you would on your smartphone to unlock it. It should have the following layout:

```
 [ DISPLAY PIN AS TYPED ]

   [ 1 ]  [ 2 ] [ 3 ] 
   
   [ 4 ]  [ 5 ] [ 6 ]    
   
   [ 7 ]  [ 8 ] [ 9 ]       

   [ < ]  [ 0 ]
```

Where ```[ < ]``` is a “backspace” button. The display should show the PIN as it is typed, and when the user enters the PIN 202113, the display changes to “YOU MAY ENTER!”

```Java



```




//main has finished, but the windows/program persist 


S = J frame() renders the window
to add any functionality: S add*(...)  <-- EVENT 
