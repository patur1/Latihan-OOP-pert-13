# Latihan-OOP-pert-13
# Bahasa Pemrograman
# Python Code

          import tkinter as tk
          from view.input_form import InputForm
          from view.mahasiswa import MahasiswaView
          from data.mahasiswa import DataMahasiswa

        class MainApp:
            def __init__(self, master):
                 self.master = master
                 self.master.title("Aplikasi Data Mahasiswa")

                 # Inisialisasi DataMahasiswa
                 self.data_mahasiswa = DataMahasiswa()

                 # Membuat tombol-tombol pada jendela utama
                 self._create_widgets()

                def _create_widgets(self):
                """Membuat tombol utama aplikasi."""
                self.button_input = tk.Button(self.master, text="Input Mahasiswa", command=self.open_input_form)
                self.button_input.pack(pady=10)

                self.button_view = tk.Button(self.master, text="Lihat Daftar Mahasiswa", command=self.open_mahasiswa_view)
                self.button_view.pack(pady=10)

               def open_input_form(self):
               """Membuka form input di jendela baru."""
               self._open_new_window(InputForm)

              def open_mahasiswa_view(self):
              """Membuka daftar mahasiswa di jendela baru."""
              self._open_new_window(MahasiswaView)

              def _open_new_window(self, view_class):
                 """Membantu membuka jendela baru dengan kelas tampilan tertentu."""
                    new_window = tk.Toplevel(self.master)
                    view_class(new_window, self.data_mahasiswa)

             if __name__ == "__main__":
                          root = tk.Tk()
                          app = MainApp(root)
                          root.mainloop()
# Hasil Run Python
1. Tampilan awal
![image](https://github.com/user-attachments/assets/770b0272-1308-4977-81fa-0964d1139292)
2. Masukkan Data Mahasiswa
![image](https://github.com/user-attachments/assets/ad05fd38-7cf4-4dee-840f-74b5bfabc878)
3. Ubah data salah satu mahasiswa
![image](https://github.com/user-attachments/assets/49c7bf67-074c-4c3f-be82-61c34355c7c0)
4. Hapus data salah satu mahasiswa
