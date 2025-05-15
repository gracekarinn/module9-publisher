Pertanyaan a

Program publisher mengirim **5 pesan** ke broker.
Setiap pesan berisi `user_id` dan `user_name`, total data kira-kira **150 byte** dalam satu kali jalan (perkiraan kasar dengan overhead serialisasi Borsh).


Pertanyaan b

URL `"amqp://guest:guest@localhost:5672"` di publisher dan subscriber sama artinya **keduanya terhubung ke broker RabbitMQ yang sama di komputer lokal**, dengan user `guest` dan port default AMQP `5672`. Jadi, pesan dari publisher bisa langsung diterima oleh subscriber.

![Screenshot](./Screenshot%202025-05-15%20at%2021.28.45.png)

![Screenshot](./cape.png)

![Screenshot](./image-3.png)
