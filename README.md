Pertanyaan a

Program publisher mengirim **5 pesan** ke broker.
Setiap pesan berisi `user_id` dan `user_name`, total data kira-kira **150 byte** dalam satu kali jalan (perkiraan kasar dengan overhead serialisasi Borsh).


Pertanyaan b

URL `"amqp://guest:guest@localhost:5672"` di publisher dan subscriber sama artinya **keduanya terhubung ke broker RabbitMQ yang sama di komputer lokal**, dengan user `guest` dan port default AMQP `5672`. Jadi, pesan dari publisher bisa langsung diterima oleh subscriber.

![Screenshot](./Screenshot%202025-05-15%20at%2021.28.45.png)

![Screenshot](./cape.png)

![Screenshot](./image-3.png)

![Screenshot](./image-4.png)

Lonjakan pada grafik tersebut menunjukkan peningkatan tajam dalam jumlah pesan yang diproses per detik. Hal ini terjadi karena publisher mengirim beberapa pesan secara cepat dan berturut-turut ke message broker, sehingga menyebabkan tingkat pengiriman pesan melonjak dalam waktu singkat dan terlihat sebagai spike pada grafik.