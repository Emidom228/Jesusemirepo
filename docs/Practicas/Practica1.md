# Reporte de Práctica 1: Temporizador 555 en Modo Astable
**Institución:** Universidad Iberoamericana Puebla  
**Materia:** Introducción a la Mecatrónica  
**Tema:** Electrónica 101: Temporizador 55  

### Lista de materiales 
 1. (1x) Protoboard
 2. (1x) NE555
 3. (1x) LED 
 4. (1x) Resistor para LED de 330Ω 
 5. Resistores temporizadores:
    - RA=1kΩ
    - RB=10kΩ
 6. (1x) Capacitor electrolítico: 100µF 
 7. (1x) Capacitor cerámico: 10nF
 8. Cables de conexión (jumpers)
 9. (1x) Puntas de fuente.
 10. (1x) Puntas de osciloscopio 
 
### *Simulación*
<img src="simulación555.JPG" alt="Simulación del temporizador 555" width="400">
---

### Fórmulas
 En modo astable, el capacitor ***C*** se carga desde la fuente de alimentación a través de ***RA +RB***. Cuando alcanza 2/3 de ***Vcc***, el 555 activa un circuito de descarga donde ***C***, se descarga através de ***RB*** hasta llegar a 1/3 de ***Vcc***. Este proceso se repite continuamente y, por ello, el LED permanece parpadeando.  
 El tiempo que le lleva al capacitor cargarse y descargarse, determina la frecuencia con la que el LED parpadea. Esos tiempos se calculan con las siguientes fórmulas:  

 **Tiempo de carga**:$$t_{alto}=0.693(R_A+R_B)C$$             
 **Tiempo de descarga**:$$t_{bajo}=0.693(R_B)C$$  
 **Periodo**: $$T=t_{alto}+t_{bajo}%$$  
 **Frecuencia**: $$f=\frac{1}{T}=\frac{1.44}{(R_A+2R_B)C}$$  
 **Duty**: $$\frac{t_{alto}}{T}=\frac{R_A+R_B}{R_A+2R_B}\times100\%$$

### Tabla Comparativa 
| Magnitud | Teórico | Medido | % de error | Inst. de medición |
| --- | --- | --- | --- | --- | 
| Vcc (V) | 5.0 | 5.37 | 7.4% | Multimetro |
|V de salida en Alto (V) | 3.5 | 4.4V | 25.7% | Multimetro |
| Frecuencia  (Hz) | 0.69 | 5.37hz | 678% | Osciloscopio |
| Duty (%) | 52.4% | 55.18% |  5.30% | Osciloscopio |
| I del LED (mA) | 1.52mA | 1.47mA | 3.29% | Multimetro | 

Para conocer el porcentaje de error se utiliza la siguiente fórmula:  $ \large \%\,error=\frac{|teórico-medido|}{teórico}\times100$  

Al realizar la fórmula en las 5 magnitudes, nos dimos cuenta que la mayoria de los porcentajes variaban por un porcentaje mínimo, mientras que la frecuencia aumento por muchisimo 

