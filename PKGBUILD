pkgname="openai-client-bin"
pkgdesc="OpenAI client made using PySide6 Qt"
pkgver="0.0.0"
pkgrel=1
arch=("x86_64")


license=('MIT')


# binaries in virtual environment will be removed
# if default behaviour makepkg is not overridden
options=(!strip)

# use pacman -Qs "package-name"
depends=("git>=2.0" "python>=3.5" "python-pip>=20.0")

provides=("openai-client")

# backup=(etc/$pkgname/{config.ini,wsetup.sh,xsetup.sh})
# backup=(~/.config/openai-client)
# backup=(home/${USER}/.config/openai-client)

source=("git+https://github.com/awesomeDev12/openai-client.git"
        "git+https://github.com/awesomeDev12/openai-client-arch-binaries.git"
        "launch_arch.sh")
# sha512sums=("SKIP")
sha512sums=("SKIP" "SKIP")

package() {
  # echo 'Hello to you!' > "${srcdir}/hello-world.sh"
  # cp "hello-world.sh" > "${srcdir}/hello-world.sh"
  mkdir -p "${pkgdir}/usr/bin"
  mkdir -p "${pkgdir}/usr/share"
  mkdir -p "${pkgdir}/usr/share/icons"
  mkdir -p "${pkgdir}/usr/share/applications"
  mkdir -p "${pkgdir}/opt"
  mkdir -p "${pkgdir}/opt/openai-client-bin"

  cp "${srcdir}/launch_arch.sh" "${pkgdir}/usr/bin/openai-client"

  cp "${srcdir}/openai-client/images/icons/desktop_icon.jpg" "${pkgdir}/usr/share/icons/openai-client.jpg"  
  cp "${srcdir}/openai-client/OpenAIClient.desktop" "${pkgdir}/usr/share/applications/openai-client.desktop"  

  # cp -r "${srcdir}/openai-client" "${pkgdir}/opt/openai-client"
  cp -r "${srcdir}/openai-client-arch-binaries/binaries" "${pkgdir}/opt/openai-client-bin/binaries"

  # mkdir -p "${pkgdir}/opt/openai-client/.venv"

  # pip install --upgrade venvs

  # python -m venv "${pkgdir}/opt/openai-client/.venv/openai-venv"
  # source "${pkgdir}/opt/openai-client/.venv/openai-venv/bin/activate"

  # pip install --upgrade pip
  # # pip install --upgrade venvs
  # pip install --upgrade PySide6
  # pip install --upgrade openai
  # which python
  # deactivate

  chmod +x "${pkgdir}/usr/bin/openai-client"


}


