# vendor
pada WordCount:
class WordCount { ... }: Ini adalah deklarasi sebuah kelas bernama WordCount. Kelas ini memiliki satu metode publik yaitu countWords.
public function countWords($sentence) { ... }: Ini adalah deklarasi dari metode countWords. Metode ini menerima satu parameter yaitu $sentence.
explode(" ", $sentence): Fungsi explode digunakan untuk memecah sebuah string menjadi array berdasarkan delimiter tertentu. Di sini, delimiter yang digunakan adalah spasi (" "), sehingga kalimat akan dipecah menjadi kata-kata.
count(explode(" ", $sentence)): Hasil dari explode akan menghasilkan array dari kata-kata. Fungsi count digunakan untuk menghitung jumlah elemen dalam array. Dalam hal ini, ini akan menghitung jumlah kata dalam kalimat.
return count(explode(" ", $sentence));: Metode ini mengembalikan jumlah kata dalam kalimat yang diberikan sebagai parameter.
pada SimpleTest:
// Path to run ./vendor/bin/phpunit --bootstrap vendor/autoload.php FileName.php: Ini adalah sebuah komentar yang memberikan petunjuk tentang cara menjalankan pengujian menggunakan PHPUnit. Anda perlu menjalankan perintah ini dari terminal untuk menjalankan pengujian.
use PHPUnit\Framework\TestCase;: Ini adalah pernyataan untuk mengimpor kelas TestCase dari framework PHPUnit. TestCase adalah kelas dasar yang digunakan untuk membuat pengujian pada PHPUnit.
require_once "Wordcount.php";: Ini adalah pernyataan yang memasukkan (include) file WordCount.php ke dalam file ini. Hal ini dilakukan karena kelas SimpleTest akan melakukan pengujian terhadap kelas WordCount.
class SimpleTest extends TestCase { ... }: Ini adalah deklarasi kelas SimpleTest yang merupakan subkelas dari TestCase. Dalam kelas ini, kita akan menulis metode-metode pengujian (test cases).
public function testCountWords() { ... }: Ini adalah deklarasi dari metode pengujian testCountWords. Metode ini akan melakukan pengujian terhadap metode countWords dari kelas WordCount.
$Wc = new WordCount();: Ini adalah pembuatan instance dari kelas WordCount. Instance ini akan digunakan untuk memanggil metode countWords yang akan diuji.
$TestSentence = "My name is Joko";: Ini adalah deklarasi variabel $TestSentence yang berisi sebuah kalimat.
$WordCount = $Wc->countWords($TestSentence);: Di sini, metode countWords dari kelas WordCount dipanggil dengan parameter $TestSentence dan hasilnya disimpan dalam variabel $WordCount.
$this->assertEquals(4, $WordCount);: Ini adalah pengujian (assertion). Pernyataan ini membandingkan nilai dari $WordCount dengan nilai ekspektasi yaitu 4. Jika kedua nilai sama, maka pengujian ini akan lulus.
