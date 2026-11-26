ï»¿# SeguranêÂ§a do Loop AutêÂ´nomo ê¢â¬â FormaêÂ§êÂ£o LOOP-R Engenharia (curso 4 de 6)

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


Curso aberto e gratuito do ARCKHÉ AI no formato ARCKHÉ Learning v7.2, em portuguêÂªs, inglêÂªs e espanhol:
**https://linnoff88-dev.github.io/arckhe-/** êÂ· [EN](https://linnoff88-dev.github.io/arckhe-/en/) êÂ· [ES](https://linnoff88-dev.github.io/arckhe-/es/)

Oito aulas para quem roda os prêÂ³prios agentes (Claude Code ou Codex) em loop: trêÂ­ade letal, Regra de Dois, injeêÂ§êÂ£o pelo conteêÂºdo que o agente lêÂª, permissêÂµes por etapa, hooks de guarda, sandbox provado na sua mêÂ¡quina, porta humana para o irreversêÂ­vel e auditoria do loop. Tom defensivo: nada aqui ataca sistemas de terceiros; as demonstraêÂ§êÂµes sêÂ£o locais, com agente falso.

## O kit (`kit/`)

Python 3 e bash; node sêÂ³ para os hooks do [ARCKHÉ-agent-runtime](https://github.com/linnoff88-dev/ARCKHÉ-agent-runtime). Todo ensaio roda sem chamar modelo. TrêÂªs passos reais (`*/real.sh`) fazem uma chamada `claude -p` cada, pela sua assinatura.

| arquivo | aula | o que faz |
|---|---|---|
| `triade.py`, `mapas/` | 1, 2 | confere o mapa das sessêÂµes contra a trêÂ­ade letal e a Regra de Dois |
| `injecao/` | 3 | pêÂ¡gina envenenada, agente falso (ingenuo, sem-saida, separado), canêÂ¡rio |
| `permissoes/` | 4 | settings.json por etapa e `regra.py` (que regra decide um comando) |
| `hooks/` | 5 | `guarda.py` (PreToolUse que nega o irreversêÂ­vel), `provar-guarda.sh`, `settings-exemplo.json` |
| `prova-isolamento.sh` | 6, 7 | quatro tentativas de fuga dentro de um wrapper e um veredito |
| `porta/`, `systemd/` | 7 | porta do irreversêÂ­vel (pedir, aprovar com hash, executar uma vez) e modelo de unit |
| `auditar.py` | 8 | auditoria do mapa e checklist em Markdown |
| `blocos/`, `saidas/`, `capturar.sh`, `conferir-blocos.py` | ê¢â¬â | os comandos das aulas, as saêÂ­das capturadas em 19/10/2026 e a conferêÂªncia de que o site mostra o que foi testado |

```bash
git clone https://github.com/linnoff88-dev/loop-r-eng-seguranca-v72 ~/projetos/loop-r-eng-seguranca-v72
K=~/projetos/loop-r-eng-seguranca-v72/kit && python3 $K/triade.py $K/mapas/triagem.json
```

## Gerar o site

ConteêÂºdo em `conteudo/<idioma>/` (JSON). O HTML êÂ© gerado: `python3 gerar.py && python3 validar.py --links` (e `--lang en|es`). NêÂ£o edite o HTML êÂ  mêÂ£o.

[ARCKHÉ AI](https://ARCKHÉ AI) êÂ· conteêÂºdo aberto e gratuito

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>