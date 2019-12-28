# Instalando no Linux (debian)

    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh

Obtive...

    This can be modified with the CARGO_HOME environment variable.

    Rustup metadata and toolchains will be installed into the Rustup
    home directory, located at:

    /home/flavio/.rustup

    This can be modified with the RUSTUP_HOME environment variable.

    This path will then be added to your PATH environment variable by
    modifying the profile file located at:

    /home/flavio/.profile

    You can uninstall at any time with rustup self uninstall and
    these changes will be reverted.

    Current installation options:


    default host triple: x86_64-unknown-linux-gnu
        default toolchain: stable
                profile: default
    modify PATH variable: yes

    1) Proceed with installation (default)
    2) Customize installation
    3) Cancel installation

Escolhe a primeira opção e...

    info: profile set to 'default'
    info: default host triple is x86_64-unknown-linux-gnu
    info: syncing channel updates for 'stable-x86_64-unknown-linux-gnu'
    info: latest update on 2019-12-19, rust version 1.40.0 (73528e339 2019-12-16)
    info: downloading component 'cargo'
    info: downloading component 'clippy'
    info: downloading component 'rust-docs'
    11.9 MiB /  11.9 MiB (100 %)   8.8 MiB/s in  1s ETA:  0s
    info: downloading component 'rust-std'
    18.5 MiB /  18.5 MiB (100 %)   8.6 MiB/s in  2s ETA:  0s
    info: downloading component 'rustc'
    57.8 MiB /  57.8 MiB (100 %)   8.2 MiB/s in  7s ETA:  0s
    info: downloading component 'rustfmt'
    info: installing component 'cargo'
    info: installing component 'clippy'
    info: installing component 'rust-docs'
    11.9 MiB /  11.9 MiB (100 %)   6.8 MiB/s in  1s ETA:  0s
    info: installing component 'rust-std'
    18.5 MiB /  18.5 MiB (100 %)  13.6 MiB/s in  1s ETA:  0s
    info: installing component 'rustc'
    57.8 MiB /  57.8 MiB (100 %)  10.9 MiB/s in  5s ETA:  0s
    info: installing component 'rustfmt'
    info: default toolchain set to 'stable'

    stable installed - rustc 1.40.0 (73528e339 2019-12-16)


    Rust is installed now. Great!

    To get started you need Cargo's bin directory ($HOME/.cargo/bin) in your PATH
    environment variable. Next time you log in this will be done
    automatically.

    To configure your current shell run source $HOME/.cargo/env



### Deu certo ?

Reinicie seu termnal.

Execute...

    rustc --version

No meu caso, deu ruim.

    bash: rustc: comando não encontrado

( que saudade do Windows !!! )

Na documentação fala que tudo é criado na pasta `.cargo/`, fui lá e encontrei na raiz da pasta um arquivo chamado `env`. Dentro dele, contia o seguinte comando:

    export PATH="$HOME/.cargo/bin:$PATH"

Será que essa porra vai funcionar ? Executei e nada (beleza, deu certo).

"Nada", neste caso, significa que deu certo.

Sem precisar reinicar o terminal executei `rustc --version` e voilá...

    rustc 1.40.0 (73528e339 2019-12-16)

Acho que foi e a saudade do Windows passou.

Por preucação, nem vou reinicar o terminal.



