Para usar o virtualenv em jupyter noteboos é necessário criar um novo kernel python.
Para atualizar o kernel com novas libs : basta instalar a lib no virtualenv que o kernel atualiza o contexto.

### Windows
Execute o powershell em mode Administrador e execute os seguinte comandos:
```
Set-ExecutionPolicy RemoteSigned
```
```
pip install virtualenv
```
```
python -m venv venv
```
```
venv\Scripts\activate
```
```
pip install ipykernel
```
```
python -m ipykernel install --user --name=kernel-venv
```
Apos isso, basta reiniciar o jupyter e/ou vcscode e selecionar o kernel **kernel-venv** no notebook.

### Linux
```
pip install virtualenv -y &&
virtualenv venv &&
source env/bin/activate &&
pip install jupyter &&
pip install ipython && pip install ipykernel &&
pip install -r requirements.txt &&
ipython kernel install --user --name=kernel-venv &&
python -m ipykernel install --user --name=kernel-venv 
```

Para listar todos os kernels:
```
jupyter kernelspec list
```
Para remover o kernel use:
```
jupyter kernelspec remove kernel-venv
```
