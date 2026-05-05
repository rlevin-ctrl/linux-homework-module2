# Домашнє завдання №2 — Файлова система і права доступу  
**Студент:** Роберт Левін

---

## Завдання 1. Ієрархія каталогів Linux

### 1. Перейти в кореневий каталог `/` і показати вміст

```bash
cd /
ls
```

**Результат:**  
<img width="796" height="179" alt="image" src="https://github.com/user-attachments/assets/7fa8a13d-8390-4f3d-9a6c-25cc53a04930" />

---

### 2. Перейти в `/etc` і показати вміст

```bash
cd /etc
ls
```

**Результат:**  
<img width="795" height="350" alt="image" src="https://github.com/user-attachments/assets/e7552f33-4399-4683-945c-5eef54720d40" />
<img width="786" height="531" alt="image" src="https://github.com/user-attachments/assets/9ec47cd8-8e7b-4d66-bd5a-f753a9e8f6b4" />

---

### 3. Перейти у каталог `/home` і показати список користувачів

```bash
cd /home
ls
```

**Результат:**  
<img width="805" height="67" alt="image" src="https://github.com/user-attachments/assets/30fad94e-3b12-492e-a151-c5e7e3961258" />

---

## Завдання 2. Файли, каталоги та посилання

### Створення каталогу

```bash
mkdir ~/lab2
```

### Створення файлу

```bash
echo "test" > ~/lab2/file.txt
```

### Копіювання файлу

```bash
cp ~/lab2/file.txt ~/lab2/file_copy.txt
```

### Перейменування копії

```bash
mv ~/lab2/file_copy.txt ~/lab2/file_renamed.txt
```

### Створення жорсткого посилання

```bash
ln ~/lab2/file.txt ~/lab2/hardlink.txt
```

### Створення символічного посилання

```bash
ln -s ~/lab2/file.txt ~/lab2/symlink.txt
```

### Пошук файлу по імені

```bash
find ~ -name "file.txt"
```

**Результат:**  
<img width="810" height="135" alt="image" src="https://github.com/user-attachments/assets/64ca3605-8974-4f42-bb3f-fed6ecf64b18" />

---

## Завдання 3. Права доступу

### Перегляд прав файлу

```bash
ls -l ~/lab2/file.txt
```

**Результат:**  
<img width="722" height="45" alt="image" src="https://github.com/user-attachments/assets/256586f3-4d8d-4349-80ab-daab459654b0" />

---

### Надати файлу права тільки на читання

```bash
chmod 444 ~/lab2/file.txt
```

### Додати власнику право на запис

```bash
chmod u+w ~/lab2/file.txt
```

### Переглянути значення umask

```bash
umask
```

**Результат:**  
<img width="791" height="132" alt="image" src="https://github.com/user-attachments/assets/f05d7e2c-c7bd-4a3b-a367-4cd9f5681592" />

---

### Встановити нове значення umask

```bash
umask 022
```

---

## Завдання 4. Користувачі

### Створення нового користувача

```bash
sudo adduser trainee
```

**Результат:**  
<img width="793" height="463" alt="image" src="https://github.com/user-attachments/assets/42efe92f-2f4f-4ec2-9d9f-ffd47337d494" />

---

### Додати користувача до sudo-групи

```bash
sudo usermod -aG sudo trainee
```

### Перевірити, що користувач існує

```bash
grep trainee /etc/passwd
```

**Результат:**  
<img width="803" height="178" alt="image" src="https://github.com/user-attachments/assets/5d29d580-d0e2-4050-bccf-0f7f6aaf734b" />


---
