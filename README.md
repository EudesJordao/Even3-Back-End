# IA Mentora de TCC 

Este é o backend de uma aplicação que utiliza inteligência artificial (OpenAI) para ajudar estudantes na orientação de seus Trabalhos de Conclusão de Curso (TCC). Desenvolvido com FastAPI.

---

## Funcionalidades

- API REST com FastAPI.
- Integração com OpenAI (ChatGPT) para respostas inteligentes e empáticas.
- Endpoint `/chat` para envio de mensagens do usuário e retorno da IA mentora.
- Suporte a CORS para integração com frontends externos.
- **Banco de dados removido nesta versão para simplificação.**

---

## Pré-requisitos

Antes de rodar o projeto, é necessário ter instalado:

- [Python 3.10+](https://www.python.org/downloads/)
- [pip](https://pip.pypa.io/en/stable/installation/)
- Uma conta e chave de API da OpenAI ([crie aqui](https://platform.openai.com/account/api-keys))

---

## Instalação

1. Clone este repositório:

```bash
git clone https://github.com/seu-usuario/seu-repo-backend.git
cd seu-repo-backend
```

2. Crie e ative um ambiente virtual (opcional, mas recomendado):

```bash
python -m venv venv
source venv/bin/activate     # Linux/macOS
venv\Scripts\activate      # Windows
```

3. Instale as dependências:

```bash
pip install -r requirements.txt
```

4. Crie um arquivo `.env` na raiz com sua chave da OpenAI:

```env
OPENAI_API_KEY=sua-chave-aqui
```

---

## Como rodar

Execute o servidor com:

```bash
uvicorn main:app --reload
```

A API estará disponível em:  
 `http://localhost:8000`

Você pode acessar a documentação interativa do Swagger em:  
`http://localhost:8000/docs`

---

## Endpoints principais

| Método | Rota     | Descrição                                |
|--------|----------|--------------------------------------------|
| POST   | `/chat`  | Envia uma mensagem para a IA mentora e recebe a resposta |

### Exemplo de corpo JSON para `/chat`:

```json
{
  "message": "Preciso de ajuda para definir o tema do meu TCC."
}
```

---

## Integração com o frontend

Este backend foi desenvolvido para ser usado com um frontend separado (por exemplo, hospedado no GitHub Pages). O CORS está configurado para aceitar requisições de qualquer origem (`*`), permitindo integração imediata com qualquer frontend.

---

## Estrutura dos arquivos

```
.
├── main.py         # Arquivo principal da API FastAPI
├── ia.py           # Função de chamada à API do ChatGPT
├── config.py       # Configuração da OpenAI API key
├── requirements.txt
├── .env            # Sua chave da OpenAI (não versionado)
```

---

## Testando

Você pode testar a API usando:

- [Swagger UI](http://localhost:8000/docs)
- [Insomnia](https://insomnia.rest/)
- [Postman](https://www.postman.com/)

---

## Licença

Este projeto é open-source e livre para uso educacional.  
Feito com 💙 para ajudar estudantes a desenvolverem seus TCCs de forma ética e consciente.
