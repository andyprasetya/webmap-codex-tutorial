# Webmap Development #CODEX
[CODEX: **COD**ing **EX**perience]

Tutorial membangun __*webmap*__ sederhana yang memuat dan menampilkan data [Overture Maps Foundation](https://overturemaps.org/), dengan menggunakan [Next.js](https://nextjs.org/), [TailwindCSS](https://tailwindcss.com/), [shadcn/ui](https://ui.shadcn.com/), dan [OpenLayers](https://openlayers.org/).

## Persiapan dan Peralatan
## 1.1. Instalasi NVM
__NVM__ (Node Version Manager) adalah *tool* paling mendasar yang akan Anda butuhkan. Instalasinya sangat mudah, Anda cukup menjalankan:

```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```

atau

```sh
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.3/install.sh | bash
```
di *shell* / *terminal* Anda.
- Catatan: Untuk versi termutakhir, Anda dapat melihat di *repository* [NVM](https://github.com/nvm-sh/nvm).

Setelah instalasi `NVM` selesai, *logout* dari *shell* / *terminal* Anda, dan *login* lagi.

## 1.2. Instalasi `Node.js` versi termutakhir

- Command untuk memeriksa apakah `NVM` sudah terpasang sebagaimana mestinya:
```sh
$ nvm -v
```

- Command untuk instalasi `Node.js` versi LTS termutakhir (`krypton`):
```sh
$ nvm install --lts=krypton
```

- Command untuk memeriksa apakah `Node.js` sudah terpasang sebagaimana mestinya:
```sh
$ node -v

$ npm -v

$ npx -v
```

## 1.3. Modifikasi file `.bashrc` di *home* *directory* Anda:

*Copy* kode berikut ini:
```sh
cdnvm() {
    command cd "$@" || return $?
    nvm_path="$(nvm_find_up .nvmrc | command tr -d '\n')"

    # If there are no .nvmrc file, use the default nvm version
    if [[ ! $nvm_path = *[^[:space:]]* ]]; then

        declare default_version
        default_version="$(nvm version default)"

        # If there is no default version, set it to `node`
        # This will use the latest version on your machine
        if [ $default_version = 'N/A' ]; then
            nvm alias default node
            default_version=$(nvm version default)
        fi

        # If the current version is not the default version, set it to use the default version
        if [ "$(nvm current)" != "${default_version}" ]; then
            nvm use default
        fi
    elif [[ -s "${nvm_path}/.nvmrc" && -r "${nvm_path}/.nvmrc" ]]; then
        declare nvm_version
        nvm_version=$(<"${nvm_path}"/.nvmrc)

        declare locally_resolved_nvm_version
        # `nvm ls` will check all locally-available versions
        # If there are multiple matching versions, take the latest one
        # Remove the `->` and `*` characters and spaces
        # `locally_resolved_nvm_version` will be `N/A` if no local versions are found
        locally_resolved_nvm_version=$(nvm ls --no-colors "${nvm_version}" | command tail -1 | command tr -d '\->*' | command tr -d '[:space:]')

        # If it is not already installed, install it
        # `nvm install` will implicitly use the newly-installed version
        if [ "${locally_resolved_nvm_version}" = 'N/A' ]; then
            nvm install "${nvm_version}";
        elif [ "$(nvm current)" != "${locally_resolved_nvm_version}" ]; then
            nvm use "${nvm_version}";
        fi
    fi
}

alias cd='cdnvm'
cdnvm "$PWD" || exit
```

Buka file `.bashrc` dengan menggunakan `nano` text editor:
```sh
$ nano .bashrc
```

dan *paste* kode yang sudah Anda *copy* tadi ke baris paling-akhir file `.bashrc`.

Simpan perubahan dengan menekan *Ctrl* + *O*, tekan `<Enter>`, dan keluar dari `nano` dengan menekan *Ctrl* + *X*.

Setelah modifikasi file `.bashrc` selesai, *logout* dari *shell* / *terminal* Anda, dan *login* lagi.

Modifikasi file `.bashrc` ini akan memastikan secara otomatis bahwa versi `Node.js` yang aktif adalah versi yang termutakhir.

## 1.3. Instalasi `Yarn`:

- Command untuk instalasi `Yarn`:
```sh
$ npm install --global yarn
```

Setelah instalasi `Yarn` selesai, *logout* dari *shell* / *terminal* Anda, dan *login* lagi. Anda sekarang sudah siap untuk tahap berikutnya, yaitu __project scaffolding__.

## Selanjutnya: [Mengawali Proyek Next.js](https://github.com/andyprasetya/webmap-codex-tutorial/tree/feat/01-create-nextjs-project)
