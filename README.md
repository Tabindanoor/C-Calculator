# C-Calculator
Code to build calculator using .net framework in C#
using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using System.Windows.Forms;

namespace CalCuLaToR
{
    public partial class Form1 : Form
    {
# declaring variables 
        string operation;
        double firstoperand;
        double secondoparand;

        public Form1()
        {
            InitializeComponent();
        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void button1_Click(object sender, EventArgs e)
        {

            textBox1.Text += btn_seven.Text;
        }

        private void button3_Click(object sender, EventArgs e)
        {

            textBox1.Text += btn_one.Text;
        }

        private void button12_Click(object sender, EventArgs e)
        {
            textBox1.Text += btn_six.Text;
        }

        private void button16_Click(object sender, EventArgs e)
        {
             if (operation == "+")
            {
                secondoparand = Convert.ToDouble(textBox1.Text);
                textBox1.Text = (firstoperand + secondoparand).ToString();
              
            }
            else if (operation == "-")
            {
                secondoparand = Convert.ToDouble(textBox1.Text);
                textBox1.Text = (firstoperand - secondoparand).ToString();
            }
            else if (operation == "*")
            {
                secondoparand = Convert.ToDouble(textBox1.Text);
                textBox1.Text = (firstoperand * secondoparand).ToString();
            }
            else if (operation == "/")
            {
                if (secondoparand != 0)
                {
                    secondoparand = Convert.ToDouble(textBox1.Text);
                    textBox1.Text = (firstoperand / secondoparand).ToString();
              
                }
                else
                {
                    textBox1.Text = "DIV/Zero!";
                }

            }
        }

        private void button8_Click(object sender, EventArgs e)
        {
            operation = "+";
            firstoperand = Convert.ToDouble(textBox1.Text);
            textBox1.Text = "";

        }

        private void button10_Click(object sender, EventArgs e)
        {
            operation = "-";
            firstoperand = Convert.ToDouble(textBox1.Text);
            textBox1.Text = "";

        }

        private void button7_Click(object sender, EventArgs e)
        {
            operation = "*";
            firstoperand = Convert.ToDouble(textBox1.Text);
            textBox1.Text = "";

        }

        private void button6_Click(object sender, EventArgs e)
        {
            operation = "/";
            firstoperand = Convert.ToDouble(textBox1.Text);
            textBox1.Text = "";

        }

        private void btn_clear_Click(object sender, EventArgs e)
        {
            textBox1.Clear();
        }

        private void textBox1_TextChanged(object sender, EventArgs e)
        {

        }

        private void btn_two_Click(object sender, EventArgs e)
        {
            textBox1.Text += btn_two.Text;
        }

        private void btn_three_Click(object sender, EventArgs e)
        {
            textBox1.Text += btn_three.Text;
        }

        private void btn_four_Click(object sender, EventArgs e)
        {
            textBox1.Text += btn_four.Text;
        }

        private void btn_5_Click(object sender, EventArgs e)
        {
            textBox1.Text += btn_5.Text;
        }

        private void btn_8_Click(object sender, EventArgs e)
        {
            textBox1.Text += btn_8.Text;
        }

        private void btn_nine_Click(object sender, EventArgs e)
        {
            textBox1.Text += btn_nine.Text;
        }

        private void btn_zero_Click(object sender, EventArgs e)
        {
            textBox1.Text += btn_zero.Text;
        }
    }
}
