
# Aplikasi Cek Ganjil Genap

Tugas 1 Modul Aplikasi Cek Ganjil Genap

Aplikasi Cek Nomor Ganjil Genap dan Bilangan Prima adalah proyek sederhana yang dikembangkan sebagai latihan dalam modul pembelajaran pemrograman GUI berbasis Java. Aplikasi ini berfungsi untuk membantu pengguna mengetahui apakah suatu nomor tertentu adalah ganjil atau genap, serta memeriksa apakah nomor tersebut adalah bilangan prima. Dengan fitur ini, pengguna dapat dengan mudah mengecek sifat dari suatu angka melalui antarmuka yang interaktif.

# Deskripsi
Aplikasi ini menggunakan komponen JFrame untuk membangun antarmuka pengguna yang sederhana dan mudah digunakan. Pengguna dapat memasukkan angka yang ingin diperiksa melalui antarmuka GUI, dan aplikasi akan menampilkan hasilnya:

Ganjil atau Genap: Aplikasi akan menentukan apakah angka yang dimasukkan adalah ganjil atau genap, berdasarkan sisa hasil bagi angka tersebut dengan 2.
Bilangan Prima: Selain ganjil atau genap, aplikasi juga akan mengecek apakah angka tersebut merupakan bilangan prima, yaitu bilangan yang hanya memiliki dua faktor pembagi: 1 dan dirinya sendiri.



# Features

Fitur tambahan dari aplikasi ini meliputi:

- Input Validasi: Aplikasi memvalidasi input untuk memastikan bahwa pengguna hanya memasukkan angka.
- Tampilan Hasil Cepat: Hasil pengecekan ditampilkan secara real-time setelah pengguna menekan tombol "Cek."
- Antarmuka Sederhana dan Ramah Pengguna: Aplikasi dirancang untuk mudah digunakan, sehingga cocok untuk pengguna yang baru belajar pemrograman GUI.

Aplikasi ini dirancang untuk latihan pemrograman dasar dalam Java dan untuk memperkenalkan konsep pengecekan kondisi serta penggunaan antarmuka grafis.


# Dokumentasi Code

```java

import javax.swing.JOptionPane;

public class AplikasiCekNomorGanjilGenapForm extends javax.swing.JFrame {
    
    
    private boolean isPrime(int number) {
        if (number <= 1) return false; // Bilangan <= 1 bukan bilangan prima
        for (int i = 2; i <= Math.sqrt(number); i++) {
            if (number % i == 0) return false; // Jika bisa dibagi dengan i, maka bukan bilangan prima
        }
        return true; // Jika tidak bisa dibagi dengan angka manapun, maka bilangan prima
    }


    /**
     * Creates new form AplikasiCekNomorGanjilGenapForm
     */
    public AplikasiCekNomorGanjilGenapForm() {
        initComponents();
    }

    /**
     * This method is called from within the constructor to initialize the form.
     * WARNING: Do NOT modify this code. The content of this method is always
     * regenerated by the Form Editor.
     */
    @SuppressWarnings("unchecked")
    // <editor-fold defaultstate="collapsed" desc="Generated Code">                          
    private void initComponents() {

        jPanel1 = new javax.swing.JPanel();
        jLabel1 = new javax.swing.JLabel();
        jLabel2 = new javax.swing.JLabel();
        jTextFieldAngka = new javax.swing.JTextField();
        jLabelHasil = new javax.swing.JLabel();
        jButton1 = new javax.swing.JButton();

        setDefaultCloseOperation(javax.swing.WindowConstants.EXIT_ON_CLOSE);

        jLabel1.setFont(new java.awt.Font("Verdana", 1, 24)); // NOI18N
        jLabel1.setText("Aplikasi Cek Nomor Ganjil Genap");

        jLabel2.setFont(new java.awt.Font("ROG Fonts", 1, 14)); // NOI18N
        jLabel2.setText("Masukan Angka");

        jTextFieldAngka.addFocusListener(new java.awt.event.FocusAdapter() {
            public void focusGained(java.awt.event.FocusEvent evt) {
                jTextFieldAngkaFocusGained(evt);
            }
        });
        jTextFieldAngka.addKeyListener(new java.awt.event.KeyAdapter() {
            public void keyTyped(java.awt.event.KeyEvent evt) {
                jTextFieldAngkaKeyTyped(evt);
            }
        });

        jButton1.setText("Cek Angka");
        jButton1.addActionListener(new java.awt.event.ActionListener() {
            public void actionPerformed(java.awt.event.ActionEvent evt) {
                jButton1ActionPerformed(evt);
            }
        });

        javax.swing.GroupLayout jPanel1Layout = new javax.swing.GroupLayout(jPanel1);
        jPanel1.setLayout(jPanel1Layout);
        jPanel1Layout.setHorizontalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addGroup(jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
                    .addComponent(jLabelHasil)
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addGap(50, 50, 50)
                        .addComponent(jLabel1))
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addGap(166, 166, 166)
                        .addComponent(jLabel2))
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addGap(153, 153, 153)
                        .addComponent(jTextFieldAngka, javax.swing.GroupLayout.PREFERRED_SIZE, 186, javax.swing.GroupLayout.PREFERRED_SIZE))
                    .addGroup(jPanel1Layout.createSequentialGroup()
                        .addGap(192, 192, 192)
                        .addComponent(jButton1)))
                .addContainerGap(33, Short.MAX_VALUE))
        );
        jPanel1Layout.setVerticalGroup(
            jPanel1Layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(jPanel1Layout.createSequentialGroup()
                .addComponent(jLabelHasil)
                .addGap(6, 6, 6)
                .addComponent(jLabel1)
                .addGap(30, 30, 30)
                .addComponent(jLabel2)
                .addGap(12, 12, 12)
                .addComponent(jTextFieldAngka, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addGap(11, 11, 11)
                .addComponent(jButton1)
                .addContainerGap(79, Short.MAX_VALUE))
        );

        javax.swing.GroupLayout layout = new javax.swing.GroupLayout(getContentPane());
        getContentPane().setLayout(layout);
        layout.setHorizontalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jPanel1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addContainerGap(javax.swing.GroupLayout.DEFAULT_SIZE, Short.MAX_VALUE))
        );
        layout.setVerticalGroup(
            layout.createParallelGroup(javax.swing.GroupLayout.Alignment.LEADING)
            .addGroup(layout.createSequentialGroup()
                .addContainerGap()
                .addComponent(jPanel1, javax.swing.GroupLayout.PREFERRED_SIZE, javax.swing.GroupLayout.DEFAULT_SIZE, javax.swing.GroupLayout.PREFERRED_SIZE)
                .addContainerGap(33, Short.MAX_VALUE))
        );

        pack();
    }// </editor-fold>                        

    private void jButton1ActionPerformed(java.awt.event.ActionEvent evt) {                                         
         String input = jTextFieldAngka.getText();
        try {
            int number = Integer.parseInt(input);
            String message = "Angka " + number + (number % 2 == 0 ? " adalah genap." : " adalah ganjil.");
            if (isPrime(number)) {
            message += " Juga merupakan bilangan prima.";
            } else {
            message += " Bukan bilangan prima.";
            }
            // Menampilkan hasil menggunakan JOptionPane
            JOptionPane.showMessageDialog(this, message, "Hasil Pemeriksaan", JOptionPane.INFORMATION_MESSAGE);
        } catch (NumberFormatException ex) {
            // Menampilkan pesan error menggunakan JOptionPane
            JOptionPane.showMessageDialog(this, "Input tidak valid. Masukkan angka!", "Error", JOptionPane.ERROR_MESSAGE);
        }
    }                                        

    private void jTextFieldAngkaKeyTyped(java.awt.event.KeyEvent evt) {                                         
         char c = evt.getKeyChar();
    if (!Character.isDigit(c)) {
        evt.consume(); // Membatalkan input jika bukan angka
    }
    }                                        

    private void jTextFieldAngkaFocusGained(java.awt.event.FocusEvent evt) {                                            
        jTextFieldAngka.setText("");
    }                                           

    /**
     * @param args the command line arguments
     */
    public static void main(String args[]) {
        /* Set the Nimbus look and feel */
        //<editor-fold defaultstate="collapsed" desc=" Look and feel setting code (optional) ">
        /* If Nimbus (introduced in Java SE 6) is not available, stay with the default look and feel.
         * For details see http://download.oracle.com/javase/tutorial/uiswing/lookandfeel/plaf.html 
         */
        try {
            for (javax.swing.UIManager.LookAndFeelInfo info : javax.swing.UIManager.getInstalledLookAndFeels()) {
                if ("Nimbus".equals(info.getName())) {
                    javax.swing.UIManager.setLookAndFeel(info.getClassName());
                    break;
                }
            }
        } catch (ClassNotFoundException ex) {
            java.util.logging.Logger.getLogger(AplikasiCekNomorGanjilGenapForm.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (InstantiationException ex) {
            java.util.logging.Logger.getLogger(AplikasiCekNomorGanjilGenapForm.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (IllegalAccessException ex) {
            java.util.logging.Logger.getLogger(AplikasiCekNomorGanjilGenapForm.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        } catch (javax.swing.UnsupportedLookAndFeelException ex) {
            java.util.logging.Logger.getLogger(AplikasiCekNomorGanjilGenapForm.class.getName()).log(java.util.logging.Level.SEVERE, null, ex);
        }
        //</editor-fold>

        /* Create and display the form */
        java.awt.EventQueue.invokeLater(new Runnable() {
            public void run() {
                new AplikasiCekNomorGanjilGenapForm().setVisible(true);
            }
        });
    }

    // Variables declaration - do not modify                     
    private javax.swing.JButton jButton1;
    private javax.swing.JLabel jLabel1;
    private javax.swing.JLabel jLabel2;
    private javax.swing.JLabel jLabelHasil;
    private javax.swing.JPanel jPanel1;
    private javax.swing.JTextField jTextFieldAngka;
    // End of variables declaration                   
}


```


## Authors

Muhammad Irwan Firmanto
2210010582 5B Reg Pagi Banjarmasin

- [@eternalsugarzy](https://www.github.com/eternalsugarzy)


## Screenshots
![Screenshot 2024-11-02 013141](https://github.com/user-attachments/assets/6605425e-726b-4944-bc11-32b2c91ba22c)





