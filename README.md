## REFLEKSI 1
###### 1. How many data your publlsher program will send to the message broker in one run?
Program publisher akan mengirimkan lima data ke message brocker dalam satu kali eksekusi.

###### 2. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
URL "amqp://guest:guest@localhost:5672" digunakan di kedua program subscriber dan publisher yang berarti keduanya terhubung ke server AMQP dengan kredensial yang sama (nama pengguna dan sandi "guest"), serta server berjalan pada localhost dengan port 5672.