rus_lc = 'абвгдежзийклмнопрстуфхцчшщъыьэюяабвгдежзийклмнопрстуфхцчшщъыьэюя'
rus_uc = 'АБВГДЕЖЗИЙКЛМНОПРСТУФХЦЧШЩЪЫЬЭЮЯАБВГДЕЖЗИЙКЛМНОПРСТУФХЦЧШЩЪЫЬЭЮЯ'


svar = input('Введите фразу, которую необходимо зашифровать: ')
n = int(input('Введите сдвиг: '))

for l in svar:
    if l.lower() in rus_lc:
        lang = 'ru'
        break
    elif l.lower() in [chr(i) for i in range(97, 123)]:
        lang = 'eng'
        break
enc_s = ''
if lang == 'ru':
    for i in range(len(svar)):
        if svar[i] in rus_lc:
             enc_s += rus_lc[(rus_lc.find(svar[i]) + n) % 32]
        elif svar[i] in rus_uc:
            enc_s += rus_uc[(rus_uc.find(svar[i]) + n) % 32]
        else:
            enc_s += svar[i]
    print(enc_s)
elif lang == 'eng':
    for word in svar:
        for l in word:
            if l == l.lower() and l.isalpha():
                enc_s += chr(97 + (ord(l) - 97 + n) % 26)
            elif l == l.upper() and l.isalpha():
                enc_s += chr(65 + (ord(l) - 65 + n) % 26)
            else:
                enc_s += l
    print(enc_s)
else:
    print('Язык не опознан.')
