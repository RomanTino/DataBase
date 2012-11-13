using System;
using System.Collections.Generic;
using System.ComponentModel;
using System.Data;
using System.Drawing;
using System.Linq;
using System.Text;
using System.Windows.Forms;

namespace DataBaseTest
{
    public partial class Form1 : Form
    {
        public Form1()
        {
            InitializeComponent();
        }

        private void button1_Click(object sender, EventArgs e)
        {
            Database1Entities ado = new Database1Entities();
            ado.Database.Connection.Open();
            Productc product = new Productc() { name = "Cake", amount = 1 };
            ado.Productcs.Add(product);
            ado.SaveChanges();
            string str = "";
            List<Productc> list = ado.Productcs.ToList<Productc>();
            foreach (Productc pr in list)
            {
                str += pr.name.ToString() + " " + pr.amount.ToString() + " ";
            }
            MessageBox.Show(str);
            ado.Database.Connection.Close();
        }
    }
}
