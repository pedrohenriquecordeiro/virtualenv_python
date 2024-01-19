Para usar o virtualenv em jupyter noteboos é necessário criar um novo kernel python.

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
