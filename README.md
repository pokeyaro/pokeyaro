<!--
### Hi there 👋

**PokeyBoa/PokeyBoa** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

## Hi there, I’m [@Ρσkəγα](https://github.com/pokeyaro) 👋

> Role: Software Engineer
>
> Fascinated by: [`NASM`](https://www.nasm.us/) [`Rust`](https://www.rust-lang.org/) [`Go`](https://go.dev/) [`TypeScript`](https://www.typescriptlang.org/) [`React`](https://react.dev/) [`Blender`](https://www.blender.org/) 
> *(yep, from bare metal to beautiful UIs — I enjoy every layer!)*
>
> Tech Stack: 
> <a href="https://www.linux.org/">
>   <img align="center" width="18" height="18" alt="tux" src="https://www.kernel.org/theme/images/logos/favicon.png" />
> </a>
> <a href="https://www.python.org/">
>   <img align="center" width="18" height="18" alt="pythonista" src="https://www.python.org/static/apple-touch-icon-144x144-precomposed.png" /> 
> </a>
> <a href="https://www.postgresql.org">
>   <img align="center" width="18" height="18" alt="pgsql" src="https://www.postgresql.org/favicon.ico" /> 
> </a>
> <a href="https://www.docker.com/">
>   <img align="center" width="18" height="18" alt="docker" src="https://www.docker.com/wp-content/uploads/2023/04/cropped-Docker-favicon-192x192.png" /> 
> </a>
> <a href="https://kubernetes.io/">
>   <img align="center" width="18" height="18" alt="k8s" src="https://kubernetes.io/icons/favicon-32.png" /> 
> </a>
> <a href="https://about.gitlab.com/">
>   <img align="center" width="18" height="18" alt="git" src="https://about.gitlab.com/nuxt-images/ico/favicon.ico" />
> </a>
> <a href="https://vuejs.org/">
>   <img align="center" width="18" height="18" alt="vue" src="https://vuejs.org/logo.svg" />
> </a>
> <a href="https://tailwindcss.com/">
>   <img align="center" width="18" height="18" alt="tailwind" src="https://tailwindcss.com/favicons/favicon-16x16.png" />
> </a>
>
> Who I Am: Exploring new tech, building things from scratch, lifting heavy things, vibing to music, and thinking deeply.
> 
> What I Value: Balance life, love code, and never stop growing. 🌱
>
> Why I Code: To light a small corner of the world with something truly my own! 💖

---

## 🧾 The Bootscroll
*A poem encoded at `0x7C00` — where machines awaken, and ideas persist.*

```Python
# Programming isn't just about syntax —
# it's about encoding ideas
# in ways machines love and humans fear.
#
# 编程的本质不仅是语法 —
# 是将想法编码成机器喜爱，
# 而人类敬畏的形式。

import subprocess

image = "ROM.img"

runes = [
    'a', 'b', 'c', 'd', 'e', 'f', 'g',
    'h', 'i', 'j', 'k', 'l', 'm', 'n',
    'o', 'p', 'q', 'r', 's', 't', 'u',
    'v', 'w', 'x', 'y', 'z', ' ', '.',
]

bit_mantra = [
    0b0001_1001, 0b0000_0100, 0b0001_0001, 0b0000_1110,
    0b0001_1010, 0b0000_1000, 0b0001_0010, 0b0001_1010,
    0b0000_1101, 0b0000_1110, 0b0001_0011, 0b0001_1010,
    0b0000_1101, 0b0000_1110, 0b0001_0011, 0b0000_0111,
    0b0000_1000, 0b0000_1101, 0b0000_0110, 0b0001_1011
]

boot_poem = (lambda λ: '"' + λ + '"')(
    "".join(
        runes[idx].upper() if i == 0 else runes[idx] if isinstance(idx, int) else idx
        for i, idx in enumerate(bit_mantra)
    )
)

# [org 0x7C00]
bios_scroll = bytes(
    # mov ah, 0x00
    # mov al, 0x03
    # int 0x10
    [
        0xB8, 0x03, 0x00,
        0xCD, 0x10,
    ] +
    # mov ah, 0x0E
    # mov al, <char>
    # int 0x10
    [
        0xB4, 0x0E,
        *sum([[0xB0, ord(db), 0xCD, 0x10] for db in boot_poem], []),
    ] +
    # hlt
    [
        0xF4,
    ] +
    # times 510-($-$$) db 0
    [
        0x66  # please print 666 on the BIOS wall. 请把 666 飘在公屏上 🔥
    ] * (510 - (3 + 2 + 2 + 4 * len(boot_poem) + 1)) +
    # dw 0xAA55
    [
        0x55, 0xAA
    ]
)

def zero():
    """ 🕯️ Begin invocation sequence """
    print(f'BIOS says: {boot_poem}')
    with open(image, "wb") as f:
        f.write(bios_scroll)
    subprocess.run(
        ["qemu-system-i386", "-drive", f"file={image},format=raw,if=floppy", "-serial", "stdio"],
        stdout=subprocess.DEVNULL,
        stderr=subprocess.DEVNULL
    )

if __name__ == '__main__':
    zero()

```

---

## 📊 GitHub Stats

<div style="display: flex; gap: 20px;">
  <a href="https://github.com/anuraghazra/github-readme-stats/" style="flex: 1;">
    <img style="width: 50%; height: auto; margin-right: 200px;" src="https://github-readme-stats.vercel.app/api?username=pokeyaro&bg_color=30,e96443,904e95&title_color=fff&text_color=fff" />
  </a>
  <a href="https://github.com/anuraghazra/github-readme-stats/" style="flex: 1;">
    <img style="width: 40%; height: auto;" src="https://github-readme-stats.vercel.app/api/top-langs/?username=pokeyaro&layout=compact" />
  </a>
</div>

## 👀 Visitors

![pic](http://profile-counter.glitch.me/pokeyaro/count.svg)

Thanks for dropping in! Feel free to poke around. 🧸


## 📞 Contact me

You can reach me by <a href="mailto:pokeya.mystic@gmail.com">📧 Email</a>.
