# Introdução

Este repositório descreve, de maneira resumida, minha jornada seguindo os passos do [The Rust Book](https://doc.rust-lang.org/stable/book/), acompanhados por vídeos no YouTube para mais detalhes.

# 1. Começando
## 1.1 Instalação
### Instalando as ferramentas básicas
Instale o gerenciador de ferramentas do Rust, `rustup`, no Linux ou macOS. Com o `rustup`, é possível gerenciar várias versões do Rust em nossa máquina.

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Verifique se `rustup`, `rustc` e `cargo` foram instalados corretamente:
```sh
rustup --version
rustc --version
cargo --version
```

### Configurando o Visual Studio Code
Instale a extensão `rust-analyzer` no Visual Studio Code.

Mais detalhes na [página oficial do Visual Studio Code para Rust](https://code.visualstudio.com/docs/languages/rust).

## 1.2 Hello, world
Vamos escrever um "Hello, world!". Primeiro, crie o diretório do projeto (note que o padrão do Rust é usar underscore `_` para representar espaços no nome de arquivos):
```sh
mkdir -p cap_01/hello_world
cd cap_01/hello_world
```

Agora, crie um arquivo [main.rs](cap_01/hello_world/main.rs). Observe que `println!` é uma macro. Por enquanto, basta saber que macros contêm um ponto de exclamação `!`:
```rust
fn main() {
    println!("Hello, world!");
}
```

Compile e execute a função `main`:
```sh
rustc main.rs
./main
# Hello, world!
```

## 1.3 Usando Cargo
O Cargo é um sistema de gerenciamento de pacotes e também serve como ferramenta de compilação. A maioria dos projetos em Rust utiliza o Cargo em vez de chamar diretamente o `rustc`.

### Criando um projeto com Cargo
Crie o diretório do projeto:
```sh
cd cap_01
cargo new hello_cargo
cd hello_cargo
tree
# .
# ├── Cargo.toml
# └── src
#     └── main.rs
```

Observe que o comando gerou os arquivos [Cargo.toml](cap_01/hello_cargo/Cargo.toml) e [src/main.rs](cap_01/hello_cargo/src/main.rs). O `Cargo.toml` descreve as dependências do projeto, enquanto `src/main.rs` contém um "Hello, world!" por padrão.

Compile o projeto:
```sh
cargo build
```

Execute o binário gerado no diretório `target`:
```sh
./target/debug/hello_cargo
# Hello, world!
```

Ou execute diretamente com Cargo:
```sh
cargo run
# Hello, world!
```
