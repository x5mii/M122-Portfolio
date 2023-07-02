# M122-Portfolio
Geschrieben von Samuel Lucena
# Datentypen analysieren
Im folgenden Modul habe ich im Powershell eine Sortiermachine gebaut.
## Einleitung
Mit diesem Skript kann man ganz einfach mehrere Dateien mit verschiedenen Dateitypen einfach sortieren. Man muss nur eingeben in welchem Ordner sich diese Dateien befinden und in welchen Ordner man sie gerne sortieren möchte.
## Wie man es benutzt
Auf das was ich mich hier fokusieren möchte ist, wie die Maschiene die einzelnen Dateien unterscheiden kann und sie einteilt. Da geht ziemlich einfach: 
```powershell
$ordnerMapping = @{ 
    ".txt" = "Textdateien"
    ".docx" = "Word-Dokumente"
    ".xlsx" = "Excel-Dateien"
    ".pptx" = "PowerPoint-Präsentationen"
    ".jpg" = "Bilddateien"
    ".pdf" = "PDF-Dokumente"
}
```
Man listet diese so wie oben auf,
```powershell
($ordnerMapping.ContainsKey($dateityp)) {
        $zielPfad = Join-Path -Path $zielOrdner -ChildPath $ordnerMapping[$dateityp]
```
und so werden diese eingeteilt und ein Ordner wird für sie erstellt.
## Und so startet man das Skript
Zunächst öffnet man das Skript in Powershell oder im Dateiexplorer. Im Dateiexplorer müss man die Datei Rechtsclicken und mit PowerShell öffnen.
![image](https://github.com/Xami28/Portfolo/assets/110893302/46ee2228-defa-40f9-a0fe-06d0afbd4778)
Dann folgt man gany einfach den Anweisungen.

## Berechtigung und Clients
Für die Ausführung des Skripts sind möglicherweise zusätzliche Berechtigungen erforderlich. Bitte überprüfen Sie, ob Ihre PowerShell ExecutionPolicy so eingestellt ist, dass die Ausführung von Skripts auf Ihrem Gerät erlaubt ist. Weitere Informationen zur ExecutionPolicy von PowerShell 5.1 finden Sie [hier](https://learn.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_execution_policies?view=powershell-5.1). Das Skript kann gleichzeitig auf verschiedenen Clients ausgeführt werden, erfordert jedoch nur ein Gerät, um ausgeführt zu werden.
