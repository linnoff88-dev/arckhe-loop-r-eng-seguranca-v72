# SeguranÃ§a do Loop AutÃ´nomo â€” FormaÃ§Ã£o LOOP-R Engenharia (curso 4 de 6)

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Curso aberto e gratuito do INEMA.CLUB no formato INEMA Learning v7.2, em portuguÃªs, inglÃªs e espanhol:
**https://inematds.github.io/loop-r-eng-seguranca-v72/** Â· [EN](https://inematds.github.io/loop-r-eng-seguranca-v72/en/) Â· [ES](https://inematds.github.io/loop-r-eng-seguranca-v72/es/)

Oito aulas para quem roda os prÃ³prios agentes (Claude Code ou Codex) em loop: trÃ­ade letal, Regra de Dois, injeÃ§Ã£o pelo conteÃºdo que o agente lÃª, permissÃµes por etapa, hooks de guarda, sandbox provado na sua mÃ¡quina, porta humana para o irreversÃ­vel e auditoria do loop. Tom defensivo: nada aqui ataca sistemas de terceiros; as demonstraÃ§Ãµes sÃ£o locais, com agente falso.

## O kit (`kit/`)

Python 3 e bash; node sÃ³ para os hooks do [inema-agent-runtime](https://github.com/inematds/inema-agent-runtime). Todo ensaio roda sem chamar modelo. TrÃªs passos reais (`*/real.sh`) fazem uma chamada `claude -p` cada, pela sua assinatura.

| arquivo | aula | o que faz |
|---|---|---|
| `triade.py`, `mapas/` | 1, 2 | confere o mapa das sessÃµes contra a trÃ­ade letal e a Regra de Dois |
| `injecao/` | 3 | pÃ¡gina envenenada, agente falso (ingenuo, sem-saida, separado), canÃ¡rio |
| `permissoes/` | 4 | settings.json por etapa e `regra.py` (que regra decide um comando) |
| `hooks/` | 5 | `guarda.py` (PreToolUse que nega o irreversÃ­vel), `provar-guarda.sh`, `settings-exemplo.json` |
| `prova-isolamento.sh` | 6, 7 | quatro tentativas de fuga dentro de um wrapper e um veredito |
| `porta/`, `systemd/` | 7 | porta do irreversÃ­vel (pedir, aprovar com hash, executar uma vez) e modelo de unit |
| `auditar.py` | 8 | auditoria do mapa e checklist em Markdown |
| `blocos/`, `saidas/`, `capturar.sh`, `conferir-blocos.py` | â€” | os comandos das aulas, as saÃ­das capturadas em 19/10/2026 e a conferÃªncia de que o site mostra o que foi testado |

```bash
git clone https://github.com/inematds/loop-r-eng-seguranca-v72 ~/projetos/loop-r-eng-seguranca-v72
K=~/projetos/loop-r-eng-seguranca-v72/kit && python3 $K/triade.py $K/mapas/triagem.json
```

## Gerar o site

ConteÃºdo em `conteudo/<idioma>/` (JSON). O HTML Ã© gerado: `python3 gerar.py && python3 validar.py --links` (e `--lang en|es`). NÃ£o edite o HTML Ã  mÃ£o.

[INEMA.CLUB](https://inema.club) Â· conteÃºdo aberto e gratuito

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>