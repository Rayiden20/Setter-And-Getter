# Setter-And-Getter
*  NAMA  : RAYIDEN ARFAH
*  NIM   : 312210127
*  KELAS : 22.TI.B1
*  MATKUL : OOP

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace TugasPert7
{
    public class Pegawai
    {


        private string nama;
        private double gajiPokok;

        public void setNama(string nama)
        {
            this.nama = nama;
        }
        public string getNama() { return this.nama; }

        public double getGajiPokok() { return this.gajiPokok; }

        public void setGajiPokok(double gajiPokok) { this.gajiPokok = gajiPokok; }

        public void cetakinfo()
        {

            Console.WriteLine("Nama : " + this.nama);
            Console.WriteLine("Gapok : " + this.gajiPokok);
        }
    }


    public class manager : Pegawai
    {

        private double tunjangan;

        public void setTunjangan(double tunjangan) { this.tunjangan = tunjangan; }
        public double getTunjangan() { return this.tunjangan; }

        public new void cetakinfo()
        {

            base.cetakinfo();
            this.cetakTunjangan();
        }
        public void cetakTunjangan()
        {
            Console.WriteLine("Tunjangan Anda : " + this.tunjangan);

        }
    }

    public class Programmer : Pegawai
    {
        private double bonus;


        public void setBonus(double bonus) { this.bonus = bonus; }

        public double getBonus() { return this.bonus; }

        public new void cetakinfo()
        {
            base.cetakinfo();
            this.cetakBonus();
        }
        public void cetakBonus()
        {
            Console.WriteLine("Bonus : " + this.bonus);


        }

    }
    class program
    {
        static void Main(string[] args)
        {
            Console.WriteLine("==== PEGAWAI ====");
            Pegawai pegawai = new Pegawai();
            pegawai.setNama("Rayiden Arfah");
            pegawai.setGajiPokok(2000000);
            pegawai.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== MANAGER ====");
            manager Manager = new manager();
            Manager.setNama("Rayiden Arfah");
            Manager.setGajiPokok(3000000);
            Manager.setTunjangan(1500000);
            Manager.cetakinfo();
            Console.WriteLine();

            Console.WriteLine("==== PROGRAMMER ====");
            Programmer programer = new Programmer();
            programer.setNama("Rayiden Arfah");
            programer.setGajiPokok(4000000);
            programer.setBonus(2500000);
            programer.cetakinfo();
            Console.WriteLine();


            Console.WriteLine("press anykey");
            Console.ReadKey();
        }
    }
}

#  HASILNYA

![ray](https://github.com/Rayiden20/Setter-And-Getter/assets/115732267/ab58fc76-fef6-4863-a95e-1bbf361d861e)
