```mermaid
flowchart LR
  A[Bloco A] --> B[Bloco B]
  B --> C[Bloco C]

- As três crases abrem e fecham o bloco.
- Após as primeiras crases você indica `mermaid`.
- Depois vem o tipo de diagrama (`flowchart`, `sequenceDiagram`, `classDiagram`, etc.) e a direção (`LR` = left-to-right, `TB` = top-to-bottom).

---

## 3. Exemplo aplicado (CPU x Memória x I/O)

```mermaid
flowchart LR
  subgraph CPU["CPU"]
    ALU[ULA]
    REG[Registradores]
    CU[UC]
  end

  subgraph MEM["Memória"]
    ROM[ROM]
    RAM[RAM]
  end

  subgraph IO["Entrada/Saída"]
    IIF[Interface I/O]
    DEV[Dispositivos]
  end

  CPU -- "Address Bus" --> MEM
  CPU -- "Data Bus" --> MEM
  CPU -- "Control Bus" --> MEM

  CPU -- "Address Bus" --> IO
  CPU -- "Data Bus" --> IO
  CPU -- "Control Bus" --> IO
