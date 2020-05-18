# Код приложения

>Можно просмотреть код приложения

```C#
namespace Kalkulator
{
        
    public partial class Form1 : Form
        
    {
        double a, b;
        int count;
        bool znak = true;
        public Form1()
        {
            InitializeComponent();
        }

        private void Button13_Click(object sender, EventArgs e) //вывод 1 в тб
        {
            textBox1.Text = textBox1.Text + 1;//+1
        }

        private void Button17_Click(object sender, EventArgs e) //вывод 0 в тб
        {
            textBox1.Text = textBox1.Text + 0;//0
        }

        private void Button14_Click(object sender, EventArgs e) //вывод 2 в тб
        {
            textBox1.Text = textBox1.Text + 2;//+2
        }

        private void Button15_Click(object sender, EventArgs e) //вывод 3 в тб
        {
            textBox1.Text = textBox1.Text + 3;//+3
        }

        private void Button9_Click(object sender, EventArgs e) //вывод 4 в тб
        {
            textBox1.Text = textBox1.Text + 4;//+4
        }

        private void Button10_Click(object sender, EventArgs e) //вывод 5 в тб
        {
            textBox1.Text = textBox1.Text + 5;//+5
        }

        private void Button11_Click(object sender, EventArgs e) //вывод 6 в тб
        {
            textBox1.Text = textBox1.Text + 6;//+6
        }

        private void Button5_Click(object sender, EventArgs e) //вывод 7 в тб
        {
            textBox1.Text = textBox1.Text + 7;//+7
        }

        private void Button6_Click(object sender, EventArgs e) //вывод 8 в тб
        {
            textBox1.Text = textBox1.Text + 8;//+8
        }

        private void Button7_Click(object sender, EventArgs e) //вывод 9 в тб
        {
            textBox1.Text = textBox1.Text + 9;//+9
        }

        private void Button4_Click(object sender, EventArgs e) //выполнение +
        {

            a = float.Parse(textBox1.Text);
            textBox1.Clear();//очистить текстбокс 1
            count = 1;
            label1.Text = a.ToString() + "+";//записать в лейбл знак +
            znak = true;
        }

        private void Button8_Click(object sender, EventArgs e) //выполнение -
        {
            a = float.Parse(textBox1.Text);
            textBox1.Clear();
            count = 2;
            label1.Text = a.ToString() + "-";//записать в лейбл знак -
            znak = true;
        }

        private void Button12_Click(object sender, EventArgs e) //выполнение *
        {
            a = float.Parse(textBox1.Text);
            textBox1.Clear();
            count = 3;
            label1.Text = a.ToString() + "*";//записать в лейбл знак *
            znak = true;
        }

        private void Button16_Click(object sender, EventArgs e) //выполнение /
        {
            a = float.Parse(textBox1.Text);
            textBox1.Clear();
            count = 4;
            label1.Text = a.ToString() + "/";//записать в лейбл знак /
            znak = true;
        }

        private void Button19_Click(object sender, EventArgs e) //выполнение =
        {
            calculate();
            label1.Text = "";
        }

        private void Button18_Click(object sender, EventArgs e) //добавление точки
        {
            if (textBox1.Text == "")
                textBox1.Text = "0,";
            if (textBox1.Text == " ")
                textBox1.Text = "0,";
            if (textBox1.Text.IndexOf(",") == -1)
                textBox1.Text += ",";
        }

        private void Button1_Click(object sender, EventArgs e) //очищение ввода
        {
            textBox1.Text = "";
            label1.Text = "";

        }

        private void Button2_Click(object sender, EventArgs e) //очищение на 1 символ
        {
            int lenght = textBox1.Text.Length - 1;
            string text = textBox1.Text;
            textBox1.Clear();
            for (int i = 0; 1 < lenght; i++) ;
        }

        private void Button3_Click(object sender, EventArgs e) //смена знаков
        {
            if (znak == true)
            {
                textBox1.Text = "-" + textBox1.Text;
                znak = false;
            }
            else if (znak == false)
            {
                textBox1.Text = textBox1.Text.Replace("-", "");
                znak = true;
            }
        }

        private void Button20_Click(object sender, EventArgs e) //синус
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Sin(a);
           
            textBox1.Text = b.ToString();
            label1.Text = a.ToString();
            Math.Pow(a, b);
        }

        private void Button21_Click(object sender, EventArgs e)//котангенс
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Tan(a);
            label1.Text = b.ToString();


        }

        private void Button22_Click(object sender, EventArgs e)//экспонента
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Exp(a);
            label1.Text = b.ToString();
        }

        private void Button23_Click(object sender, EventArgs e)//число в квадрат
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Pow(a,2);
            label1.Text = b.ToString();


        }

        private void Button24_Click(object sender, EventArgs e)//косинус
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Cos(a);
           label1.Text = b.ToString();
        }

        private void Button25_Click(object sender, EventArgs e)//модуль числа
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Abs(a);
            label1.Text = b.ToString();
        }
        
        private void Button26_Click(object sender, EventArgs e)//возведение в степень
           
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Pow(a, 4);
            label1.Text = b.ToString();

        }

        private void Button28_Click(object sender, EventArgs e)//тангенс
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Tan(a);
            label1.Text = b.ToString();
        }

        private void Button29_Click(object sender, EventArgs e)//логорифм
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Log(a);
            label1.Text = b.ToString();
        }

        private void Button30_Click(object sender, EventArgs e)//возвести в квадрат
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Sqrt(a);
            label1.Text = b.ToString();
        }

        private void Button31_Click(object sender, EventArgs e)//число в 
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = Math.Pow(a, 4);
            label1.Text = b.ToString();

        }

        private void Button27_Click(object sender, EventArgs e)//функция 1 разделить на введенное значение
        {
            a = Convert.ToInt32(float.Parse(textBox1.Text));
            b = 1 / a;
            textBox1.Text = b.ToString();
        }

        private void Button32_Click(object sender, EventArgs e)//показ доп функций
        {
            if 
                (button25.Visible == true)
                 
           
            {
                button25.Visible = false;
                button26.Visible = false;
                button22.Visible = false;
                button23.Visible = false;
                button30.Visible = false;
                button31.Visible = false;
                button27.Visible = false;
                button28.Visible = false;
                button24.Visible = false;
                button20.Visible = false;
                button21.Visible = false;
                button3.Visible = false;
                button32.Text = ">";

            }

            else
            {
                button25.Visible = true;
                button26.Visible = true;
                button22.Visible = true;
                button23.Visible = true;
                button30.Visible = true;
                button31.Visible = true;
                button27.Visible = true;
                button28.Visible = true;
                button24.Visible = true;
                button20.Visible = true;
                button21.Visible = true;
                button3.Visible = true;
                button32.Text = "<";

            }
            
        }

        private void TextBox1_KeyPress(object sender, KeyPressEventArgs e)
        {
           
                char ch = e.KeyChar;

                if (!Char.IsDigit(ch) && ch != 8) //Если символ, введенный с клавы - не цифра (IsDigit),
                {
                    e.Handled = true;// то событие не обрабатывается. ch!=8 (8 - это Backspace)
                }
            if (e.KeyChar == '.')
                e.Handled = ((Control)sender).Text != "0";
        }

        private void Label1_Click(object sender, EventArgs e)
        {

        }

        private void TextBox1_TextChanged(object sender, EventArgs e)
        {
            if (textBox1.Text == "")
            {
                button4.Enabled = false;
                button8.Enabled = false;
                button12.Enabled = false;
                button16.Enabled = false;
                button19.Enabled = false;
                button32.Enabled = false;
                button1.Enabled = false;
                button25.Enabled = false;
                button26.Enabled = false;
                button22.Enabled = false;
                button23.Enabled = false;
                button30.Enabled = false;
                button31.Enabled = false;
                button27.Enabled = false;
                button28.Enabled = false;
                button24.Enabled = false;
                button20.Enabled = false;
                button21.Enabled = false;
                button3.Enabled = false;
                // button4.Enabled = false;
            }
            else
            {
                button4.Enabled = true;
                button8.Enabled = true;
                button12.Enabled = true;
                button16.Enabled = true;
                button19.Enabled = true;
                button32.Enabled = true;
                button1.Enabled = true;
                button25.Enabled = true;
                button26.Enabled = true;
                button22.Enabled = true;
                button23.Enabled = true;
                button30.Enabled = true;
                button31.Enabled = true;
                button27.Enabled = true;
                button28.Enabled = true;
                button24.Enabled = true;
                button20.Enabled = true;
                button21.Enabled = true;
                button3.Enabled = true;
                // button4.Enabled = false;
            }
        }

        private void Form1_Load(object sender, EventArgs e)
        {

        }

        private void calculate()
        {
            switch (count)
            {
                case 1:
                    b = a + float.Parse(textBox1.Text);//сложить
                    textBox1.Text = b.ToString();
                    break;
                case 2:
                    b = a - float.Parse(textBox1.Text);//вычисть
                    textBox1.Text = b.ToString();
                    break;
                case 3:
                    b = a * float.Parse(textBox1.Text);//умножить
                    textBox1.Text = b.ToString();
                    break;
                case 4:
                    b = a / float.Parse(textBox1.Text);//разделить
                    textBox1.Text = b.ToString();
                    break;

                default:
                    break;
            }
        }

    }
}
