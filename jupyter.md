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
Apos isso, basta selecionar o kernel **kernel-venv** no notebook.

Para listar todos os kernels:
```
jupyter kernelspec list
```
Para remover o kernel use:
```
jupyter kernelspec uninstall kernel-venv
```
