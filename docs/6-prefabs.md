### Prefabs

###Ethan (Jogador)
- Descrição: Personagem controlável principal do jogo.
- Quando são utilizados: Presente durante todo o jogo.
- Componentes: Sprite Renderer (AstroCat animado em diferentes estados); Rigidbody2D (movimentação com física); Collider2D (detecção de colisões); Audio Source (sons de passos, pulo, dano, etc.).
- Scripts: EthanMovement.cs (Controla os comandos de movimento), EthanCombat.cs (Controla a pistola e ataques básicos), EthanSurvival.cs (Gerencia o status da bateria da lanterna e munições da pistola)


###O Perseguidor (Antagonista)
- Descrição: Criatura das sombras que caça Ethan quando ele está sem luz.
- Quando são utilizados: Em trechos onde se quer aumentar a dificuldade.
- Componente: Sprite Renderer (inimigo animado), Rigidbody2D, Collider2D e Audio Source (som de ataque, dano).
- Scripts:PerseguidorAI.cs (Define os padrões de patrulha da criatura), PerseguidorDetection.cs (Monitora a presença de Ethan com base na iluminação), PerseguidorAttack.cs (Executa ataques quando Ethan está vulnerável (sem luz), PerseguidorAudio.cs (Controla os ruídos que o Perseguidor emite (sussurros, grunhidos, passos)).

###Sombras
- Descrição: Experimentos fracassados que ainda vagam pela fábrica.
- Quando são utilizados: Em trechos onde se quer aumentar a dificuldade.
- Componente: Sprite Renderer, Collider2D, Audio Source.
- Scripts: SombrasBehavior.cs (Define patrulha e comportamento reativo à lanterna, interage com colisores para detectar presença do jogador e rxecuta ataques ou foge dependendo da estratégia do jogador).

###Baterias 
- Descrição:  Recursos limitados espalhados pelo cenário.
- Quando são utilizados: São posicionadas estrategicamente para reabastecer energia.
- Componente: Sprite Renderer, Collider2D (trigger), Audio Source.
- Scripts: BatteryItem.cs (Controla a interação da bateria com o jogador) , BatteryUsage.cs (Consumo e Aplicação), BatterySpawn.cs (Distribuição no Cenário) e BatteryHUD.cs (Exibição na Interface).

###Lanternas
- Descrição:  Item essencial para manter O Perseguidor afastado
- Quando são utilizados: Quando queremos manter o perseguidor afastado.
- Componente: Sprite Renderer, Collider2D (trigger), Audio Source.
- Scripts: LanternaSystem.cs → Gerencia iluminação e consumo de bateria.

###Pistola
- Descrição: Arma de último recurso contra sombras
- Quando são utilizados: Quando queremos manter as sombras afastadas.
- Componente: Sprite Renderer, Collider2D (trigger), Audio Source.
- Scripts: InventoryManager.cs → Controla coleta e uso de munições.
