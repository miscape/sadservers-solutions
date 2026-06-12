## Passo 1: Estrai solo la prima colonna degli IP
```bash
cut -d ' ' -f 1 /home/admin/access.log > solo_ip.txt
```

## Passo 2: Ordina gli IP
```bash
sort solo_ip.txt > ip_ordinati.txt
```

## Passo 3: Conta quante volte appare ogni IP
```bash
uniq -c ip_ordinati.txt > ip_contati.txt
```

## Passo 4: Trova il numero più alto
```bash
sort -n ip_contati.txt
```

## Passo 5: Salva la soluzione
```bash
echo "IL_TUO_IP_TROVATO" > /home/admin/highestip.txt
```