# calculator
//Hesap Makinesi
//bilgisayarımda gelişen bir problemden dolayı dosyayı githuba ekleyemedim :(

actor hesap_makinesi {
  var hucre: Int = 0;
  
  // toplama fonksiyonu
  public func toplama(s: Int) : async Int {
    hucre += s;
    return hucre;
  };

  // çıkarma fonksiyonu
  public func cikarma(s: Int) : async Int {
    hucre -= s;
    return hucre;
  };

  // çarpma fonksiyonu
  public func carpma(s: Int) : async Int {
    hucre *= s;
    return hucre;
  };

  // bölme fonksiyonu
  public func bolme(s: Int) : async ?Int {
    if (s == 0) {
      return null;
    } else {
      hucre /= s;
      return ?hucre;
    }
  };

  // temizle fonksiyonu
  public func temizle() : async () {
    hucre := 0;  
  };
};
