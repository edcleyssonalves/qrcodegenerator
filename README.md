# QR PIX GENERATOR

QRPIX GENERATOR é uma biblioteca Python projetada para simplificar a geração de QR Codes para pagamentos via Pix. Ela permite criar rapidamente códigos Pix personalizados

## Principais Caracteristicas

- Geração automática de payloads Pix válidos.
- Suporte a qualquer tipo de chave Pix (CPF, CNPJ, e-mail ou telefone).
- Geração de Payload Pix: cria um payload no formato QRCP-S, conforme especificações do sistema Pix.
- Geração do Pix Copia e Cola: cria a linha digitável a partir do payload gerado, o codigo do Pix Copia e Cola é mostrado no saida.
- Leve, independente e fácil de integrar a projetos Python existentes.

## Instalação 

Instale a versão mais recente diretamente do PyPI usando pip:

```sh
pip install qrpix
```

## Uso básico

```sh
from payload import Payload

payload = Payload(
    nome="Maria José",
    chavepix="+5584994226558",
    valor="0.00",
    cidade="BRASIL",
    txtId="TesteQRPIX"
)

codigo_pix = payload.gerarPayload()
print("Pix Copia e Cola:", codigo_pix)

```

## Referência

 - [Manual BRCode](https://www.bcb.gov.br/content/estabilidadefinanceira/spb_docs/ManualBRCode.pdf)
 - [Códigos QR EMV](https://www.emvco.com/emv-technologies/qr-codes/)
 - [Pix EMV QRCode Tester](https://openpix.com.br/qrcode/scanner/)


## Tecnologias Utilizadas

![Python](https://img.shields.io/badge/Python_3.11+-3776AB?style=for-the-badge&logo=python&logoColor=white)

