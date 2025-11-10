# 📱 Guia de Markers para AR

Este guia explica como obter ou criar imagens de markers para usar com AR.js.

## 🎯 O que é um Marker?

Um marker é uma imagem especial que o AR.js reconhece através da câmera. Quando você aponta a câmera para o marker, objetos 3D aparecem sobre ele.

## 📥 Opção 1: Usar o Marker Hiro (Padrão)

O marker Hiro é o padrão do AR.js e já está configurado no seu projeto.

### Como obter:
1. **Baixar a imagem:**
   - Acesse: https://jeromeetienne.github.io/AR.js/data/images/HIRO.jpg
   - Ou baixe diretamente: [HIRO.jpg](https://jeromeetienne.github.io/AR.js/data/images/HIRO.jpg)

2. **Usar o marker:**
   - **Imprimir:** Imprima a imagem em papel (tamanho mínimo recomendado: 8cm x 8cm)
   - **Tela:** Abra a imagem em outro dispositivo (tablet, celular, computador)
   - **Apontar:** Aponte a câmera do seu dispositivo para o marker

### Características:
- ✅ Funciona imediatamente (já está configurado)
- ✅ Alta precisão de detecção
- ✅ Funciona bem em diferentes condições de luz

---

## 🎨 Opção 2: Criar um Marker Customizado

Você pode criar seu próprio marker personalizado usando ferramentas online.

### Ferramentas Recomendadas:

#### 1. **AR.js Marker Generator** (Recomendado)
- **URL:** https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html
- **Como usar:**
  1. Acesse o site
  2. Digite um número ou texto (ex: "CQT", "ARCO", "123")
  3. Clique em "Generate"
  4. Baixe o arquivo `.patt` (pattern)
  5. Baixe a imagem do marker (PNG ou JPG)

#### 2. **NFT Marker Creator**
- **URL:** https://carnaux.github.io/NFT-Marker-Creator/
- **Como usar:**
  1. Faça upload de uma imagem (PNG, JPG)
  2. A ferramenta gera o arquivo `.patt`
  3. Baixe ambos os arquivos

#### 3. **AR.js Documentation**
- **URL:** https://ar-js-org.github.io/AR.js-Docs/marker-based/
- Documentação completa sobre markers

### Configurando um Marker Customizado:

1. **Gerar o marker:**
   - Use uma das ferramentas acima
   - Baixe o arquivo `.patt` (pattern)
   - Baixe a imagem do marker (PNG/JPG)

2. **Adicionar ao projeto:**
   - Coloque o arquivo `.patt` em: `public/assets/markers/`
   - Coloque a imagem em: `public/assets/markers/`
   - Exemplo: `public/assets/markers/custom-marker.patt`
   - Exemplo: `public/assets/markers/custom-marker.png`

3. **Configurar no `ra.json`:**
   ```json
   {
     "configuracoes": {
       "markerUrl": "/assets/markers/custom-marker.patt",
       "markerImageUrl": "/assets/markers/custom-marker.png"
     }
   }
   ```

4. **Para usar URL externa:**
   ```json
   {
     "configuracoes": {
       "markerUrl": "https://seu-site.com/markers/custom-marker.patt",
       "markerImageUrl": "https://seu-site.com/markers/custom-marker.png"
     }
   }
   ```

---

## 📋 Checklist para Criar um Marker

- [ ] Escolher uma ferramenta de geração
- [ ] Gerar o arquivo `.patt` (pattern)
- [ ] Baixar a imagem do marker
- [ ] Testar a qualidade da imagem (boa resolução, contraste)
- [ ] Adicionar os arquivos ao projeto
- [ ] Configurar no `ra.json`
- [ ] Testar no aplicativo

---

## 💡 Dicas Importantes

### Para Melhor Detecção:
- ✅ Use markers com **alto contraste** (preto e branco funcionam melhor)
- ✅ Imprima em **papel branco** de boa qualidade
- ✅ Tamanho mínimo: **8cm x 8cm** (quanto maior, melhor)
- ✅ Mantenha o marker **plano** (sem dobrar ou amassar)
- ✅ Boa **iluminação** (evite sombras sobre o marker)
- ✅ Mantenha o marker **parado** durante a detecção

### Problemas Comuns:
- ❌ Marker muito pequeno → Aumente o tamanho
- ❌ Pouca luz → Melhore a iluminação
- ❌ Marker dobrado/amassado → Use um novo
- ❌ Câmera muito longe → Aproxime-se do marker
- ❌ Marker muito escuro/claro → Ajuste o contraste

---

## 🔗 Links Úteis

- **Marker Hiro (Padrão):** https://jeromeetienne.github.io/AR.js/data/images/HIRO.jpg
- **AR.js Marker Generator:** https://jeromeetienne.github.io/AR.js/three.js/examples/marker-training/examples/generator.html
- **NFT Marker Creator:** https://carnaux.github.io/NFT-Marker-Creator/
- **Documentação AR.js:** https://ar-js-org.github.io/AR.js-Docs/
- **Mais Markers Pré-fabricados:** https://github.com/AR-js-org/AR.js/tree/master/data/data

---

## 📝 Exemplo de Configuração Completa

```json
{
  "metadados": {
    "marca": "CQT",
    "codigo": "ARCO"
  },
  "configuracoes": {
    "usarAFrame": true,
    "usarVideo": true,
    "usarFaceTracking": false,
    "cameraFacing": "environment",
    "markerUrl": "https://cdn.jsdelivr.net/gh/AR-js-org/AR.js@master/data/data/patt.hiro",
    "markerImageUrl": "https://jeromeetienne.github.io/AR.js/data/images/HIRO.jpg"
  }
}
```

---

**Pronto!** Agora você sabe como obter e criar markers para seu projeto AR! 🚀

