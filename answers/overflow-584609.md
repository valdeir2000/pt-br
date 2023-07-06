# rfc7231

A [rfc7231](https://datatracker.ietf.org/doc/html/rfc7231#section-4.3.1), trata, na seção 4.3.1, sobre o assunto, mas não deixa claro.

> Uma carga útil (body) dentro de uma mensagem de solicitação GET não tem semântica definida; enviar um corpo de carga útil em uma solicitação GET **pode** fazer com que algumas implementações existentes rejeitem a solicitação.

Ela lhe dá possibilidade de rejeitar e retornar o erro _400 Bad Request_

# rfc2616 (obsoleta)

De acordo com a **seção 4.3**, do [rfc2616](https://datatracker.ietf.org/doc/html/rfc2616#section-4.3), que tratava sobre o corpo da requisição:

> "Um corpo de mensagem **não** deve ser incluído numa requisição se a especificação do método não permitir o envio de um organismo de entidade nos pedidos (um corpo)."

Neste caso, o cliente estaria ferindo a especificação.

**Mas o servidor, o que deve fazer?**

Ainda de acordo com a RFC2616, o servidor deve processar a requisição e ignorar o corpo da requisição.

> "Um servidor deve ler e encaminhar um corpo de mensagem em qualquer solicitação; se o método de solicitação não incluir semântica definida para um corpo de entidade, o corpo da mensagem deve ser ignorado ao lidar com a solicitação."

