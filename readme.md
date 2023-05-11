# Desafio frontend

## O resultado final desse projeto deve ficar o mais parecido com o link de referência mencionando abaixo, considerando apenas as seguintes sessões:
- Tela inicial (home)
- Sobre
- Contato
### Link de referência: [sqad.com.br](https://sqad.com.br)
---

**Principais pontos a serem levados em consideração:**
- Responsividade do site (smartphones, tablets e desktop)
- Ancoras nos menus para levar a cada sessão
- Integração com microsserviço sqadmail para disparo de email, podendo utilizar as libs fetch, axios ou ajax
- Não é permitido o uso de libs ou frameworks de css tais como bootstrap, material UI, Bulma, etc
- É permitido o uso de libs pequenas para coisas específicas como por exemplo, libs para menu mobile, libs para carrousel de fotos, icones, etc
- Necessário clonar este projeto em sua maquina e após concluído, subir no seu github pessoal e enviar o link por email para análise.

---

## Documentação sqadmail:
Para realizar o disparo do email é necessário fazer uma requisição na url https://mail.squadytecnologia.com.br/send/ utilizando o método POST.

Você precisará passar uma autenticação do tipo Bearer Token no header da requisição. 

Token: ```49f3ad6c6f1312b45f7b24fe567cb23bd9ad6c05```

O body da requisição deve ser do tipo Multipart Form contendo apenas um parâmetro chamado ```data```, que deve receber um JSON (como string) na seguinte estrutura:
```json
{
  "subject": "Desafio Frontend",
  "from_email": "noreply@squadytecnologia.com.br",
  "recipient_list": ["alisson@sqad.com.br"],
  "template_id": "f0622748-905e-42d3-a910-2f0ecd4edd8e",
  "context_template": {
		"%name%": "Nome digitado no formulário",
		"%phone%": "Celular digitado no formulário",
		"%email%": "Email digitado no formulário",
		"%subject%": "Assunto digitado no formulário",
		"%message%": "Mensagem digitado no formulário",
  }
}
```

## Boa sorte 😉