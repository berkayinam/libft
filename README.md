# libft

42 okulunun ilk projesi olan libft, C dilinde temel bir kütüphane oluşturmayı amaçlayan bir projedir. 125/100

## 📚 Proje Hakkında

libft projesi, C standart kütüphanesindeki bazı fonksiyonları yeniden yazarak ve yeni fonksiyonlar ekleyerek kendi kütüphanemizi oluşturmayı hedeflemektedir. Bu proje, C programlama dilinin temellerini pekiştirmek ve bellek yönetimi konusunda deneyim kazanmak için tasarlanmıştır.

## 💻 Teknolojiler

- C Programlama Dili
- Makefile
- Shell Script
- Git

## 🛠️ Kurulum

### Gereksinimler
- GCC Derleyici
- Make
- Git

### Derleme
```bash
git clone https://github.com/berkayinam/libft.git
cd libft
make
```

### Bonus Fonksiyonlar İçin
```bash
make bonus
```

## 📝 Fonksiyonlar

### Libc Fonksiyonları
- [x] ft_isalpha
- [x] ft_isdigit
- [x] ft_isalnum
- [x] ft_isascii
- [x] ft_isprint
- [x] ft_strlen
- [x] ft_memset
- [x] ft_bzero
- [x] ft_memcpy
- [x] ft_memmove
- [x] ft_strlcpy
- [x] ft_strlcat
- [x] ft_toupper
- [x] ft_tolower
- [x] ft_strchr
- [x] ft_strrchr
- [x] ft_strncmp
- [x] ft_memchr
- [x] ft_memcmp
- [x] ft_strnstr
- [x] ft_atoi

### Ek Fonksiyonlar
- [x] ft_substr
- [x] ft_strjoin
- [x] ft_strtrim
- [x] ft_split
- [x] ft_itoa
- [x] ft_strmapi
- [x] ft_striteri
- [x] ft_putchar_fd
- [x] ft_putstr_fd
- [x] ft_putendl_fd
- [x] ft_putnbr_fd

### Bonus Fonksiyonlar
- [x] ft_lstnew
- [x] ft_lstadd_front
- [x] ft_lstsize
- [x] ft_lstlast
- [x] ft_lstadd_back
- [x] ft_lstdelone
- [x] ft_lstclear
- [x] ft_lstiter
- [x] ft_lstmap

## 🎯 42 Proje Gereksinimleri

### Zorunlu Kısım
- [x] Libc fonksiyonları
- [x] Ek fonksiyonlar
- [x] Makefile kuralları
- [x] Bellek yönetimi
- [x] Header dosyası

### Bonus Kısım
- [x] Bağlı liste fonksiyonları
- [x] Bonus Makefile kuralları

## 📚 Fonksiyon Örnekleri

### String İşlemleri
```c
char *ft_strjoin(char const *s1, char const *s2)
{
    char    *str;
    size_t  i;
    size_t  j;

    if (!s1 || !s2)
        return (NULL);
    str = (char *)malloc(ft_strlen(s1) + ft_strlen(s2) + 1);
    if (!str)
        return (NULL);
    i = 0;
    while (s1[i])
    {
        str[i] = s1[i];
        i++;
    }
    j = 0;
    while (s2[j])
        str[i++] = s2[j++];
    str[i] = '\0';
    return (str);
}
```

### Bellek İşlemleri
```c
void *ft_memset(void *b, int c, size_t len)
{
    unsigned char *ptr;

    ptr = (unsigned char *)b;
    while (len--)
        *ptr++ = (unsigned char)c;
    return (b);
}
```

## 🔍 Test ve Doğrulama

### Unit Test
```bash
make test
```

### Bellek Kontrolü
```bash
valgrind ./test_program
```

## 🐛 Hata Ayıklama

### Yaygın Hatalar
1. Bellek Sızıntıları
   - malloc kontrolü
   - free kullanımı
   - NULL kontrolleri

2. Segmentation Fault
   - Pointer kontrolleri
   - Array sınırları
   - NULL dereferencing

## 📈 Optimizasyon İpuçları

1. Bellek Yönetimi
   - Gereksiz malloc kullanımından kaçınma
   - Buffer boyutu optimizasyonu
   - Bellek fragmentasyonu kontrolü

2. Performans
   - Gereksiz döngülerden kaçınma
   - Algoritma karmaşıklığı
   - Cache kullanımı

## 📝 Lisans

Bu proje [MIT](LICENSE) lisansı altında lisanslanmıştır.

## 📚 Kaynaklar

- [C Programming Language](https://www.cprogramming.com/)
- [GNU C Library Reference](https://www.gnu.org/software/libc/manual/)
- [42 Docs](https://harm-smits.github.io/42docs/)

---

⭐️ Bu projeyi beğendiyseniz yıldız vermeyi unutmayın!
