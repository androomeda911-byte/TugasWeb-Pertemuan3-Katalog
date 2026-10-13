/* ==========================================================
   TUGAS RUTIN 3
   JAVASCRIPT KATALOG PRODUK RESPONSIF
   ========================================================== */


/*
   Menunggu sampai seluruh HTML selesai dimuat
*/

document.addEventListener("DOMContentLoaded", () => {


    /*
       Mengambil semua tombol
       yang terdapat di dalam product-card
    */

    const buttons =
        document.querySelectorAll(".product-card button");


    /*
       Melakukan perulangan
       untuk setiap tombol
    */

    buttons.forEach((button) => {


        /*
           Event ketika tombol diklik
        */

        button.addEventListener("click", () => {


            /*
               Mengambil nama produk
               dari card yang tombolnya diklik
            */

            const productCard =
                button.closest(".product-card");


            const productName =
                productCard
                    .querySelector(".card-title")
                    .textContent
                    .trim();


            /*
               Mengubah teks tombol
            */

            button.innerHTML =
                '<i class="bi bi-check-circle"></i> Ditambahkan';


            /*
               Mengubah warna tombol
            */

            button.classList.remove(
                "btn-outline-primary"
            );


            button.classList.add(
                "btn-success"
            );


            /*
               Menampilkan informasi
               di Console Browser
            */

            console.log(
                `${productName} ditambahkan ke keranjang.`
            );

        });

    });

});