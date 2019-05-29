## Atajo para pushear branches.

Si usas bash:
```bash
echo "alias fpush=\"git push --set-upstream origin `git branch | grep \* | cut -d ' ' -f2`\"" >> ~/.bashrc
```

Si usas zsh (con o sin OMZ)
```bash
echo "alias fpush=\"git push --set-upstream origin `git branch | grep \* | cut -d ' ' -f2`\"" >> ~/.zshrc
```

Si usas fish con OMF
```bash
echo "alias fpush=\"git push --set-upstream origin `git branch | grep \* | cut -d ' ' -f2`\"" >> ~/.config/fish/conf.d/omf.fish
```

Si usas fish sin OMF
```bash
echo "Deberias visitar https://github.com/oh-my-fish/oh-my-fish";
```

Luego, el primer push lo hace solo tipeando "fpush", y los push siguientes pueden salir todos con "git push" asecas. Ese comando pushea el branch con el que se esta trabajando y crea el upstream para que no haga falta poner el "origin lalala" en el push.

Nota: despues de crear el alias, hay que abrir otra pestaña de la terminal o reiniciarla.
