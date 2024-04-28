Tips ini memudahkan kita agar otomatis menambahkan tanda bintang (*) pada label saat inputan nya di beri parameter required.
Tips ini hanya berlaku jika kalian menggunakan Bootstrap atau susunan seperti :
```
<div class="mb-2">
  <label>Nama label</label>
  <input name="nama" required />
</div>
```

Cara nya cukup sederhana, kalian cukup menambahkan kode javascript pada halaman nya.
Kode nya seperti di bawah :
```
window.addEventListener("DOMContentLoaded", (event) => {
  const formGroups = document.querySelectorAll(".mb-2");
  formGroups.forEach((formGroup) => {
    const input = formGroup.querySelector(
      "input[required], select[required]"
    );
    if (input) {
      const label = formGroup.querySelector("label");
      label.innerHTML += ' <span class="text-danger">*</span>';
    }
  });
});
```
