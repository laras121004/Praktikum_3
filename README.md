# Praktikum_3
## - Lengkapi latihan class Mahasiswa dengan setter dan getter
public class Mahasiswa extends Manusia {
    String nim;
    String jurusan;

    public Mahasiswa(String nama, String jenisKelamin, int umur, String alamat, String nim, String jurusan) {
        super(nama, jenisKelamin, umur, alamat);
        this.nim = nim;
        this.jurusan = jurusan;
    }

    // Getter dan Setter untuk Mahasiswa
    public String getNim() {
        return nim;
    }

    public void setNim(String nim) {
        this.nim = nim;
    }

    public String getJurusan() {
        return jurusan;
    }

    public void setJurusan(String jurusan) {
        this.jurusan = jurusan;
    }
} 
## *Penjelasan
Kelas Mahasiswa
Kelas Mahasiswa ini adalah subclass dari kelas Manusia. Kelas ini memperluas kelas Manusia dengan menambahkan atribut khusus yang hanya dimiliki oleh mahasiswa, yaitu nim (Nomor Induk Mahasiswa) dan jurusan.

Atribut:
String nim: Untuk menyimpan Nomor Induk Mahasiswa.
String jurusan: Untuk menyimpan informasi jurusan dari mahasiswa tersebut.

Hubungan dengan Kelas Manusia
Kelas Mahasiswa adalah subclass yang mewarisi atribut dan metode dari superclass Manusia. Artinya, objek Mahasiswa dapat mengakses atribut dan metode dari Manusia seperti nama, jenisKelamin, umur, dan alamat, serta menggunakan metode yang ada di kelas Manusia.

Kesimpulan:
Kelas ini memungkinkan untuk membuat objek mahasiswa yang memiliki informasi seperti nama, jenis kelamin, umur, alamat, nim, dan jurusan. Setiap objek Mahasiswa dapat mengubah atau mendapatkan informasi tersebut menggunakan getter dan setter.

# Hasil Outout
!gambar[]

## - Implementasikan java code diagram pada class berikut:
!gambar[]

- Menampilkan class Pegawai
public class Pegawai {
    private String nama;
    private double gajiPokok;

    public void setNama(String nama) {
        this.nama = nama;
    }

    public String getNama() {
        return nama;
    }

    public void setGajiPokok(double gajiPokok) {
        this.gajiPokok = gajiPokok;
    }

    public double getGajiPokok() {
        return gajiPokok;
    }

    public void cetakInfo() {
        System.out.println("Nama: " + nama);
        System.out.println("Gaji Pokok: " + gajiPokok);
    }
} 

- Menampilkan Class Manager
  class Manager  extends Pegawai {
    private double tunjangan;

    public void setTunjangan(double tunjangan) {
        this.tunjangan = tunjangan;
    }

    public double getTunjangan() {
        return tunjangan;
    }
}

- Menampilkan Class Programmer
  class Programmer extends Pegawai {
    private double bonus;

    public void setBonus(double bonus) {
        this.bonus = bonus;
    }

    public double getBonus() {
        return bonus;
    }

    /**
     *
     */
    @Override
    public void cetakInfo() {
        super.cetakInfo();
        System.out.println("Bonus: " + bonus);
    }

    public void cetakBonus() {
        System.out.println("Bonus: " + bonus);
    }
} 

- Menampilkan Class Main
public class Main {
   public static void main(String[] args) {
        // Membuat objek Manager
        Manager manajer = new Manager();
        manajer.setNama("Budi");
        manajer.setGajiPokok(5000000);
        manajer.setTunjangan(2000000);
        manajer.cetakInfo();

        // Membuat objek Programmer
        Programmer programmer = new Programmer();
        programmer.setNama("Siti");
        programmer.setGajiPokok(4000000);
        programmer.setBonus(1000000);
        programmer.cetakInfo();  
}
}

Pada implementasi ini, class Manager dan Programmer mewarisi atribut dan metode dari class Pegawai. Mereka juga menambahkan atribut baru yaitu tunjangan untuk Manager dan bonus untuk Programmer, dengan metode setter, getter, dan metode tambahan untuk mencetak informasi yang relevan.

