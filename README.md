- 👋 Hi, I’m @pritiumbare
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
pritiumbare/pritiumbare is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
hello i am priti umbare i had written the code for healthcare chatbot which helps people for interaction with doctors and booking appointment
--->
package kratin;
import java.awt.Color;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;

import javax.swing.JButton;
import javax.swing.JComboBox;
import javax.swing.JFrame;
import javax.swing.JLabel;
import javax.swing.JTextArea;
import javax.swing.JTextField;

class Chatbot extends JFrame
{
	private JTextArea ca=new JTextArea();
	private JTextField cf=new JTextField();
	private JButton ba=new JButton();
	private JLabel l=new JLabel();
	//Private JComboBox com=new JComboBox();
	
	
	Chatbot()
	{
		JFrame f=new JFrame();
		f.setDefaultCloseOperation(EXIT_ON_CLOSE);
		f.setVisible(true);
		f.setResizable(false);
		f.setLayout(null);
		f.setSize(400,400);
		f.getContentPane().setBackground(Color.cyan);
		f.setTitle("ChatBot");
		f.add(ca);
		f.add(cf);
		ca.setSize(800,310);
		ca.setLocation(1,1);
		cf.setSize(300,20);
		cf.setLocation(1,320);
		
		f.add(ba);
		l.setText("SEND");
		ba.add(l);
		ba.setSize(400,20);
		ba.setLocation(300, 320);
		//ba.setSize(300,20);
		//ba.setLocation(300,320);
		ba.addActionListener(new ActionListener()
				{
			public void actionPerformed(ActionEvent e)
			{
				if(e.getSource()==ba)
				{
					String text=cf.getText().toLowerCase();
					ca.setForeground(Color.GREEN);
					ca.append("you-->"+text+"\n");
					cf.setText("");
					if(text.contains("hi"))
					{
						replyMath("Hi welcome to healthcare ");
					}
					else if(text.contains("can you help me"))
					{
						replyMath("sure,you have to answer some questions \n what type of help you need \n 1.Book appointment \n 2.help me dignose \n 3.contact hospital");
						
					}
					
					else if(text.contains("book appointment")) 
					{
						replyMath("enter some details:1.name \n 2.gender \n 3.appointment date");
						
						
					}
					else if(text.contains("name")) 
					{
					replyMath("okay thank you ");
				   }
				else if(text.contains("help me dignose")) 
				{
						replyMath("what is your age");
				}
				else if(text.contains("age")) 
					{
					replyMath("what is symptoms :1.cough \n 2.fever \n 3.Headache");
				     }
			    	else if(text.contains("symptoms"))
					{
						replyMath("Hmm,clearly you are not feeling well please contact to hospital");
					}
					
					else if(text.contains("contact hospital"))
					{
						replyMath("your appointment date and name");
					}
					else
					{
						replyMath("I cant Understand");
					}
				}
				
			}
			}
				
				);
		
		
		
	}
	
	
	public void replyMath(String s)
	{
		ca.append("chatbot-->"+s+"\n");
		
	}
}



public class healthcare_chatbot {

	
	public static void main(String[] args) {
		// TODO Auto-generated method stub
		new Chatbot();
		int ch;
		
//		switch(ch)
//		{
//		case 1:System.out.println("")
//		}
		
	
		
        
	}

}

