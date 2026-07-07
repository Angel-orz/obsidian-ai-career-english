---
topic: CNN
date: 2026-07-08
---

# German Workplace — CNN

## German AI Terms
| German | English | Pronunciation |
|--------|---------|---------------|
| die Faltung | Convolution | FAL-tung |
| der Kernel / der Filter | Kernel / Filter | KER-nel / FIL-ter |
| die Feature-Map | Feature Map | FEE-chur-map |
| das Max-Pooling | Max Pooling | max POO-ling |
| die Schrittweite | Stride | SHRIT-vai-tuh |
| das Transferlernen | Transfer Learning | TRANS-fer-ler-nen |
| das rezeptive Feld | Receptive Field | reh-tsep-TEE-veh feld |
| die Bildverarbeitung | Computer Vision | BILD-fer-ar-bai-tung |

## German Meeting Phrases
| German | English |
|--------|---------|
| "Wir verwenden ein vortrainiertes Modell und fine-tunen es auf unseren Daten." | "We use a pre-trained model and fine-tune it on our data." |
| "Die ersten Faltungsschichten erkennen Kanten und Texturen." | "The first convolution layers detect edges and textures." |
| "Mit Data Augmentation konnen wir unseren kleinen Datensatz kunstlich vergrossern." | "With data augmentation we can artificially enlarge our small dataset." |

## German Workplace Scenario
**Szenario:** Meeting mit dem Entwicklungsteam uber ein Bilderkennungsprojekt.

**Teamleiter:** "Wir haben nur 2.000 Bilder fur die Qualitatskontrolle. Reicht das fur ein CNN?"

**Sie:** "Ja, absolut — mit Transferlernen. Wir nehmen ein vortrainiertes ResNet-50, das bereits auf 1,2 Millionen ImageNet-Bildern trainiert wurde. Die ersten Schichten erkennen bereits Kanten und Texturen — das sind universelle Merkmale. Wir ersetzen nur die letzte Klassifikationsschicht und trainieren sie auf unseren 2.000 Bildern. Das dauert vielleicht 20 Minuten auf einer GPU."

**Teamleiter:** "Und wie verhindern wir Uberanpassung?"

**Sie:** "Mit Data Augmentation — wir spiegeln die Bilder zufallig, drehen sie leicht und variieren die Helligkeit. So wird aus einem Bild effektiv eine ganze Familie von Varianten. Das vergrossert unseren Trainingsdatensatz kunstlich um das 5- bis 10-fache."

## German Workplace Tips
> **Tip:** In German engineering environments, practical feasibility often matters more than state-of-the-art. Always mention compute requirements and training time: "Das Training dauert etwa 30 Minuten auf einer einzelnen GPU" shows you've thought about implementation, not just theory.

## Related
- [[CNN]] (04_meetings)
