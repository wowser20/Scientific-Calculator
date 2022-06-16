import java.awt.Color;
import java.awt.Container;
import java.awt.Font;
import java.awt.event.ActionEvent;
import java.awt.event.ActionListener;
import java.awt.event.KeyAdapter;
import java.awt.event.KeyEvent;
import java.math.BigInteger;
import java.text.DecimalFormat;
import java.util.EmptyStackException;
import java.util.Stack;

import javax.script.ScriptEngine;
import javax.script.ScriptEngineManager;
import javax.script.ScriptException;
import javax.swing.*;
@SuppressWarnings("serial")
/*
 * Scientific Calculator Using Java
 * @Andrea Ella Remoreras
 * CS26L - 3RD TASK PERFORMANCE
 * 
 * 
 **/
public class Scientific_Calculator extends JFrame implements ActionListener{
	
	private JTextField txt_number;
	private JLabel lbl_Logo;
	private JButton btn1,btn2,btn3,btn4,btn5,btn6,btn7,btn8,btn9,btn_abs,btn0,btn_pi,btnopen_par,btnclose_par,btn_Clear,btn_Delete,btn_Equals, btn_Percent,btn_ln,btn_Square,btn_Plus,btn_Minus,btn_Plusmin,btn_Divide,btn_Multiply,btn_Period,btn_pow2,btn_pow, btn_pow3,btn_Sin,btn_Sin_1,btn_Tan_1, btn_Cos_1,btn_Tan,btn_Cos, btn_Log, btn00;
	
	MathEval ev = new MathEval();
	
	
	Scientific_Calculator(){
		
		
		Container pane = getContentPane();
		pane.setLayout(null);
		pane.setBackground(new Color(0,25,51));
		
		txt_number= new JTextField("");
		txt_number.setFont(new Font("Dialog", Font.BOLD, 20));
		txt_number.setBackground(new Color(0,204,204));
		txt_number.setForeground(Color.BLACK);
		
		txt_number.addKeyListener(new KeyAdapter() {
            public void keyTyped(KeyEvent e) {
                char caracter = e.getKeyChar();
                if (((caracter < '0') || (caracter > '9'||(caracter == '.')
                        && (caracter != '\b')))) {
                    e.consume();
    }
    }           
	});
		
		
		lbl_Logo=new JLabel("SCIENTIFIC");
		lbl_Logo.setFont(new Font("Dialog", Font.BOLD, 20));
		lbl_Logo.setForeground(Color.WHITE);
		
		
		
		btn_Plusmin=new JButton("±");
		btn_Plusmin.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Plusmin.setBackground(new Color(64,64,64));
		btn_Plusmin.setForeground(Color.WHITE);
		
		btn_Square=new JButton("√");
		btn_Square.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Square.setBackground(new Color(64,64,64));
		btn_Square.setForeground(Color.WHITE);
		
		btn_Percent=new JButton("%");
		btn_Percent.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Percent.setBackground(new Color(64,64,64));
		btn_Percent.setForeground(Color.WHITE);
		
		btn_Sin=new JButton("sin");
		btn_Sin.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Sin.setBackground(new Color(64,64,64));
		btn_Sin.setForeground(Color.WHITE);
		
		btn_Sin_1=new JButton("sinh");
		btn_Sin_1.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Sin_1.setBackground(new Color(64,64,64));
		btn_Sin_1.setForeground(Color.WHITE);
		
		btn_Cos=new JButton("cos");
		btn_Cos.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Cos.setBackground(new Color(64,64,64));
		btn_Cos.setForeground(Color.WHITE);
		
		btn_Cos_1=new JButton("cosh");
		btn_Cos_1.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Cos_1.setBackground(new Color(64,64,64));
		btn_Cos_1.setForeground(Color.WHITE);
		
		btn_Tan=new JButton("tan");
		btn_Tan.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Tan.setBackground(new Color(64,64,64));
		btn_Tan.setForeground(Color.WHITE);
		
		btn_Tan_1=new JButton("tanh");
		btn_Tan_1.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Tan_1.setBackground(new Color(64,64,64));
		btn_Tan_1.setForeground(Color.WHITE);
		
		btn_Log=new JButton("log");
		btn_Log.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_Log.setBackground(new Color(64,64,64));
		btn_Log.setForeground(Color.WHITE);
		
		btn_ln=new JButton("ln");
		btn_ln.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_ln.setBackground(new Color(64,64,64));
		btn_ln.setForeground(Color.WHITE);
		
		btn_pow2=new JButton("x²");
		btn_pow2.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_pow2.setBackground(new Color(64,64,64));
		btn_pow2.setForeground(Color.WHITE);
		
		btn_pow3=new JButton("x³");
		btn_pow3.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_pow3.setBackground(new Color(64,64,64));
		btn_pow3.setForeground(Color.WHITE);
		
		btn_pow=new JButton("^");
		btn_pow.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_pow.setBackground(new Color(64,64,64));
		btn_pow.setForeground(Color.WHITE);
		
		btn_pi=new JButton("π");
		btn_pi.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_pi.setBackground(new Color(64,64,64));
		btn_pi.setForeground(Color.WHITE);
		
		btn_abs=new JButton("Abs");
		btn_abs.setFont(new Font("Dialog", Font.BOLD, 15));
		btn_abs.setBackground(new Color(64,64,64));
		btn_abs.setForeground(Color.WHITE);
		
		btnopen_par=new JButton("(");
		btnopen_par.setFont(new Font("Dialog", Font.BOLD, 15));
		btnopen_par.setBackground(new Color(64,64,64));
		btnopen_par.setForeground(Color.WHITE);
		
		btnclose_par=new JButton(")");
		btnclose_par.setFont(new Font("Dialog", Font.BOLD, 15));
		btnclose_par.setBackground(new Color(64,64,64));
		btnclose_par.setForeground(Color.WHITE);
		
		btn1=new JButton("1");
		btn1.setFont(new Font("Dialog", Font.BOLD, 30));
		btn1.setBackground(Color.GRAY);
		btn1.setForeground(Color.WHITE);
		
		btn2=new JButton("2");
		btn2.setFont(new Font("Dialog", Font.BOLD, 30));
		btn2.setBackground(Color.GRAY);
		btn2.setForeground(Color.WHITE);
		
		btn3=new JButton("3");
		btn3.setFont(new Font("Dialog", Font.BOLD, 30));
		btn3.setBackground(Color.GRAY);
		btn3.setForeground(Color.WHITE);
		
		btn4=new JButton("4");
		btn4.setFont(new Font("Dialog", Font.BOLD, 30));
		btn4.setBackground(Color.GRAY);
		btn4.setForeground(Color.WHITE);
		
		btn5=new JButton("5");
		btn5.setFont(new Font("Dialog", Font.BOLD, 30));
		btn5.setBackground(Color.GRAY);
		btn5.setForeground(Color.WHITE);
		
		btn6=new JButton("6");
		btn6.setFont(new Font("Dialog", Font.BOLD, 30));
		btn6.setBackground(Color.GRAY);
		btn6.setForeground(Color.WHITE);
		
		btn7=new JButton("7");
		btn7.setFont(new Font("Dialog", Font.BOLD, 30));
		btn7.setBackground(Color.GRAY);
		btn7.setForeground(Color.WHITE);
		
		btn8=new JButton("8");
		btn8.setFont(new Font("Dialog", Font.BOLD, 30));
		btn8.setBackground(Color.GRAY);
		btn8.setForeground(Color.WHITE);
		
		btn9=new JButton("9");
		btn9.setFont(new Font("Dialog", Font.BOLD, 30));
		btn9.setBackground(Color.GRAY);
		btn9.setForeground(Color.WHITE);
		
		btn0= new JButton("0");
		btn0.setFont(new Font("Dialog", Font.BOLD, 30));
		btn0.setBackground(Color.GRAY);
		btn0.setForeground(Color.WHITE);
		
		btn00=new JButton("00");
		btn00.setFont(new Font("Dialog", Font.BOLD, 30));
		btn00.setBackground(Color.GRAY);
		btn00.setForeground(Color.WHITE);
		
		
		btn_Period=new JButton(".");
		btn_Period.setFont(new Font("Dialog", Font.BOLD, 30));
		btn_Period.setBackground(Color.GRAY);
		btn_Period.setForeground(Color.WHITE);
		
		btn_Plus=new JButton("+");
		btn_Plus.setFont(new Font("Dialog", Font.BOLD, 30));
		btn_Plus.setBackground(new Color(64,64,64));
		btn_Plus.setForeground(Color.WHITE);
		
		btn_Minus=new JButton("-");
		btn_Minus.setFont(new Font("Dialog", Font.BOLD, 30));
		btn_Minus.setBackground(new Color(64,64,64));
		btn_Minus.setForeground(Color.WHITE);
		
		btn_Multiply=new JButton("x");
		btn_Multiply.setFont(new Font("Dialog", Font.BOLD, 30));
		btn_Multiply.setBackground(new Color(64,64,64));
		btn_Multiply.setForeground(Color.WHITE);
		
		btn_Divide= new JButton("÷");
		btn_Divide.setFont(new Font("Dialog", Font.BOLD, 30));
		btn_Divide.setBackground(new Color(64,64,64));
		btn_Divide.setForeground(Color.WHITE);
		
		
		
		btn_Clear=new JButton("AC");
		btn_Clear.setFont(new Font("Dialog", Font.BOLD, 20));
		btn_Clear.setBackground(new Color(255,128,0));
		btn_Clear.setForeground(Color.WHITE);
		 
		btn_Delete=new JButton("DEL");
		btn_Delete.setFont(new Font("Dialog", Font.BOLD, 20));
		btn_Delete.setBackground(new Color(255,128,0));
		btn_Delete.setForeground(Color.WHITE);
		
		btn_Equals=new JButton("=");
		btn_Equals.setFont(new Font("Dialog", Font.BOLD, 30));
		btn_Equals.setBackground(new Color(64,64,64));
		btn_Equals.setForeground(Color.WHITE);
		
		
		pane.add(lbl_Logo).setBounds(185,0,150,50);
		pane.add(txt_number).setBounds(20,50,446,100);
		
		pane.add(btn_pow2).setBounds(20,170,70,40);
		pane.add(btn_pow3).setBounds(95,170,70,40);
		pane.add(btn_pow).setBounds(170,170,70,40);
		pane.add(btn_Square).setBounds(245,170,70,40);
		pane.add(btn_Log).setBounds(320,170,70,40);
		pane.add(btn_ln).setBounds(395,170,70,40);
		
		pane.add(btn_pi).setBounds(20,215,70,40);
		pane.add(btn_Plusmin).setBounds(95,215,70,40);
		pane.add(btn_abs).setBounds(170,215,70,40);
		pane.add(btn_Sin).setBounds(245,215,70,40);
		pane.add(btn_Cos).setBounds(320,215,70,40);
		pane.add(btn_Tan).setBounds(395,215,70,40);
		
		pane.add(btnopen_par).setBounds(20,260,70,40);
		pane.add(btnclose_par).setBounds(95,260,70,40);
		pane.add(btn_Percent).setBounds(170,260,70,40);
		pane.add(btn_Sin_1).setBounds(245,260,70,40);
		pane.add(btn_Cos_1).setBounds(320,260,70,40);
		pane.add(btn_Tan_1).setBounds(395,260,70,40);
		
		pane.add(btn7).setBounds(20,340,80,60);
		pane.add(btn8).setBounds(110,340,80,60);
		pane.add(btn9).setBounds(200,340,80,60);
		pane.add(btn_Delete).setBounds(300,340,80,60);
		pane.add(btn_Clear).setBounds(388,340,80,60);
		
		pane.add(btn4).setBounds(20,405,80,60);
		pane.add(btn5).setBounds(110,405,80,60);
		pane.add(btn6).setBounds(200,405,80,60);
		pane.add(btn_Multiply).setBounds(300,405,80,60);
		pane.add(btn_Divide).setBounds(388,405,80,60);
		
		pane.add(btn1).setBounds(20,470,80,60);
		pane.add(btn2).setBounds(110,470,80,60);
		pane.add(btn3).setBounds(200,470,80,60);
		pane.add(btn_Plus).setBounds(300,470,80,60);
		pane.add(btn_Minus).setBounds(388,470,80,60);
		
		pane.add(btn0).setBounds(20,535,80,60);
		pane.add(btn_Period).setBounds(110,535,80,60);
		pane.add(btn00).setBounds(200,535,80,60);
		pane.add(btn_Equals).setBounds(300,535,170,60);
		
	
		setTitle("Scientific Calculator");
		setSize(500,650);
		setVisible(true);
		setLocationRelativeTo(null);
		setDefaultCloseOperation(EXIT_ON_CLOSE);
		
		btn_pow2.addActionListener(this);
		btn_pow3.addActionListener(this);
		btn_pow.addActionListener(this);
		btn_Square.addActionListener(this);
		btn_Log.addActionListener(this);
		btn_ln.addActionListener(this);
		btn_pi.addActionListener(this);
		btn_Plusmin.addActionListener(this);
		btn_abs.addActionListener(this);
		btn_Sin.addActionListener(this);
		btn_Cos.addActionListener(this);
		btn_Tan.addActionListener(this);
		btnopen_par.addActionListener(this);
		btnclose_par.addActionListener(this);
		btn_Percent.addActionListener(this);
		btn_Sin_1.addActionListener(this);
		btn_Cos_1.addActionListener(this);
		btn_Tan_1.addActionListener(this);
		
		btn7.addActionListener(this);
		btn8.addActionListener(this);
		btn9.addActionListener(this);
		btn_Delete.addActionListener(this);
		btn_Clear.addActionListener(this);
		btn4.addActionListener(this);
		btn5.addActionListener(this);
		btn6.addActionListener(this);
		btn_Multiply.addActionListener(this);
		btn_Divide.addActionListener(this);
		btn1.addActionListener(this);
		btn2.addActionListener(this);
		btn3.addActionListener(this);
		btn_Plus.addActionListener(this);
		btn_Minus.addActionListener(this);
		btn0.addActionListener(this);
		btn_Period.addActionListener(this);
		btn00.addActionListener(this);
		btn_Equals.addActionListener(this);
		
	}

	public static void main (String[]args){
		
		new Scientific_Calculator();
	}


	@Override
	public void actionPerformed(ActionEvent e) {
		// TODO Auto-generated method stub
		if(e.getSource().equals(btn_Equals)){
			
			try {
				Calculate();
			}catch(Exception e2) {
				txt_number.setText("\t"+"   Syntax Error");
			}
		}
		else if(e.getSource().equals(btn1)){
			txt_number.setText(txt_number.getText()+"1");
		}
		else if(e.getSource().equals(btn2)){
			txt_number.setText(txt_number.getText()+"2");
		}
		else if(e.getSource().equals(btn3)){
			txt_number.setText(txt_number.getText()+"3");
		}
		else if(e.getSource().equals(btn4)){
			txt_number.setText(txt_number.getText()+"4");
		}
		else if(e.getSource().equals(btn5)){
			txt_number.setText(txt_number.getText()+"5");
		}
		else if(e.getSource().equals(btn6)){
			txt_number.setText(txt_number.getText()+"6");
		}
		else if(e.getSource().equals(btn7)){
			txt_number.setText(txt_number.getText()+"7");
		}
		else if(e.getSource().equals(btn8)){
			txt_number.setText(txt_number.getText()+"8");
		}
		else if(e.getSource().equals(btn9)){
			txt_number.setText(txt_number.getText()+"9");
		}
		else if(e.getSource().equals(btn0)){
			txt_number.setText(txt_number.getText()+"0");
		}
		else if(e.getSource().equals(btn00)){
			txt_number.setText(txt_number.getText()+"00");
		}
		else if(e.getSource().equals(btn_Delete)){
			try{
				String s = txt_number.getText().toString();
				s = s.substring(0, s.length() - 1);
				txt_number.setText(s);
			}catch(Exception e1){
				JOptionPane.showMessageDialog(null, "Input box is empty");
		}
		
		}
		else if(e.getSource().equals(btn_Clear)){
			txt_number.setText("");
		}
		else if(e.getSource().equals(btn_Multiply)){
			txt_number.setText(txt_number.getText()+"*");
		}
		else if(e.getSource().equals(btn_Divide)){
			txt_number.setText(txt_number.getText()+"÷");
		}
		else if(e.getSource().equals(btn_Plus)){
			txt_number.setText(txt_number.getText()+"+");
		}
		else if(e.getSource().equals(btn_Minus)){
			txt_number.setText(txt_number.getText()+"-");
		}
		else if(e.getSource().equals(btn_Period)){
			txt_number.setText(txt_number.getText()+".");
		}
		else if(e.getSource().equals(btn_pow2)){
			txt_number.setText(txt_number.getText()+"^2");
		}
		else if(e.getSource().equals(btn_pow3)){
			txt_number.setText(txt_number.getText()+"^3");
		}
		else if(e.getSource().equals(btn_pow)){
			txt_number.setText(txt_number.getText()+"^");
		}
		else if(e.getSource().equals(btn_Square)){
			txt_number.setText(txt_number.getText()+"sqrt(");
		}
		else if(e.getSource().equals(btn_Log)){
			txt_number.setText(txt_number.getText()+"log(");
		}
		else if(e.getSource().equals(btn_ln)){
			txt_number.setText(txt_number.getText()+"ln2");
		}
		else if(e.getSource().equals(btn_Plusmin)){
			txt_number.setText(txt_number.getText()+"±");
		}
		else if(e.getSource().equals(btn_abs)){
			txt_number.setText(txt_number.getText()+"abs(");
		}
		else if(e.getSource().equals(btn_Sin)){
			txt_number.setText(txt_number.getText()+"sin(");
		}
		else if(e.getSource().equals(btn_Cos)){
			txt_number.setText(txt_number.getText()+"cos(");
		}
		else if(e.getSource().equals(btn_Tan)){
			txt_number.setText(txt_number.getText()+"tan(");
		}
		else if(e.getSource().equals(btnopen_par)){
			txt_number.setText(txt_number.getText()+"(");
		}
		else if(e.getSource().equals(btnclose_par)){
			txt_number.setText(txt_number.getText()+")");
		}
		else if(e.getSource().equals(btn_Percent)){
			txt_number.setText(txt_number.getText()+"%");
		}
		else if(e.getSource().equals(btn_Sin_1)){
			txt_number.setText(txt_number.getText()+"sinh(");
		}
		else if(e.getSource().equals(btn_Cos_1)){
			txt_number.setText(txt_number.getText()+"cosh(");
		}
		else if(e.getSource().equals(btn_Tan_1)){
			txt_number.setText(txt_number.getText()+"tanh(");
		
		}
		else if(e.getSource().equals(btn_pi)) {
			txt_number.setText(txt_number.getText()+"PI");
		}
		else
		{
		JOptionPane.showMessageDialog(null,"Button not available");
		}

	}
	public void evaluate() {
		StringBuilder finalStr = new StringBuilder();
		String expr  = (String)txt_number.getText();
		if(isProperExpression(expr)) {
			expr = replaceBefore(expr);
			char[] temp = expr.toCharArray();
			String operators = "(+-*/%)";
			for(int i = 0; i < temp.length; i++) {
				if((i == 0 && temp[i] != '*') || (i == temp.length-1 && temp[i] != '/' && temp[i] != '!')) {
					finalStr.append(temp[i]);
				} else if((i > 0 && i < temp.length -1) || (i==temp.length-1 && temp[i] == '!')) {
					if(temp[i] == '!') {
						StringBuilder str = new StringBuilder();
						for(int k = i-1; k >= 0; k--) {
							if(Character.isDigit(temp[k])) {
								str.insert(0, temp[k] );
							} else {
								break;
							}
						}
						Long prev = Long.valueOf(str.toString());
						BigInteger val = new BigInteger("1");
						for(Long j = prev; j > 1; j--) {
							val = val.multiply(BigInteger.valueOf(j));
						}
						finalStr.setLength(finalStr.length() - str.length());
						finalStr.append("(" + val + ")");
						if(temp.length > i+1) {
							char next = temp[i+1];
							if(operators.indexOf(next) == -1) { 
								finalStr.append("*");
							}
						}
					} else {
						finalStr.append(temp[i]);
					}
				}
			}
			expr = finalStr.toString();
			if(expr != null && !expr.isEmpty()) {
				ScriptEngineManager mgr = new ScriptEngineManager();
				ScriptEngine engine = mgr.getEngineByName("JavaScript");
				try {
					String i  = engine.eval(expr).toString();
					double a  = Double.parseDouble(i);
					DecimalFormat dc = new DecimalFormat("0.00");
					String formattedText = dc.format(a);
					txt_number.setText(formattedText);
					if (txt_number.getText().equals("NaN")) {
						txt_number.setText("0");
					}
				} catch (ScriptException e) {
					txt_number.setText("Error");
				}
			} 
		} else {
			txt_number.setText("Syntax Eror");
		}
	}

private static boolean isProperExpression(String expr) {
	expr = expr.replaceAll("[^()]", "");
	char[] arr = expr.toCharArray();
	Stack<Character> stack = new Stack<Character>();
	int i =0;
	while(i < arr.length) {
		try {
			if(arr[i] == '(') {
				stack.push(arr[i]);
			} else {
				stack.pop();
			}
		} catch (EmptyStackException e) {
			stack.push(arr[i]);
		}
		i++;
	}
	return stack.isEmpty();
}
private static String replaceBefore(String expr) {
	expr = expr.replace("(", "*(");
	expr = expr.replace("+*", "+").replace("-*", "-").replace("*", "").replace("/*", "/").replace("%*", "%");
	return expr;
}
public void Calculate() {//method for the equal button
	String s = Double.toString(ev.evaluate(txt_number.getText()));
	txt_number.setText(s);

	try {
		if ((ev.evaluate(txt_number.getText()) == Math.floor(ev.evaluate(txt_number.getText()))) && !Double.isInfinite(ev.evaluate(txt_number.getText()))) {
			double a  = Double.parseDouble(s);
			DecimalFormat dc = new DecimalFormat("0");
			String formattedText = dc.format(a);
			txt_number.setText(formattedText);
			
		}else {
			double a  = Double.parseDouble(s);
			DecimalFormat dc = new DecimalFormat("0.00");
			String formattedText = dc.format(a);
			txt_number.setText(formattedText);
		}
	} catch (Exception e2) {
		txt_number.setText("Syntax Error");
	}
	
}
}

	
	
	
