# tugas-parkir-langganan

void main() {
  String status = "member";
  int jamParkir = 3;
  bool tiketHilang = false;

  if (tiketHilang) {
    print("Tiket hilang");
    print("Denda: Rp20000");
  } else if (status == "member") {
    print("Status: Member bulanan");
    print("Biaya parkir: Gratis");
  } else {
    int tarif = 5000;

    if (jamParkir > 1) {
      tarif = tarif + (jamParkir - 1) * 3000;
    }

    print("Status: Non-member");
    print("Lama parkir: $jamParkir jam");
    print("Biaya parkir: Rp$tarif");
  }
}
