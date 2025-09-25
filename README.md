# HS25-webeC

GitHub-Page: https://norarxmos.github.io/HS25-webeC/Example.html

>## Assignment 1
>Choose one of the following topics and create an HTML solution that you can extend over the course of this semester.
>
>### Possible topics
>
>* A web solution to keep track of your daily learning achievements.
>* A web solution to keep track of your programming errors.
>* A web solution to keep track of your plans in life.


## Topic
ToDo-Applikation mit inkludiertem Zeittracking für Hausaufgaben und Alltägliches.

***

### **Feature 1: Task-Management und Erstellung von ToDos**

**Idee**: Du kannst Aufgaben anlegen, bearbeiten, und löschen. Jede Aufgabe kann eine Beschreibung, eine Deadline und Priorität haben. Aufgaben können als erledigt markiert werden.

**Technische Umsetzung**:

* **HTML**: Erstelle Formulare für das Hinzufügen und Bearbeiten von Aufgaben.
* **CSS**: Style die Aufgabenliste und verwende ein einfaches Layout (z.B. Flexbox oder Grid).
* **JavaScript**: Implementiere Funktionen, um Aufgaben zu erstellen, anzuzeigen und zu löschen.
* **Backend (Grails)**: Speichere Aufgaben in einer Datenbank und rufe sie bei jedem Seitenaufruf ab.
  
***

### **Feature 2: Fortschrittsbalken**

**Idee**: Jede Aufgabe erhält einen Fortschrittsbalken, der den Arbeitsfortschritt anzeigt. Der Fortschritt kann manuell angepasst oder automatisch aktualisiert werden, wenn eine Aufgabe als erledigt markiert wird.

**Technische Umsetzung**:

* **CSS**: Implementiere einen anpassbaren Fortschrittsbalken, der in Prozent die erledigte Arbeit anzeigt.
* **JavaScript**: Ermögliche das dynamische Anpassen des Fortschritts, z.B. durch eine Schaltfläche "Fortschritt aktualisieren".
* **Backend (Grails)**: Speichere den Fortschritt der Aufgabe in der Datenbank.
  
***

### **Feature 3: Farbige Kennzeichnung**

**Idee**: Aufgaben können nach Dringlichkeit oder Wichtigkeit farblich markiert werden, um schnell die wichtigsten Aufgaben zu erkennen. Dies kann über ein Dropdown-Menü oder Tags geschehen.

**Technische Umsetzung**:

* **CSS**: Verwende Farben zur Kennzeichnung der Aufgaben (z.B. rot für hohe Dringlichkeit, grün für erledigt).
* **JavaScript**: Ermögliche es, beim Erstellen oder Bearbeiten einer Aufgabe eine Farbe oder Priorität auszuwählen.
* **Backend (Grails)**: Speichere die Farbzuweisung in der Datenbank und zeige sie auf der Benutzeroberfläche an.
  
***

### **Feature 4: Filter und Sortierung**

**Idee**: Die Aufgaben können nach verschiedenen Kriterien wie Deadline, Priorität oder Fortschritt sortiert und gefiltert werden.

**Technische Umsetzung**:

* **JavaScript**: Implementiere ein Filter- und Sortiersystem, das es dem Benutzer ermöglicht, Aufgaben nach Deadline, Priorität oder Status zu sortieren und zu filtern.
* **Backend (Grails)**: Die Aufgaben können auch serverseitig nach Kriterien gefiltert werden, wenn dies gewünscht wird.
  
***

### **Feature 5: Zeiterfassung (Start/Stop Timer)**

**Idee**: Du kannst für jede Aufgabe einen Timer starten und stoppen. Die Zeit wird erfasst und gespeichert, aber erst wenn die Aufgabe als erledigt markiert wird, wird die Gesamtzeit zur Schätzung für zukünftige Aufgaben verwendet.

**Technische Umsetzung**:

* **HTML/CSS**: Füge für jede Aufgabe einen Start/Stop-Button und eine dynamische Anzeige der verstrichenen Zeit hinzu.
* **JavaScript**:

  * Verwende `setInterval()` zum Starten des Timers und `clearInterval()` zum Stoppen.
  * Zeige die verstrichene Zeit in Echtzeit an (z.B. in Stunden:Minuten:Sekunden).
  * Wenn die Aufgabe als erledigt markiert wird (Checkbox), wird die gesammelte Zeit gespeichert und in der Datenbank abgelegt.
* **Backend (Grails)**: Speichere die erfasste Zeit in der Datenbank für jede Aufgabe. Diese Zeiten könnten später verwendet werden, um die durchschnittliche benötigte Zeit für ähnliche Aufgaben zu schätzen.
  
***

### **Feature 6: Benachrichtigungen und Erinnerungen**

**Idee**: Du kannst Erinnerungen für Deadlines und wichtige Aufgaben erstellen. Diese Erinnerungen können entweder als Pop-up im Browser oder innerhalb der App angezeigt werden. Zusätzlich gibt es eine Funktion, die einmal wöchentlich eine Erinnerungs-E-Mail an den Benutzer sendet.

**Technische Umsetzung**:

* **HTML/CSS**: Zeige Erinnerungen als Pop-ups innerhalb der App oder als Notification im Browser an. Verwende kleine Icons (z.B. eine Uhr) zur visuellen Darstellung der Erinnerungen.
* **JavaScript (Browser)**:

  * Nutze die **Notification API**, um Browser-Pop-ups anzuzeigen, die dich an wichtige Aufgaben erinnern.
  * **setTimeout()** oder **setInterval()** kann verwendet werden, um automatische Erinnerungen zu erstellen, die auf Deadlines basieren.
* **Backend (Grails)**:

  * Plane serverseitig Erinnerungen mithilfe von Cron-Jobs oder ähnlichen Mechanismen. Du könntest eine API erstellen, die täglich überprüft, welche Aufgaben bald fällig sind, und diese an die Nutzer erinnert.
  * **E-Mail-Benachrichtigung**: Verwende einen Job (wie den oben genannten Cron-Job), um einmal wöchentlich eine E-Mail mit allen bevorstehenden Aufgaben und Deadlines zu senden.

