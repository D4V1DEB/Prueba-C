# Jenkins Setup - Guía Rápida

## 1. INSTALAR

**Java 21:**
https://adoptium.net/
→ Temurin 21 LTS Windows x64

**Python 3.12+:**
https://www.python.org/downloads/

**Git:**
https://git-scm.com/download/win

**Jenkins:**
https://www.jenkins.io/download/
→ Windows LTS (.msi)

---

## 2. PRIMER INICIO JENKINS

1. Abre: http://localhost:8080
2. Contraseña inicial:
```
C:\ProgramData\Jenkins\.jenkins\secrets\initialAdminPassword
```
3. Install suggested plugins
4. Crea usuario admin

---

## 3. CREAR PIPELINE

1. New Item → Nombre: TrafficPulse → Pipeline
2. Configurar:
   - Pipeline script from SCM
   - Git
   - URL: https://github.com/jss930/AvanceIngSoftware.git
   - Branch: */merge1
   - Script Path: Jenkinsfile
3. Save → Build Now

---

## COMANDOS ÚTILES

```powershell
# Ver versión Java
java -version

# Reiniciar Jenkins
Restart-Service Jenkins

# Ver logs
Get-Content "C:\ProgramData\Jenkins\.jenkins\jenkins.err.log" -Tail 50
```
