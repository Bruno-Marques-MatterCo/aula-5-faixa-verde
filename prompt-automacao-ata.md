# Automação: Gerador de Ata de Reunião com Claude Code

Cole o prompt abaixo no Claude Code:

```
Crie um script em Python que fique rodando continuamente vigiando a pasta 
~/Downloads. Quando um novo arquivo .docx aparecer nessa pasta:

1. Leia o conteúdo do documento Word
2. Identifique se parece uma transcrição ou anotação de reunião (procure por 
   nomes de participantes, falas, ou marcações de tempo)
3. Se for, gere uma ATA estruturada com:
   - Data e participantes (extraídos do texto ou do nome do arquivo)
   - Pauta discutida (resumida em tópicos)
   - Decisões tomadas
   - Ações e responsáveis (quem ficou de fazer o quê)
   - Prazos mencionados
4. Marque cada ação com Confiança (Alta/Média/Baixa) — Baixa quando não 
   ficar claro quem é o responsável ou qual o prazo
5. Salve como "ATA - [nome do arquivo] - [data].docx" na mesma pasta
6. Envie notificação do sistema: "ATA gerada. X ações identificadas, 
   Y precisam de confirmação"
7. Continue vigiando — não pare depois de processar um arquivo

Use a biblioteca watchdog para monitorar a pasta e python-docx para ler e 
gerar arquivos Word.

Depois de criar o script, me explique como ele funciona: como o vigia de 
pasta detecta o novo arquivo, como a leitura do Word acontece, e como 
rodar isso em segundo plano no meu sistema.
```
