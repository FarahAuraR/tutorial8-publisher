## REFLEKSI 1
###### 1. How many data your publlsher program will send to the message broker in one run?
Program publisher akan mengirimkan lima data ke message brocker dalam satu kali eksekusi.

###### 2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
URL "amqp://guest:guest@localhost:5672" digunakan di kedua program subscriber dan publisher yang berarti keduanya terhubung ke server AMQP dengan kredensial yang sama (nama pengguna dan sandi "guest"), serta server berjalan pada localhost dengan port 5672.

###### Running RabbitMQ as message broker
![Commit 3](assets/images/commit3.png)

###### Sending and processing event
![Commit 4](assets/images/commit4.png)
###### what was happening?
Ketika menjalankan cargo run pada subscriber lalu menjalankan cargo run pada publisher, dapat terlihat bahwa publisher mengirim 5 event ke message broker yang kemudian di consume oleh subscriber.

###### Monitoring chart based on publisher
![Commit 5](assets/images/commit5.png)
###### how the spike got to do with running the publisher?
Spike pada grafik menunjukkan tingkat pesan yang mengukur seberapa banyak pesan yang dikirimkan ke saluran dalam interval waktu. Karena publisher mengirim beberapa pesan ke message broker, tingkat pesan meningkat, sehingga menyebabkan spike pada grafik.