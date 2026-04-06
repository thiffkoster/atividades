# atividades 1

class Retangulo {
    constructor(largura, altura) {
      this.largura = largura;
      this.altura = altura;
    }
    calcularArea() { return this.largura * this.altura; }
    calcularPerimetro() { return 2 * (this.largura + this.altura); }
  }

# atividades 2

class Usuario {
    constructor(nome, senha) {
      this.nome = nome;
      this.senha = senha;
    }
    login(senhaInformada) {
      return this.senha === senhaInformada ? "Acesso concedido" : "Senha incorreta";
    }
  }

# atividades 3

class Carrinho {
    constructor() { this.produtos = []; }
    adicionar(nome, preco, qtd) { this.produtos.push({ nome, preco, qtd }); }
    calcularTotal() {
      return this.produtos.reduce((total, p) => total + (p.preco * p.qtd), 0);
    }
  }

# atividades 4

class Funcionario {
    calcularSalario() { return 2000; }
  }
  class Desenvolvedor extends Funcionario {
    calcularSalario() { return super.calcularSalario() + 3000; }
  }
  class Designer extends Funcionario {
    calcularSalario() { return super.calcularSalario() + 2000; }
  }

# atividades 5

class Conta {
    constructor(saldo) { this.saldo = saldo; }
    transferir(valor, destino) {
      if (this.saldo >= valor) {
        this.saldo -= valor;
        destino.saldo += valor;
        return true;
      }
      return false;
    }
  }

# atividades 6

class Produto {
    constructor(nome, estoque) {
      this.nome = nome;
      this.estoque = estoque;
    }
    vender(qtd) {
      if (this.estoque >= qtd) {
        this.estoque -= qtd;
        return "Venda realizada";
      }
      return "Estoque insuficiente";
    }
    repor(qtd) { this.estoque += qtd; }
  }

# atividades 7

class Livro {
    constructor(titulo) {
      this.titulo = titulo;
      this.disponivel = true;
    }
    emprestar() {
      if (this.disponivel) {
        this.disponivel = false;
        return `Você pegou ${this.titulo}`;
      }
      return "Livro indisponível";
    }
  }

# atividades 8

class Forma { calcularArea() {} }

class Circulo extends Forma {
  constructor(raio) { super(); this.raio = raio; }
  calcularArea() { return Math.PI * (this.raio ** 2); }
}

class Quadrado extends Forma {
  constructor(lado) { super(); this.lado = lado; }
  calcularArea() { return this.lado ** 2; }
}

# atividades 9

class SistemaLogin {
    constructor() { this.usuarios = []; }
    cadastrar(email, senha) {
      const existe = this.usuarios.find(u => u.email === email);
      if (!existe) {
        this.usuarios.push({ email, senha });
        return "Cadastro realizado!";
      }
      return "Erro: E-mail já cadastrado.";
    }
  }
