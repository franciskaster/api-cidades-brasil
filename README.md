# 🇧🇷 Estados e Municípios do Brasil

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python](https://img.shields.io/badge/Python-3.6+-blue.svg)](https://www.python.org/)
[![Data Source](https://img.shields.io/badge/Data%20Source-IBGE-green.svg)](https://www.ibge.gov.br/)

> **Repositório atualizado com dados oficiais dos 5.570 municípios brasileiros organizados por estado**

Este repositório contém uma lista completa e atualizada de todos os estados e municípios do Brasil, extraída diretamente da fonte oficial do IBGE. Os dados estão organizados de forma estruturada e prontos para uso em aplicações web, mobile ou desktop.

## 📊 Estatísticas dos Dados

- **27 Estados** (incluindo o Distrito Federal)
- **5.570 Municípios** totais
- **Codificação UTF-8** para preservar acentos e caracteres especiais
- **Fonte oficial**: IBGE - Instituto Brasileiro de Geografia e Estatística
- **Última atualização**: 17/10/2025

## 🚀 Como Usar

### Download Direto
```bash
# Clone o repositório
git clone https://github.com/seu-usuario/estado-cidades-brasil.git
cd estado-cidades-brasil
```

### Uso em JavaScript/Node.js
```javascript
// Carregar dados
const municipios = require('./municipios.json');

// Listar todos os estados
const estados = Object.keys(municipios);
console.log(estados);

// Buscar municípios de um estado
const cidadesSP = municipios['São Paulo'];
console.log(`São Paulo tem ${cidadesSP.length} municípios`);

// Buscar município específico
const encontrarMunicipio = (nome) => {
  for (const [estado, cidades] of Object.entries(municipios)) {
    if (cidades.includes(nome)) {
      return { estado, municipio: nome };
    }
  }
  return null;
};
```

### Uso em Python
```python
import json

# Carregar dados
with open('municipios.json', 'r', encoding='utf-8') as f:
    municipios = json.load(f)

# Listar estados
estados = list(municipios.keys())
print(f"Total de estados: {len(estados)}")

# Contar municípios por estado
for estado, cidades in municipios.items():
    print(f"{estado}: {len(cidades)} municípios")
```

## 📁 Estrutura do Projeto

```
estado-cidades-brasil/
├── README.md              # Este arquivo
├── municipios.json        # Dados completos em JSON
├── cidades.py            # Script de extração dos dados
├── index.html            # Site estático para visualização
└── LICENSE               # Licença MIT
```

## 🌐 Site de Demonstração

Acesse o [site estático](https://seu-usuario.github.io/estado-cidades-brasil/) para:
- 🔍 Buscar municípios por estado
- 📊 Visualizar estatísticas dos dados
- ⬇️ Download em diferentes formatos (JSON, CSV, XML)
- 📱 Interface responsiva e moderna

## 🔧 Script de Atualização

O arquivo `cidades.py` contém o script para extrair e atualizar os dados diretamente do IBGE:

```bash
# Instalar dependências
pip install requests beautifulsoup4

# Executar script de atualização
python cidades.py
```

## 📋 Formato dos Dados

```json
{
  "Acre": [
    "Assis Brasil",
    "Brasiléia",
    "Bujari",
    // ... outros municípios
  ],
  "Alagoas": [
    "Anadia",
    "Arapiraca",
    "Atalaia",
    // ... outros municípios
  ]
  // ... outros estados
}
```

## 🤝 Contribuindo

Contribuições são bem-vindas! Se você encontrar algum erro ou quiser sugerir melhorias:

1. Faça um fork do projeto
2. Crie uma branch para sua feature (`git checkout -b feature/AmazingFeature`)
3. Commit suas mudanças (`git commit -m 'Add some AmazingFeature'`)
4. Push para a branch (`git push origin feature/AmazingFeature`)
5. Abra um Pull Request

## 📝 Licença

Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.

## ⚠️ Importante

- Os dados são extraídos diretamente do site oficial do IBGE
- A lista é atualizada conforme as mudanças oficiais
- Caso encontre discrepâncias, abra uma [issue](https://github.com/seu-usuario/estado-cidades-brasil/issues)
- Para uso comercial, verifique as políticas do IBGE

## 📞 Contato

- **GitHub**: [@seu-usuario](https://github.com/seu-usuario)
- **Email**: seu-email@exemplo.com
- **Issues**: [Reportar problemas](https://github.com/seu-usuario/estado-cidades-brasil/issues)

---

⭐ **Se este projeto foi útil, considere dar uma estrela!**
