<style>
    body {text-align: justify}
</style>

# <b>Laporan Praktikum Pertemuan 5</b>
<b> Nama: Elang Putra Adam

Kelas: TI 3G

NIM: 2141720074 </b>

# <b>Pertanyaan</b>
buka https://jti-polinema.github.io/flutter-codelab/16-flutter-fundamental-bagian-1/#7

1. Selesaikan Praktikum 3 dan 4, lalu dokumentasikan dan push ke repository Anda berupa screenshot hasil pekerjaan beserta penjelasannya di file README.md!
2. Pada praktikum 4 mulai dari Langkah 3 sampai 6, buatlah file widget tersendiri di folder basic_widgets, kemudian pada file main.dart cukup melakukan import widget sesuai masing-masing langkah tersebut!
3. Selesaikan Codelabs: Your first Flutter app, lalu buatlah laporan praktikumnya dan push ke repository GitHub Anda!
4. README.md berisi: capture hasil akhir tiap praktikum (side-by-side, bisa juga berupa file GIF agar terlihat proses perubahan ketika ada aksi dari pengguna) di browser dan perangkat fisik (device) dengan menampilkan NIM dan Nama Anda sebagai ciri pekerjaan Anda. Jika mode developer di perangkat HP Anda belum aktif, silakan cari di internet cara mengaktifkannya!
5. Kumpulkan berupa link repository/commit GitHub Anda ke Assignment ini !

# <b>Praktikum 3: Menerapkan Widget Dasar</b>

<b>Langkah 1: Text Widget</b>

Buat folder baru basic_widgets di dalam folder lib. Kemudian buat file baru di dalam basic_widgets dengan nama text_widget.dart. Ketik atau salin kode program berikut ke project hello_world Anda pada file text_widget.dart.

    import 'package:flutter/material.dart';

    class MyTextWidget extends StatelessWidget {
        const MyTextWidget({Key? key}) : super(key: key);

        @override
        Widget build(BuildContext context) {
            return const Text(
                "Nama saya Fulan, sedang belajar Pemrograman Mobile",
                style: TextStyle(color: Colors.red, fontSize: 14),
                textAlign: TextAlign.center);
        }
    }

> **_Perhatian:_**  Gantilah teks <b>Fulan</b> dengan nama lengkap Anda.

Lakukan import file text_widget.dart ke main.dart, lalu ganti bagian text widget dengan kode di atas. Maka hasilnya seperti gambar berikut. Screenshot hasil milik Anda, lalu dibuat laporan pada file README.md.

![Alt text](/images/image-4.png)

<b>Jawab:</b>
1. Membuat folder baru dan file baru dengan isi kode diatas dan mengubah Fulan menjadi nama lengkap.

![Alt text](/images/image.png)

2. Mengubah isi main.dart untuk menampilkan widget yang telah dibuat pada langkah 1.

![Alt text](/images/image-1.png)

3. Menambahkan import folder agar class dapat diidentifikasi pada file main.dart.

![Alt text](/images/image-2.png)

4. Hasil running program di website.

![Alt text](/images/image-3.png)

5. Hasil running program di device.

![Alt text](/images/image-12.png)

<b>Langkah 2: Image Widget</b>

Buat sebuah file image_widget.dart di dalam folder basic_widgets dengan isi kode berikut

    import 'package:flutter/material.dart';

    class MyImageWidget extends StatelessWidget {
        const MyImageWidget({Key? key}) : super(key: key);

        @override
        Widget build(BuildContext context) {
            return const Image(
                /images/image: AssetImage("logo_polinema.jpg")
            );
        }
    }

Lakukan penyesuaian asset pada file pubspec.yaml dan tambahkan file logo Anda di folder assets project hello_world.

    flutter:
        assets:
            - logo_polinema.jpg

Jangan lupa sesuaikan kode dan import di file main.dart kemudian akan tampil gambar seperti berikut.

![Alt text](/images/image-5.png)

<b>Jawab:</b>

1. Membuat file baru pada folder basic_widgets lalu mengisikan kode seperti berikut.

![Alt text](/images/image-6.png)

2. Membuat folder assets pada root folder dan tambahkan folder images(opsional), masukkan gambar logo_polinema disana.

![Alt text](/images/image-7.png)

3. Ubah isi pubspec.yaml agar direktori assets dapat terbaca oleh aplikasi flutter

![Alt text](/images/image-8.png)

4. Ubah isi main.dart untuk menampilkan gambar logo_polinema.png

![Alt text](/images/image-9.png)

5. Tambahkan import package agar class dari file image_widget.dart dapat dipanggil.

![Alt text](/images/image-10.png)

6. Hasil running program di website.

![Alt text](/images/image-11.png)

7. Hasil running program di device.

![Alt text](/images/image-13.png)

# <b>Praktikum 4: Menerapkan Widget Material Design dan iOS Cupertino</b>

Selesaikan langkah-langkah praktikum berikut ini dengan melanjutkan project hello_world Anda. Lakukan langkah yang sama seperti pada Praktikum 3, yaitu setiap widget dibuat file sendiri lalu import ke main.dart dan screenshot hasilnya.

<b>Langkah 1: Cupertino Button dan Loading Bar</b>

Buat file di basic_widgets > loading_cupertino.dart. Import stateless widget dari material dan cupertino. Lalu isi kode di dalam method Widget build adalah sebagai berikut.

    return MaterialApp(
        home: Container(
            margin: const EdgeInsets.only(top: 30),
            color: Colors.white,
            child: Column(
                children: <Widget>[
                    CupertinoButton(
                        child: const Text("Contoh button"),
                        onPressed: () {},
                    ),
                    const CupertinoActivityIndicator(),
                ],
            ),
        ),
    );

<b>Jawab:</b>

1. Membuat file baru pada folder basic_widget dari Praktikum sebelumnya lalu isikan kode diatas.

![Alt text](/images/image-14.png)

> **_Note:_**  Sebelum menambahkan kode pada langkah 1, tambahkan import package material dan cupertino terlebih dahulu. Setelah itu tambahkan stateless widget.

2. Memasukkan class yang telah dibuat pada file loading_cupertino.dart ke bagian MaterialApp di main.dart.

![Alt text](/images/image-15.png)

3. Tambahkan import package file loading_cupertino.dart agar class LoadCupertino() dapat dipanggil.

![Alt text](/images/image-16.png)

4. Hasil running program di website.

![Alt text](/images/image-17.png)

5. Hasil running program di device.

![Alt text](/images/image-18.png)

<b>Langkah 2: Floating Action Button (FAB)</b>

Button widget terdapat beberapa macam pada flutter yaitu ButtonBar, DropdownButton, TextButton, FloatingActionButton, IconButton, OutlineButton, PopupMenuButton, dan ElevatedButton.

Buat file di basic_widgets > fab_widget.dart. Import stateless widget dari material. Lalu isi kode di dalam method Widget build adalah sebagai berikut.

    return MaterialApp(
        home: Scaffold(
            floatingActionButton: FloatingActionButton(
                onPressed: () {
                // Add your onPressed code here!
                },
                child: const Icon(Icons.thumb_up),
                backgroundColor: Colors.pink,
            ),
        ),
    );

<b>Jawab:</b>

1. Membuat file baru pada folder basic_widget dari Praktikum sebelumnya lalu isikan kode diatas.

![Alt text](/images/image-19.png)

> **_Note:_**  Sebelum menambahkan kode pada langkah 2, tambahkan import package material terlebih dahulu. Setelah itu tambahkan stateless widget.

2. Memasukkan class yang telah dibuat pada file fab_widget.dart ke bagian MaterialApp di main.dart.

![Alt text](/images/image-20.png)

3. Tambahkan import package file fab_widget.dart agar class FabWidget() dapat dipanggil.

![Alt text](/images/image-21.png)

4. Hasil running program di website.

![Alt text](/images/image-22.png)

5. Hasil running program di device.

![Alt text](/images/image-23.png)

<b>Langkah 3: Scaffold Widget</b>

Scaffold widget digunakan untuk mengatur tata letak sesuai dengan material design.

Ubah isi kode main.dart seperti berikut.

    import 'package:flutter/material.dart';

    void main() {
        runApp(const MyApp());
    }

    class MyApp extends StatelessWidget {
        const MyApp({Key? key}) : super(key: key);

        // This widget is the root of your application.
        @override
        Widget build(BuildContext context) {
            return MaterialApp(
                title: 'Flutter Demo',
                theme: ThemeData(
                    primarySwatch: Colors.red,
                ),
                home: const MyHomePage(title: 'My Increment App'),
            );
        }
    }

    class MyHomePage extends StatefulWidget {
        const MyHomePage({Key? key, required this.title}) : super(key: key);

        final String title;

        @override
        State<MyHomePage> createState() => _MyHomePageState();
    }

    class _MyHomePageState extends State<MyHomePage> {
        int _counter = 0;

        void _incrementCounter() {
            setState(() {
            _counter++;
        });
    }

    @override
    Widget build(BuildContext context) {
        return Scaffold(
            appBar: AppBar(
                title: Text(widget.title),
            ),
            body: Center(
                child: Column(
                    mainAxisAlignment: MainAxisAlignment.center,
                    children: <Widget>[
                        const Text(
                            'You have pushed the button this many times:',
                        ),
                        Text(
                            '$_counter',
                            style: Theme.of(context).textTheme.headline4,
                        ),
                    ],
                ),
            ),
            bottomNavigationBar: BottomAppBar(
                child: Container(
                    height: 50.0,
                ),
            ),
            floatingActionButton: FloatingActionButton(
                onPressed: _incrementCounter,
                tooltip: 'Increment Counter',
                child: const Icon(Icons.add),
            ), 
            floatingActionButtonLocation: FloatingActionButtonLocation.centerDocked,
            );
        }
    }

<b>Jawab:</b>

> **_Note:_**  Pada praktikum 4 mulai dari Langkah 3 sampai 6, buatlah file widget tersendiri di folder basic_widgets, kemudian pada file main.dart cukup melakukan import widget sesuai masing-masing langkah tersebut!

1. Membuat file baru pada folder basic_widgets setelah itu inputkan kode diatas.

![Alt text](/images/image-24.png)

2. Memanggil class yang sudah dibuat pada file scaffold_widget ke main.dart.

![Alt text](/images/image-25.png)

3. Menambahkan import package yang mengarah ke file scaffold_widget agar class ScaffoldWidget dapat dipanggil.

![Alt text](/images/image-26.png)

4. Hasil running program di website

![Alt text](/images/image-27.png)

5. Hasil running program di device

![Alt text](/images/image-28.png)

<b>Langkah 4: Dialog Widget</b>

Dialog widget pada flutter memiliki dua jenis dialog yaitu AlertDialog dan SimpleDialog.

Ubah isi kode main.dart seperti berikut.

    class MyApp extends StatelessWidget {
        const MyApp({Key? key}) : super(key: key);

        @override
        Widget build(BuildContext context) {
            return const MaterialApp(
                home: Scaffold(
                    body: MyLayout(),
                ),
            );
        }
    }

    class MyLayout extends StatelessWidget {
        const MyLayout({Key? key}) : super(key: key);

        @override
        Widget build(BuildContext context) {
            return Padding(
                padding: const EdgeInsets.all(8.0),
                child: ElevatedButton(
                    child: const Text('Show alert'),
                    onPressed: () {
                        showAlertDialog(context);
                    },
                ),
            );
        }
    }

    showAlertDialog(BuildContext context) {
        // set up the button
        Widget okButton = TextButton(
            child: const Text("OK"),
            onPressed: () {
                Navigator.pop(context);
            },
        );

        // set up the AlertDialog
        AlertDialog alert = AlertDialog(
            title: const Text("My title"),
            content: const Text("This is my message."),
            actions: [
                okButton,
            ],
        );

        // show the dialog
        showDialog(
            context: context,
            builder: (BuildContext context) {
                return alert;
            },
        );
    }

<b>Jawab:</b>

> **_Note:_**  Pada praktikum 4 mulai dari Langkah 3 sampai 6, buatlah file widget tersendiri di folder basic_widgets, kemudian pada file main.dart cukup melakukan import widget sesuai masing-masing langkah tersebut!

1. Membuat file baru pada folder basic_widgets setelah itu inputkan kode diatas.

![Alt text](/images/image-30.png)

> **_Note:_**  Tambahkan package material terlebih dahulu agar tidak terjadi error.

2. Memanggil class yang sudah dibuat pada file dialog_widget ke main.dart.

![Alt text](/images/image-31.png)

3. Menambahkan import package yang mengarah ke file dialog_widget agar class DialogWidget dapat dipanggil.

![Alt text](/images/image-32.png)

4. Hasil running program di website

![Alt text](/images/image-29.png)

5. Hasil running program di device

![Alt text](/images/image-33.png)

<b>Langkah 5: Input dan Selection Widget</b>

Flutter menyediakan widget yang dapat menerima input dari pengguna aplikasi yaitu antara lain Checkbox, Date and Time Pickers, Radio Button, Slider, Switch, TextField.

Contoh penggunaan TextField widget adalah sebagai berikut:

    class MyApp extends StatelessWidget {
        const MyApp({Key? key}) : super(key: key);

        @override
        Widget build(BuildContext context) {
            return MaterialApp(
                home: Scaffold(
                    appBar: AppBar(title: const Text("Contoh TextField")),
                    body: const TextField(
                        obscureText: false,
                        decoration: InputDecoration(
                            border: OutlineInputBorder(),
                            labelText: 'Nama',
                        ),
                    ),
                ),
            );
        }
    }

<b>Jawab:</b>

> **_Note:_**  Pada praktikum 4 mulai dari Langkah 3 sampai 6, buatlah file widget tersendiri di folder basic_widgets, kemudian pada file main.dart cukup melakukan import widget sesuai masing-masing langkah tersebut!

1. Membuat file baru pada folder basic_widgets setelah itu inputkan kode diatas.

![Alt text](/images/image-34.png)

> **_Note:_**  Tambahkan package material terlebih dahulu agar tidak terjadi error.

2. Memanggil class yang sudah dibuat pada file inselect_widget ke main.dart.

![Alt text](/images/image-35.png)

3. Menambahkan import package yang mengarah ke file inselect_widget agar class InputSelectionWidget dapat dipanggil.

![Alt text](/images/image-36.png)

4. Hasil running program di website

![Alt text](/images/image-37.png)

5. Hasil running program di device

![Alt text](/images/image-38.png)

<b>Langkah 6: Date and Time Pickers</b>

Date and Time Pickers termasuk pada kategori input dan selection widget, berikut adalah contoh penggunaan Date and Time Pickers.

    import 'dart:async';
    import 'package:flutter/material.dart';

    void main() => runApp(const MyApp());

    class MyApp extends StatelessWidget {
        const MyApp({Key? key}) : super(key: key);

        @override
        Widget build(BuildContext context) {
            return const MaterialApp(
                title: 'Contoh Date Picker',
                home: MyHomePage(title: 'Contoh Date Picker'),
            );
        }
    }

    class MyHomePage extends StatefulWidget {
        const MyHomePage({Key? key, required this.title}) : super(key: key);

        final String title;

        @override
        _MyHomePageState createState() => _MyHomePageState();
    }

    class _MyHomePageState extends State<MyHomePage> {
        // Variable/State untuk mengambil tanggal
        DateTime selectedDate = DateTime.now();

        //  Initial SelectDate FLutter
        Future<void> _selectDate(BuildContext context) async {
            // Initial DateTime FIinal Picked
            final DateTime? picked = await showDatePicker(
                context: context,
                initialDate: selectedDate,
                firstDate: DateTime(2015, 8),
                lastDate: DateTime(2101));
            if (picked != null && picked != selectedDate) {
                setState(() {
                    selectedDate = picked;
                });
            }
        }

        @override
        Widget build(BuildContext context) {
            return Scaffold(
                appBar: AppBar(
                    title: Text(widget.title),
                ),
                body: Center(
                    child: Column(
                        mainAxisSize: MainAxisSize.min,
                        children: <Widget>[
                            Text("${selectedDate.toLocal()}".split(' ')[0]),
                            const SizedBox(
                                height: 20.0,
                            ),
                            ElevatedButton(
                                onPressed: () => {
                                    _selectDate(context),
                                    // ignore: avoid_print
                                    print(selectedDate.day + selectedDate.month + selectedDate.year)
                                },
                                child: const Text('Pilih Tanggal'),
                            ),
                        ],
                    ),
                ),
            );
        }
    }

<b>Jawab:</b>

> **_Note:_**  Pada praktikum 4 mulai dari Langkah 3 sampai 6, buatlah file widget tersendiri di folder basic_widgets, kemudian pada file main.dart cukup melakukan import widget sesuai masing-masing langkah tersebut!

1. Membuat file baru pada folder basic_widgets setelah itu inputkan kode diatas.

![Alt text](/images/image-39.png)

2. Memanggil class yang sudah dibuat pada file datetime_widget ke main.dart.

![Alt text](/images/image-40.png)

3. Menambahkan import package yang mengarah ke file datetime_widget agar class DateTimeWidget dapat dipanggil.

![Alt text](/images/image-41.png)

4. Hasil running program di website

![Alt text](/images/image-42.png)

![Alt text](/images/image-43.png)

5. Hasil running program di device

![Alt text](/images/image-44.png)

![Alt text](/images/image-45.png)