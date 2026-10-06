# tugas-parkir-langganan

enum Kendaraan {
  motor,
  mobil
}

void main() {
  // Input
  Kendaraan kendaraan = Kendaraan.motor;
  int durasi = 150;

  // Menghitung jam dan sisa menit
  int jam = durasi ~/ 60;
  int sisaMenit = durasi % 60;

  // Sisa menit dibulatkan ke atas
  if (sisaMenit > 0) {
    jam = jam + 1;
  }

  // Minimal 1 jam
  if (jam < 1) {
    jam = 1;
  }

  int tarif = 0;

  // Menentukan tarif berdasarkan kendaraan
  switch (kendaraan) {
    case Kendaraan.motor:
      if (jam == 1) {
        tarif = 2000;
      } else {
        tarif = 2000 + (jam - 1) * 1000;
      }
      break;

    case Kendaraan.mobil:
      if (jam == 1) {
        tarif = 5000;
      } else {
        tarif = 5000 + (jam - 1) * 3000;
      }
      break;
  }

  // Menampilkan hasil
  print("=== PROGRAM TARIF PARKIR ===");

  if (kendaraan == Kendaraan.motor) {
    print("Kendaraan: Motor");
  } else {
    print("Kendaraan: Mobil");
  }

  print("Durasi: $durasi menit");
  print("Durasi dibulatkan: $jam jam");
  print("Sisa menit: $sisaMenit menit");
  print("Total tarif: Rp$tarif");
}
