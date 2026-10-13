# Blazor ViaCEP

Aplicação em Blazor WebAssembly para consultar CEPs brasileiros usando a API pública do ViaCEP.

## Visão geral

Este projeto é uma simples interface web para buscar informações de endereço a partir de um CEP, exibindo dados como:

- Logradouro
- Complemento
- Bairro
- Cidade
- UF
- DDD

A aplicação valida o valor informado, remove caracteres não numéricos e faz a requisição diretamente à API do ViaCEP.

## Tecnologias utilizadas

- .NET 10
- Blazor WebAssembly
- C#
- HTML/CSS
- Bootstrap
- API pública ViaCEP

## Funcionalidades

- Entrada de CEP com validação
- Remoção automática de caracteres não numéricos
- Verificação de CEP inválido ou não encontrado
- Exibição do resultado em tabela
- Tratamento de erros de rede e requisição

## Pré-requisitos

Antes de executar o projeto, certifique-se de ter instalado:

- .NET SDK 10.0
- Um navegador moderno

## Como executar

1. Clone o repositório:

```bash
git clone https://github.com/GustavoMdancers/blazor-viacep-net.git
cd blazor-viacep-net
```

2. Restaure os pacotes:

```bash
dotnet restore
```

3. Execute a aplicação:

```bash
dotnet run --project BlazorViaCep/BlazorViaCep.csproj
```

4. Abra o endereço exibido no terminal no navegador.

## Estrutura do projeto

```text
blazor-viacep-net/
├── BlazorViaCep/
│   ├── Layout/
│   ├── Models/
│   ├── Pages/
│   ├── Properties/
│   ├── wwwroot/
│   ├── App.razor
│   ├── BlazorViaCep.csproj
│   ├── Program.cs
│   └── _Imports.razor
├── LICENSE
├── README.md
└── .gitignore
```

## Modelo de dados

A resposta da API do ViaCEP é convertida para a classe `Endereco`:

- `Cep`
- `Rua`
- `Complemento`
- `Bairro`
- `Cidade`
- `Uf`
- `Ibge`
- `Gia`
- `Ddd`
- `Siafi`

## Observações

- A consulta é feita diretamente para `https://viacep.com.br/ws/{cep}/json/`
- A aplicação roda no cliente, em ambiente WebAssembly
- O comportamento é simples e pensado para uso local e didático

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo [LICENSE](./LICENSE) para mais detalhes.
