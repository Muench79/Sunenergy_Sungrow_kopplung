Der Home Assistant Blue Print für Multigerät Nulleinspeisung für Sunenergyxt 500 wurde angepasst. 
Problem bei Standart Script laden die Sunenergy xt die komplette PV Leistung der Sungrow Main PV Analge.
Aus diesem Grund wurde der Sungrow Batteriestatus eingelesen und ein schiebe Regler für den Ziel SOC von Sungrow sowie ein Faktor implemtiert
Wenn die Sungrow Speicher kleiner als Wert vom Schieberegler ist dann wird das negative_gs_budget_w mit einem Faktor versehen. 
Das sorgt dann dafür das die Sunenergyxt in ihrer AC Ladeleistung begrenzt werden und somit der Sungrow Main PV Speicher ausreichend geladen wird. 
Wenn der Sungrow Speicher 100% hat wird der Faktor intern auf 1 gesetzt und die Sunenergy xt können auf die max Ladeleistung zugreifen.
